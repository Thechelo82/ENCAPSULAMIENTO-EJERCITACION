# ENCAPSULAMIENTO-EJERCITACION
TPs de Axel Chambi 5°5


class CuentaBancaria:
    def __init__(self, titular, saldo, numero_cuenta):
        self.titular = titular
        self.saldo = saldo
        self.numero_cuenta = numero_cuenta

    def depositar(self, cantidad):
        self.saldo += cantidad

    def retirar(self, cantidad):
        if cantidad <= self.saldo:
            self.saldo -= cantidad


class Libro:
    def __init__(self, titulo, autor, año_publicacion):
        self.titulo = titulo
        self.autor = autor
        self.año_publicacion = año_publicacion

    def descripcion(self):
        return f"{self.titulo} de {self.autor} ({self.año_publicacion})"

    def es_clasico(self):
        return 2025 - self.año_publicacion > 50


class Estudiante:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
        self.notas = []

    def agregar_nota(self, nota):
        self.notas.append(nota)

    def promedio(self):
        if self.notas:
            return sum(self.notas) / len(self.notas)
        return 0


class Rectangulo:
    def __init__(self, base, altura):
        self.base = base
        self.altura = altura

    def area(self):
        return self.base * self.altura

    def perimetro(self):
        return 2 * (self.base + self.altura)


class Empleado:
    def __init__(self, nombre, salario, departamento):
        self.nombre = nombre
        self.salario = salario
        self.departamento = departamento

    def aumentar_salario(self, porcentaje):
        self.salario += self.salario * porcentaje / 100

    def mostrar_informacion(self):
        return f"{self.nombre}, {self.departamento}, ${self.salario}"


class Producto:
    def __init__(self, nombre, precio, stock):
        self.nombre = nombre
        self.precio = precio
        self.stock = stock

    def aumentar_stock(self, cantidad):
        self.stock += cantidad

    def disminuir_stock(self, cantidad):
        if cantidad <= self.stock:
            self.stock -= cantidad


class Juego:
    def __init__(self, nombre, genero, precio):
        self.nombre = nombre
        self.genero = genero
        self.precio = precio

    def mostrar_informacion(self):
        return f"{self.nombre} ({self.genero}) - ${self.precio}"

    def esta_en_oferta(self, precio_oferta):
        return self.precio < precio_oferta


class Circulo:
    def __init__(self, radio):
        if radio >= 0:
            self.radio = radio
        else:
            self.radio = 0

    def area(self):
        return 3.1416 * self.radio ** 2

    def circunferencia(self):
        return 2 * 3.1416 * self.radio
