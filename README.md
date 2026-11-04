[README (2).md](https://github.com/user-attachments/files/34399279/README.2.md)

# 30 funciones básicas de Python

Trabajo colaborativo en el que se investigan y documentan 30 funciones incorporadas (*built-in*) de Python. Para cada función se explica **para qué sirve**, su **sintaxis** y un **ejemplo práctico** con su resultado. Todo el contenido está en esta página; el mismo trabajo, ejecutable, está en el notebook [`00_funciones_python_completo.ipynb`](00_funciones_python_completo.ipynb).

**Asignatura:** Introducción a la Ciencia de Datos  
**Docente:** Carlos Andrés Gómez

## Integrantes

| Integrante | Usuario de GitHub | Funciones | Notebook original |
|---|---|---|---|
| David Navarro (ID 37011) | @david222001navarro-boop | 1 a 10 | [`01_funciones_1_a_10 .ipynb`](01_funciones_1_a_10%20.ipynb) |
| Daniel Gonzales (ID 46993) | _@usuario2_ | 11 a 20 | [`Funciones_11_a_20_Python_Zootecnia.ipynb`](Funciones_11_a_20_Python_Zootecnia.ipynb) |
| _Integrante 3_ | _@usuario3_ | 21 a 30 | _pendiente_ |

Cada integrante subió su parte con su propia cuenta; los commits de cada uno están en la pestaña **Commits** del repositorio.

## Introducción

Python incluye funciones incorporadas (*built-in*) que están disponibles sin instalar librerías adicionales y que se usan en casi todos los programas. En este trabajo se investigan y documentan **30 funciones básicas**. Para cada una se explica **para qué sirve**, su **sintaxis** y un **ejemplo práctico** con su resultado.

El trabajo se dividió entre los integrantes y aquí se reúne en una sola página.

| Parte | Responsable | Funciones |
|---|---|---|
| 1 | David Navarro | `print`, `input`, `type`, `int`, `float`, `str`, `bool`, `len`, `sum`, `min` |
| 2 | Daniel Gonzales | `max`, `abs`, `round`, `pow`, `range`, `sorted`, `reversed`, `enumerate`, `zip`, `any` |
| 3 | Integrante 3 | `all`, `list`, `tuple`, `set`, `dict`, `format`, `isinstance`, `help`, `dir`, `open` |

---
# Parte 1: funciones 1 a 10

_Desarrollada por: David Navarro_

## 1. `print()`

**¿Para qué sirve?** Muestra información en la pantalla. Es útil para comunicar resultados o revisar valores durante la ejecución.

**Sintaxis:** `print(*objetos, sep=' ', end='\n')`

**Parámetros y valor devuelto:** Recibe uno o varios valores separados por coma. `sep` define qué se pone entre ellos y `end` qué se pone al final. Devuelve `None`.

**Ten en cuenta:** Por defecto termina cada impresión con un salto de línea. Con `print('a', 'b', sep='-')` se obtiene `a-b`.

**Ejemplo práctico:**

```python
print("Hola, Python")
```

**Salida:**

```text
Hola, Python
```

**Resultado esperado:** Hola, Python

## 2. `input()`

**¿Para qué sirve?** Solicita al usuario que escriba un dato y lo devuelve como texto (`str`).

**Sintaxis:** `input(mensaje='')`

**Parámetros y valor devuelto:** Recibe un mensaje opcional que se muestra antes de esperar la escritura. Devuelve siempre un `str`.

**Ten en cuenta:** Aunque el usuario escriba un número, `input()` lo entrega como texto. Si se necesita un número hay que convertirlo con `int()` o `float()`.

**Ejemplo práctico:**

```python
nombre = input("Escribe tu nombre: ")
print("Hola,", nombre)
```

**Salida:**

```text
Escribe tu nombre:  DAVID
Hola, DAVID
```

**Resultado esperado:** Si se escribe Ana: Hola, Ana

## 3. `type()`

**¿Para qué sirve?** Indica el tipo de dato de un valor u objeto.

**Sintaxis:** `type(objeto)`

**Parámetros y valor devuelto:** Recibe un objeto y devuelve su clase, por ejemplo `<class 'int'>`.

**Ten en cuenta:** Sirve para comprobar qué tipo tiene una variable cuando un resultado no es el esperado.

**Ejemplo práctico:**

```python
print(type(25))
print(type("texto"))
```

**Salida:**

```text
<class 'int'>
<class 'str'>
```

**Resultado esperado:** <class 'int'>  
<class 'str'>

## 4. `int()`

**¿Para qué sirve?** Convierte un valor compatible en un número entero.

**Sintaxis:** `int(x=0, base=10)`

**Parámetros y valor devuelto:** Recibe un número o un texto que represente un entero. Devuelve un `int`.

**Ten en cuenta:** Si se le pasa un decimal lo trunca (`int(3.9)` da `3`). Con un texto no numérico, como `int('abc')`, lanza `ValueError`.

**Ejemplo práctico:**

```python
edad = int("20")
print(edad + 1)
```

**Salida:**

```text
21
```

**Resultado esperado:** 21

## 5. `float()`

**¿Para qué sirve?** Convierte un valor compatible en un número decimal.

**Sintaxis:** `float(x=0.0)`

**Parámetros y valor devuelto:** Recibe un número o un texto que represente un decimal. Devuelve un `float`.

**Ten en cuenta:** Los decimales se escriben con punto, no con coma: `float('12.5')` funciona y `float('12,5')` produce un error.

**Ejemplo práctico:**

```python
precio = float("12.5")
print(precio * 2)
```

**Salida:**

```text
25.0
```

**Resultado esperado:** 25.0

## 6. `str()`

**¿Para qué sirve?** Convierte un valor en una cadena de texto.

**Sintaxis:** `str(objeto)`

**Parámetros y valor devuelto:** Recibe cualquier objeto y devuelve su representación como `str`.

**Ten en cuenta:** Es necesaria para unir texto con números usando `+`, porque Python no mezcla ambos tipos automáticamente.

**Ejemplo práctico:**

```python
numero = 45
print("Número: " + str(numero))
```

**Salida:**

```text
Número: 45
```

**Resultado esperado:** Número: 45

## 7. `bool()`

**¿Para qué sirve?** Convierte un valor a verdadero (`True`) o falso (`False`) según las reglas de Python.

**Sintaxis:** `bool(x)`

**Parámetros y valor devuelto:** Recibe cualquier valor y devuelve `True` o `False`.

**Ten en cuenta:** Se consideran falsos el `0`, el texto vacío `''`, las colecciones vacías (`[]`, `{}`) y `None`. Casi todo lo demás es verdadero.

**Ejemplo práctico:**

```python
print(bool(1))
print(bool(0))
```

**Salida:**

```text
True
False
```

**Resultado esperado:** True  
False

## 8. `len()`

**¿Para qué sirve?** Devuelve la cantidad de elementos de una secuencia o colección, como texto, lista o tupla.

**Sintaxis:** `len(s)`

**Parámetros y valor devuelto:** Recibe un texto o una colección y devuelve un entero con su tamaño.

**Ten en cuenta:** En un texto cuenta caracteres, incluidos los espacios. Con un número, como `len(25)`, lanza `TypeError`.

**Ejemplo práctico:**

```python
fruta = "manzana"
print(len(fruta))
```

**Salida:**

```text
7
```

**Resultado esperado:** 7

## 9. `sum()`

**¿Para qué sirve?** Suma los elementos numéricos de un iterable, por ejemplo, una lista.

**Sintaxis:** `sum(iterable, start=0)`

**Parámetros y valor devuelto:** Recibe un iterable de números y un valor inicial opcional. Devuelve la suma total.

**Ten en cuenta:** Si la lista tiene decimales el resultado es decimal. No sirve para unir textos.

**Ejemplo práctico:**

```python
notas = [4.0, 3.5, 4.5]
print(sum(notas))
```

**Salida:**

```text
12.0
```

**Resultado esperado:** 12.0

## 10. `min()`

**¿Para qué sirve?** Devuelve el menor elemento de una colección o el menor de varios argumentos comparables.

**Sintaxis:** `min(iterable)   o   min(a, b, c, ...)`

**Parámetros y valor devuelto:** Recibe una colección o varios valores comparables. Devuelve el menor de ellos.

**Ten en cuenta:** También funciona con textos, que compara por orden alfabético. Con una colección vacía lanza `ValueError`.

**Ejemplo práctico:**

```python
temperaturas = [18, 22, 15, 20]
print(min(temperaturas))
```

**Salida:**

```text
15
```

**Resultado esperado:** 15

---
# Parte 2: funciones 11 a 20

_Desarrollada por: Daniel Gonzales (ejemplos aplicados a Zootecnia)_

En este notebook se explican diez funciones incorporadas de Python, desde `max()` hasta `any()`. Los ejemplos se relacionan con situaciones de Zootecnia, como el peso de animales, el consumo de alimento, los registros de una granja y el seguimiento de animales.

Reconocer para qué sirve cada función, comprender su sintaxis y aplicarla mediante ejemplos prácticos que se puedan ejecutar en Python.

> **Instrucción:** ejecuta cada celda de código para comprobar los resultados. Los datos de los ejemplos son ficticios y se usan únicamente con fines académicos.

## 11. `max()`

**¿Para qué sirve?**  
Devuelve el elemento de mayor valor de una colección o el mayor entre varios valores. Es útil para identificar, por ejemplo, el animal con mayor peso dentro de un grupo.

**Sintaxis general:** `max()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
pesos_kg = [42.5, 38.0, 45.2, 41.7, 39.8]
mayor_peso = max(pesos_kg)

print("El mayor peso registrado es:", mayor_peso, "kg")
```

**Salida:**

```text
El mayor peso registrado es: 45.2 kg
```

**Resultado esperado:**

```text
El mayor peso registrado es: 45.2 kg
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 12. `abs()`

**¿Para qué sirve?**  
Devuelve el valor absoluto de un número; es decir, elimina su signo negativo. Puede utilizarse para calcular la diferencia sin signo entre un peso esperado y uno registrado.

**Sintaxis general:** `abs()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
peso_esperado = 40
peso_registrado = 37.5

diferencia = abs(peso_esperado - peso_registrado)

print("La diferencia de peso es:", diferencia, "kg")
```

**Salida:**

```text
La diferencia de peso es: 2.5 kg
```

**Resultado esperado:**

```text
La diferencia de peso es: 2.5 kg
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 13. `round()`

**¿Para qué sirve?**  
Redondea un número al número de decimales indicado. Es útil para presentar promedios o mediciones con una cantidad determinada de decimales.

**Sintaxis general:** `round()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
pesos = [32.4, 34.7, 33.8]
promedio = sum(pesos) / len(pesos)
promedio_redondeado = round(promedio, 2)

print("Peso promedio:", promedio_redondeado, "kg")
```

**Salida:**

```text
Peso promedio: 33.63 kg
```

**Resultado esperado:**

```text
Peso promedio: 33.63 kg
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 14. `pow()`

**¿Para qué sirve?**  
Calcula una potencia: eleva el primer número al exponente indicado. Con dos argumentos, `pow(base, exponente)` equivale a `base ** exponente`.

**Sintaxis general:** `pow()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
lado_corral = 5
area_corral = pow(lado_corral, 2)

print("Área del corral:", area_corral, "m²")
```

**Salida:**

```text
Área del corral: 25 m²
```

**Resultado esperado:**

```text
Área del corral: 25 m²
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 15. `range()`

**¿Para qué sirve?**  
Genera una secuencia de números enteros. Se utiliza frecuentemente en ciclos `for` para repetir instrucciones un número determinado de veces. El límite final no se incluye.

**Sintaxis general:** `range()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
print("Registro de los primeros cinco días:")
for dia in range(1, 6):
    print("Día", dia)
```

**Salida:**

```text
Registro de los primeros cinco días:
Día 1
Día 2
Día 3
Día 4
Día 5
```

**Resultado esperado:**

```text
Registro de los primeros cinco días:
Día 1
Día 2
Día 3
Día 4
Día 5
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 16. `sorted()`

**¿Para qué sirve?**  
Devuelve una nueva lista con los elementos ordenados. Por defecto, ordena de menor a mayor y no modifica la lista original.

**Sintaxis general:** `sorted()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
pesos = [28.5, 31.2, 27.9, 30.0]
pesos_ordenados = sorted(pesos)

print("Pesos originales:", pesos)
print("Pesos ordenados:", pesos_ordenados)
```

**Salida:**

```text
Pesos originales: [28.5, 31.2, 27.9, 30.0]
Pesos ordenados: [27.9, 28.5, 30.0, 31.2]
```

**Resultado esperado:**

```text
Pesos originales: [28.5, 31.2, 27.9, 30.0]
Pesos ordenados: [27.9, 28.5, 30.0, 31.2]
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 17. `reversed()`

**¿Para qué sirve?**  
Permite recorrer los elementos de una secuencia en orden inverso. Devuelve un iterador; por eso, en este ejemplo se convierte a lista con `list()`.

**Sintaxis general:** `reversed()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
dias_registro = ["lunes", "martes", "miércoles", "jueves"]
dias_invertidos = list(reversed(dias_registro))

print("Orden inverso:", dias_invertidos)
```

**Salida:**

```text
Orden inverso: ['jueves', 'miércoles', 'martes', 'lunes']
```

**Resultado esperado:**

```text
Orden inverso: ['jueves', 'miércoles', 'martes', 'lunes']
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 18. `enumerate()`

**¿Para qué sirve?**  
Permite recorrer una colección obteniendo al mismo tiempo la posición (índice) y el elemento. Por defecto, el índice comienza en cero; se puede cambiar con `start`.

**Sintaxis general:** `enumerate()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
identificacion_animales = ["Bovino 101", "Bovino 102", "Bovino 103"]

for posicion, animal in enumerate(identificacion_animales, start=1):
    print(posicion, "-", animal)
```

**Salida:**

```text
1 - Bovino 101
2 - Bovino 102
3 - Bovino 103
```

**Resultado esperado:**

```text
1 - Bovino 101
2 - Bovino 102
3 - Bovino 103
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 19. `zip()`

**¿Para qué sirve?**  
Combina elementos de dos o más colecciones posición por posición. Es útil para relacionar cada animal con su peso. Si las colecciones tienen longitudes diferentes, se detiene al terminar la más corta.

**Sintaxis general:** `zip()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
animales = ["Ternera A", "Ternera B", "Ternera C"]
pesos = [95.5, 102.0, 98.3]

for animal, peso in zip(animales, pesos):
    print(animal, ":", peso, "kg")
```

**Salida:**

```text
Ternera A : 95.5 kg
Ternera B : 102.0 kg
Ternera C : 98.3 kg
```

**Resultado esperado:**

```text
Ternera A : 95.5 kg
Ternera B : 102.0 kg
Ternera C : 98.3 kg
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

## 20. `any()`

**¿Para qué sirve?**  
Devuelve `True` si al menos uno de los elementos de un iterable es verdadero; devuelve `False` si ninguno lo es. En este ejemplo se comprueba si algún animal supera el umbral de temperatura definido para el ejercicio.

**Sintaxis general:** `any()` se utiliza sobre uno o varios valores o colecciones, según el caso.

**Ejemplo práctico:**

El siguiente ejemplo aplica la función a una situación relacionada con el manejo de registros pecuarios.

```python
temperaturas_c = [38.2, 38.7, 39.6, 38.4]
hay_temperatura_superior = any(temp > 39.5 for temp in temperaturas_c)

print("¿Algún registro supera 39.5 °C?", hay_temperatura_superior)
```

**Salida:**

```text
¿Algún registro supera 39.5 °C? True
```

**Resultado esperado:**

```text
¿Algún registro supera 39.5 °C? True
```

**Interpretación:** El resultado permite comprender cómo la función ayuda a procesar información que puede aparecer en los registros de una explotación pecuaria.

---
# Parte 3: funciones 21 a 30

_Desarrollada por: Integrante 3_

## 21. `all()`

**¿Para qué sirve?** Devuelve `True` si todos los elementos de un iterable son verdaderos; con un iterable vacío también devuelve `True`.

**Sintaxis:** `all(iterable)`

**Parámetros y valor devuelto:** Recibe un iterable. Devuelve `False` en cuanto encuentra un elemento falso.

**Ten en cuenta:** Es la contraparte de `any()`. Es habitual para comprobar que se cumplen todos los requisitos de una lista.

**Ejemplo práctico:**

```python
requisitos = [True, True, True]
print(all(requisitos))
```

**Salida:**

```text
True
```

**Resultado esperado:** True

## 22. `list()`

**¿Para qué sirve?** Crea una lista a partir de un iterable o una lista vacía si no se proporciona argumento.

**Sintaxis:** `list(iterable=())`

**Parámetros y valor devuelto:** Recibe un iterable, como un texto o una tupla. Devuelve una lista con sus elementos.

**Ten en cuenta:** `list('aei')` separa el texto en una lista de caracteres.

**Ejemplo práctico:**

```python
vocales = list("aei")
print(vocales)
```

**Salida:**

```text
['a', 'e', 'i']
```

**Resultado esperado:** ['a', 'e', 'i']

## 23. `tuple()`

**¿Para qué sirve?** Crea una tupla, una colección ordenada que no puede modificarse después de creada.

**Sintaxis:** `tuple(iterable=())`

**Parámetros y valor devuelto:** Recibe un iterable y devuelve una tupla con sus elementos.

**Ten en cuenta:** Al ser inmutable, intentar asignar un elemento (`coordenadas[0] = 5`) produce un `TypeError`.

**Ejemplo práctico:**

```python
coordenadas = tuple([10, 20])
print(coordenadas)
```

**Salida:**

```text
(10, 20)
```

**Resultado esperado:** (10, 20)

## 24. `set()`

**¿Para qué sirve?** Crea un conjunto, que almacena elementos únicos y elimina duplicados.

**Sintaxis:** `set(iterable=())`

**Parámetros y valor devuelto:** Recibe un iterable y devuelve un conjunto sin elementos repetidos.

**Ten en cuenta:** Un conjunto no garantiza el orden de sus elementos. Por eso el ejemplo usa `sorted()` al imprimir.

**Ejemplo práctico:**

```python
codigos = set([1, 2, 2, 3])
print(sorted(codigos))
```

**Salida:**

```text
[1, 2, 3]
```

**Resultado esperado:** [1, 2, 3]

## 25. `dict()`

**¿Para qué sirve?** Crea un diccionario que almacena pares de clave y valor.

**Sintaxis:** `dict(clave=valor, ...)   o   dict(iterable_de_pares)`

**Parámetros y valor devuelto:** Recibe pares clave-valor. Devuelve un diccionario al que se accede por clave.

**Ten en cuenta:** Si se consulta una clave que no existe con `persona['correo']`, lanza `KeyError`.

**Ejemplo práctico:**

```python
persona = dict(nombre="Ana", edad=21)
print(persona["nombre"])
```

**Salida:**

```text
Ana
```

**Resultado esperado:** Ana

## 26. `format()`

**¿Para qué sirve?** Devuelve una representación formateada de un valor; resulta útil para presentar números con una cantidad específica de decimales.

**Sintaxis:** `format(valor, especificador='')`

**Parámetros y valor devuelto:** Recibe un valor y un código de formato. Devuelve un texto. El código `.2f` indica 2 decimales fijos.

**Ten en cuenta:** Otros códigos útiles: `,` para separador de miles y `.1%` para porcentajes.

**Ejemplo práctico:**

```python
caudal = 0.19
print(format(caudal, ".2f"))
```

**Salida:**

```text
0.19
```

**Resultado esperado:** 0.19

**Otro ejemplo con más decimales y separador de miles:**

```python
print(format(3.14159, ".2f"))
print(format(1500000, ","))
```

**Salida:**

```text
3.14
1,500,000
```

## 27. `isinstance()`

**¿Para qué sirve?** Comprueba si un objeto pertenece a un tipo de dato o a una familia de tipos.

**Sintaxis:** `isinstance(objeto, tipo)`

**Parámetros y valor devuelto:** Recibe un objeto y un tipo (o una tupla de tipos). Devuelve `True` o `False`.

**Ten en cuenta:** Se puede preguntar por varios tipos a la vez: `isinstance(5, (int, float))`.

**Ejemplo práctico:**

```python
caudal = 0.19
print(isinstance(caudal, float))
```

**Salida:**

```text
True
```

**Resultado esperado:** True

## 28. `help()`

**¿Para qué sirve?** Muestra documentación de una función, tipo u objeto. En Jupyter puede usarse para consultar cómo funciona.

**Sintaxis:** `help(objeto)`

**Parámetros y valor devuelto:** Recibe un objeto (sin paréntesis si es una función, como `len`). Imprime su documentación.

**Ten en cuenta:** En Jupyter también se puede escribir `len?` para ver la ayuda en un panel.

**Ejemplo práctico:**

```python
help(len)
```

**Salida:**

```text
Help on built-in function len in module builtins:

len(obj, /)
    Return the number of items in a container.
```

**Resultado esperado:** Muestra la ayuda y la descripción de len().

## 29. `dir()`

**¿Para qué sirve?** Devuelve una lista de nombres de atributos y métodos disponibles en un objeto o módulo.

**Sintaxis:** `dir(objeto)`

**Parámetros y valor devuelto:** Recibe un objeto y devuelve una lista de nombres. Sin argumentos, lista los nombres del entorno actual.

**Ten en cuenta:** Sirve para descubrir qué métodos tiene un texto, una lista, etc.

**Ejemplo práctico:**

```python
print("hola".upper())
print("upper" in dir("hola"))
```

**Salida:**

```text
HOLA
True
```

**Resultado esperado:** HOLA  
True

## 30. `open()`

**¿Para qué sirve?** Abre un archivo para leerlo o escribirlo. Conviene usar `with` para que el archivo se cierre automáticamente.

**Sintaxis:** `open(archivo, modo='r', encoding=None)`

**Parámetros y valor devuelto:** Recibe la ruta del archivo y el modo: `'r'` leer, `'w'` escribir (reemplaza el contenido), `'a'` agregar al final. Devuelve un objeto archivo.

**Ten en cuenta:** Este ejemplo crea un archivo `ejemplo.txt` en la carpeta del notebook. El repositorio lo ignora con `.gitignore`.

**Ejemplo práctico:**

```python
with open("ejemplo.txt", "w", encoding="utf-8") as archivo:
    archivo.write("Primera línea")

with open("ejemplo.txt", "r", encoding="utf-8") as archivo:
    print(archivo.read())
```

**Salida:**

```text
Primera línea
```

**Resultado esperado:** Primera línea

---
## Conclusión

Estas funciones permiten mostrar y convertir datos, medir colecciones, calcular valores, ordenar información, recorrer secuencias y trabajar con archivos sin instalar librerías adicionales. Practicar con ejemplos pequeños ayuda a entender su comportamiento y a reutilizarlas en programas más grandes.

**Fuente:** [Documentación oficial de Python: funciones incorporadas](https://docs.python.org/3/library/functions.html)
