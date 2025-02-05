---
layout: post
title:  "Diferencias entre Función y Método"
date:   2025-02-05 05:39:14 -0500
categories: Python
---

En **Python**, tanto **funciones** como **métodos** son bloques de código reutilizables, pero tienen diferencias clave en su uso y contexto.

---

### **1. Función**
- Es un **bloque de código independiente** que puede recibir parámetros y devolver valores.
- Se define con `def` y puede ser utilizada en cualquier parte del código.
- No está ligada a una clase u objeto en particular.

#### **Ejemplo de Función:**
```python
def sumar(a, b):
    return a + b

resultado = sumar(5, 3)  # Llamada a la función
print(resultado)  # Salida: 8
```

Aquí, `sumar` es una función independiente que no depende de ninguna clase.

---

### **2. Método**
- Es una función que está **definida dentro de una clase** y opera sobre los objetos de esa clase.
- El primer parámetro de un método dentro de una clase es **`self`**, que representa la instancia del objeto.
- Puede acceder y modificar los atributos del objeto.

#### **Ejemplo de Método:**
```python
class Calculadora:
    def __init__(self, valor):
        self.valor = valor  # Atributo de la clase

    def sumar(self, otro_valor):
        return self.valor + otro_valor  # Método que usa self

# Crear un objeto de la clase Calculadora
calc = Calculadora(5)
resultado = calc.sumar(3)  # Llamada al método
print(resultado)  # Salida: 8
```

Aquí, `sumar` es un **método** porque está dentro de la clase `Calculadora` y usa `self` para acceder a los atributos del objeto.

---

### **Diferencias Clave**

- **Ubicación**  
  - Función: Independiente, fuera de clases  
  - Método: Dentro de una clase  

- **Uso de self**  
  - Función: No usa `self`  
  - Método: Usa `self` para acceder a atributos  

- **Llamado**  
  - Función: Se llama directamente  
  - Método: Se llama desde un objeto (`obj.metodo()`)  

- **Ejemplo de llamada**  
  - Función: `sumar(5, 3)`  
  - Método: `obj.sumar(3)`  

---
En otras palabras:
- **Usa funciones** cuando necesites código reutilizable que no dependa de una clase.
- **Usa métodos** cuando trabajes con **Programación Orientada a Objetos (POO)** y necesites manipular atributos de instancias.
