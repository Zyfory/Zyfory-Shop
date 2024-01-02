class Tienda:
    def __init__(self, nombre):
        self.nombre = nombre
        self.productos = []

    def agregar_producto(self, nombre, precio):
        self.productos.append(Producto(nombre, precio))

    def mostrar_productos(self):
        for producto in self.productos:
            print(f"Nombre: {producto.nombre}, Precio: {producto.precio}")

class Producto:
    def __init__(self, nombre, precio):
        self.nombre = nombre
        self.precio = precio

class Usuario:
    def __init__(self, nombre):
        self.nombre = nombre
        self.carrito = []

    def agregar_al_carrito(self, producto):
        self.carrito.append(producto)

    def mostrar_carrito(self):
        for producto in self.carrito:
            print(f"Nombre: {producto.nombre}, Precio: {producto.precio}")

# Crear la tienda
tienda = Tienda("Mi Tienda")

# Agregar productos
tienda.agregar_producto("Manzana", 0.5)
tienda.agregar_producto("Banana", 0.3)

# Mostrar productos
tienda.mostrar_productos()

# Crear usuario
usuario = Usuario("Juan")

# Agregar producto al carrito
usuario.agregar_al_carrito(tienda.productos[0])

# Mostrar carrito
usuario.mostrar_carrito()
