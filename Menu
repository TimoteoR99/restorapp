class Restaurante:
    def __init__(self, num_mesas):
        self.num_mesas = num_mesas
        self.mesas = {i: None for i in range(1, num_mesas + 1)}
        self.menu_cafes = {
            1: {'nombre': 'Café Americano', 'precio': 5.0},
            2: {'nombre': 'Café Latte', 'precio': 7.0},
            3: {'nombre': 'Café Mocha', 'precio': 8.0},
            4: {'nombre': 'Cappuccino', 'precio': 6.0},
            5: {'nombre': 'Expreso', 'precio': 6.5}
        }
        self.menu_tortas = {
            1: {'nombre': 'Torta de Chocolate', 'precio': 12.0},
            2: {'nombre': 'Torta de Vainilla', 'precio': 10.0},
            3: {'nombre': 'Torta de Zanahoria', 'precio': 9.0},
            4: {'nombre': 'Torta de Frutas', 'precio': 11.0},
            5: {'nombre': 'Torta Red Velvet', 'precio': 13.0}
        }
        self.menu_sandwich = {
            1: {'nombre': 'Sandwich de Jamón y Queso', 'precio': 8.0},
            2: {'nombre': 'Sandwich de Pollo', 'precio': 9.0},
            3: {'nombre': 'Sandwich Vegetariano', 'precio': 7.5},
            4: {'nombre': 'Sandwich de Atún', 'precio': 8.5},
            5: {'nombre': 'Sandwich de Roast Beef', 'precio': 10.0}
        }

    def mostrar_menu(self):
        print("Menú:")
        print("------")
        print("Cafés:")
        for cafe_id, cafe in self.menu_cafes.items():
            print(f"{cafe_id}. {cafe['nombre']} - ${cafe['precio']}")
        print("Tortas:")
        for torta_id, torta in self.menu_tortas.items():
            print(f"{torta_id}. {torta['nombre']} - ${torta['precio']}")
        print("Sandwiches:")
        for sandwich_id, sandwich in self.menu_sandwich.items():
            print(f"{sandwich_id}. {sandwich['nombre']} - ${sandwich['precio']}")

    def realizar_pedido(self, mesa, opcion):
        if mesa in self.mesas:
            if self.mesas[mesa] is None:
                if opcion in self.menu_cafes:
                    pedido = self.menu_cafes[opcion]
                elif opcion in self.menu_tortas:
                    pedido = self.menu_tortas[opcion]
                elif opcion in self.menu_sandwich:
                    pedido = self.menu_sandwich[opcion]
                else:
                    print("Opción inválida.")
                    return
                self.mesas[mesa] = pedido
                print(f"Pedido realizado en la mesa {mesa}: {pedido['nombre']}")
            else:
                print(f"La mesa {mesa} ya tiene un pedido.")
        else:
            print(f"Mesa {mesa} no válida.")

    def mostrar_pedidos(self):
        print("Pedidos:")
        print("--------")
        for mesa, pedido in self.mesas.items():
            if pedido is not None:
                print(f"Mesa {mesa}: {pedido['nombre']}")
            else:
                print(f"Mesa {mesa}: Sin pedido.")


restaurante = Restaurante(10)

# Mostrar el menú
restaurante.mostrar_menu()

# Realizar pedidos
restaurante.realizar_pedido(1, 2)  # Café Latte en la mesa 1
restaurante.realizar_pedido(5, 8)  # Opción inválida
restaurante.realizar_pedido(3, 3)  # Café Mocha en la mesa 3
restaurante.realizar_pedido(1, 3)  # Café Mocha en la mesa 1 (mesa ya tiene un pedido)

# Mostrar los pedidos realizados
restaurante.mostrar_pedidos()
