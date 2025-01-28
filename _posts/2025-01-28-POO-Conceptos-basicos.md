---
layout: post
title:  "Conceptos Básicos para Dominar la Programación Orientada a Objetos con Python"
date:   2025-01-28 10:50:14 -0500
categories: Unidad 1
---

## 1. Clases y Objetos
- **Clase**: Plantilla o blueprint para crear objetos. Define atributos y métodos.
- **Objeto**: Instancia de una clase, que sigue su estructura.

### Ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

persona1 = Persona("Alice", 30)  # Objeto
```

---

## 2. Atributos
- **Atributos de instancia**: Datos específicos de cada objeto, definidos con `self`.
- **Atributos de clase**: Compartidos por todas las instancias de la clase.

### Ejemplo:
```python
class Coche:
    ruedas = 4  # Atributo de clase

    def __init__(self, marca):
        self.marca = marca  # Atributo de instancia

coche1 = Coche("Toyota")
coche2 = Coche("Honda")
```

---

## 3. Métodos
- **Métodos de instancia**: Utilizan `self` para acceder a atributos/métodos.
- **Métodos de clase**: Usan `@classmethod` y reciben `cls` como parámetro.
- **Métodos estáticos**: Usan `@staticmethod` y no necesitan `self` ni `cls`.

### Ejemplo:
```python
class Calculadora:
    def sumar(self, a, b):
        return a + b  # Método de instancia

    @classmethod
    def info(cls):
        return "Clase Calculadora"  # Método de clase

    @staticmethod
    def restar(a, b):
        return a - b  # Método estático
```

---

## 4. Encapsulación
Restringe el acceso a atributos y métodos:
- **Públicos**: Accesibles desde cualquier parte (`self.atributo`).
- **Protegidos**: Usan `_atributo`, no se recomienda acceder directamente.
- **Privados**: Usan `__atributo`, sólo accesibles dentro de la clase.

### Ejemplo:
```python
class CuentaBancaria:
    def __init__(self, saldo):
        self.__saldo = saldo  # Atributo privado

    def mostrar_saldo(self):
        return self.__saldo
```

---

## 5. Herencia
Permite que una clase herede atributos y métodos de otra, fomentando la reutilización.

### Ejemplo:
```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hablar(self):
        pass  # Método genérico

class Perro(Animal):
    def hablar(self):
        return "Guau"

class Gato(Animal):
    def hablar(self):
        return "Miau"

perro = Perro("Fido")
print(perro.hablar())  # Guau
```

---

## 6. Polimorfismo
Permite que clases diferentes utilicen métodos con el mismo nombre pero con implementaciones distintas.

### Ejemplo:
```python
animales = [Perro("Fido"), Gato("Whiskers")]

for animal in animales:
    print(animal.hablar())
```

---

## 7. Abstracción
Define una interfaz común para clases relacionadas, omitiendo detalles innecesarios. Usa el módulo `abc`.

### Ejemplo:
```python
from abc import ABC, abstractmethod

class Figura(ABC):
    @abstractmethod
    def area(self):
        pass

class Cuadrado(Figura):
    def __init__(self, lado):
        self.lado = lado

    def area(self):
        return self.lado ** 2
```

---

## 8. Composición
Incluye objetos de una clase dentro de otra como atributos, en lugar de usar herencia.

### Ejemplo:
```python
class Motor:
    def iniciar(self):
        return "Motor iniciado"

class Coche:
    def __init__(self):
        self.motor = Motor()

coche = Coche()
print(coche.motor.iniciar())  # Motor iniciado
```

---

## 9. Manejo de Excepciones en POO
Es importante manejar errores para asegurar que el programa sea robusto.

### Ejemplo:
```python
class Division:
    def dividir(self, a, b):
        try:
            return a / b
        except ZeroDivisionError:
            return "Error: No se puede dividir entre cero"
```

---

## 10. Buenas Prácticas en POO
1. Nombrar clases usando **CamelCase** (ej. `MiClase`).
2. Mantener métodos cortos y con una única responsabilidad.
3. Usar herencia con moderación; preferir composición cuando sea posible.
4. Documentar clases y métodos para mejorar la mantenibilidad.
5. Escribir pruebas unitarias para verificar el comportamiento de las clases.

