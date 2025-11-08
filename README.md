# 🧩 Resumen de conceptos: Fundamentos de programación

## 🧠 1. Conceptos Universales del Código

Estos conceptos son comunes a todos los lenguajes de programación.
Solo cambia la sintaxis, no la idea.

| **Concepto** | **Qué es** | **Ejemplo / Notas** |
|---------------|-------------|----------------------|
| **Palabras reservadas** | Palabras propias del lenguaje que tienen un significado fijo. No puedes usarlas como nombres. Algunas, como `if`, `else`, `for`, `while`, también forman parte de las **estructuras de control** (condicionales y bucles) que determinan el flujo del programa. | `if`, `for`, `def`, `class`, `with`, `return` |
| **Identificadores** | Nombres creados por el programador para variables, funciones o clases. | `nombre`, `guardarDatos`, `Usuario` |
| **Variables** | Espacios de memoria que guardan datos y tienen un nombre. | `x = 5` |
| **Datos** | Los valores que se almacenan. Pueden ser simples (`int`, `float`, `bool`, `string`) o estructurados (`list`, `array`, `object`). | `5`, `"Hola"`, `[1,2,3]` |
| **Expresiones** | Combinaciones de datos, variables y operadores que devuelven un resultado. | `x + 3`, `edad > 18` |
| **Sentencias / Instrucciones** | Líneas de código que ejecutan una acción. | `print("Hola")`, `x = 3` |


## ⚙️ 2. Funciones, Métodos, Clases y Objetos

Estos son los pilares de la programación estructurada y orientada a objetos.

| **Concepto** | **Qué es** | **Detalle** |
|---------------|-------------|--------------|
| **Función** | Bloque de código que realiza una tarea específica y puede reutilizarse. En los lenguajes de programación existen **funciones creadas por el usuario** y **funciones integradas (built-in)** que ya vienen con el lenguaje. | **Ejemplo (usuario):** `def saludar(): print("Hola!")` <br> **Ejemplo (integradas):** `print()`, `input()`, `sum()`, `len()` |
| **Método** | Una función que pertenece a un objeto o clase. | Se llama con punto: `objeto.metodo()`. |
| **Clase** | El molde que define cómo serán los objetos. Contiene atributos (datos) y métodos (comportamientos). | `class Persona:` |
| **Objeto** | Una instancia creada a partir de una clase. Representa algo concreto. | `p = Persona()` |
| **Atributo** | Una variable que pertenece a un objeto o clase. | `p.nombre = "Ana"` |
| **Método constructor** | Función especial que se ejecuta al crear un objeto y define sus propiedades iniciales. Se declara dentro de una clase con `constructor()`. | `class Persona { constructor(nombre) { this.nombre = nombre; } }` |




### 🔹 Regla clave (fundamental):
> * Una función fuera de una clase es una función.
> * Si esa misma función está dentro de una clase, se llama método.
>
> En otras palabras, un método es una función con “dueño” (la clase u objeto).

## 🧱 3. Módulos y Paquetes

A medida que los programas crecen, el código se organiza en partes.

| **Elemento** | **Qué es** | **Ejemplo** |
|---------------|-------------|--------------|
| **Módulo** | Un archivo `.py` que contiene funciones, clases o variables. | `import math` → `math.sqrt(9)` |
| **Paquete** | Una carpeta con varios módulos y un archivo `__init__.py`. | `from herramientas import calculos` |
| **Función de módulo** | Una función que pertenece a un módulo, no a un objeto. | `json.dump()` (función dentro del módulo `json`) |



### 💡 Ejemplo conceptual:

> ``` json.dump(contactos, archivo) ```
>
> * ```json``` es el módulo,
> * ```.dump()``` es una función dentro del módulo.

No pertenece al objeto contactos, sino al módulo json.

## ☕ 4. Lenguajes y Orientación a Objetos

| **Lenguaje** | **Paradigma** | **OOP** | **Observación** |
|---------------|----------------|----------|------------------|
| **Python** | Multi-paradigma | ✅ | Todo es un objeto, pero no estás obligado a usar clases. |
| **Java** | Orientado a objetos puro | ✅ | Todo debe estar dentro de clases. No existen funciones sueltas. |
| **JavaScript** | Multi-paradigma | ✅ | Usa prototipos (similares a clases). Puedes usar objetos o funciones libres. |


### 💡 Conclusión:

> Los tres lenguajes soportan la programación orientada a objetos,<br>
> pero solo Java la exige de forma estricta.<br>
> Python y JavaScript te permiten mezclar estilos (estructurado u orientado a objetos).

## 🧮 5. Listas y Arrays

Ambos sirven para guardar varios datos en una sola variable, pero se comportan distinto según el lenguaje.

| **Característica** | **Lista (Python)** | **Array (Java / JS)** |
|----------------------|--------------------|------------------------|
| **Tipos de datos** | Puede mezclar tipos (`[1, "a", True]`) | Generalmente homogéneos (aunque en JS puede mezclar) |
| **Tamaño** | Dinámico (puede crecer o reducirse) | Suele ser fijo (excepto en JS, que es dinámico) |
| **Nivel** | Alto nivel (flexible) | Bajo nivel (más control, menos flexibilidad) |


### 🔹 En términos prácticos:

> Una lista en Python es como un array sin restricciones.<br>
> Hace lo mismo (guardar elementos en orden y acceder por índice),<br>
> pero te da más libertad para modificarla o mezclar tipos.<br>
> 
> En JavaScript, los arrays se comportan casi igual que las listas de Python:<br>
> son dinámicos, flexibles y permiten combinar tipos de datos.

## 🔠 6. Concatenación

Concatenar significa unir secuencias de datos (como textos, listas o arrays) de forma lineal.

### 🔹 Fundamento

Concatenar = unir elementos uno detrás de otro.

```"Hola" + "Mundo" → "HolaMundo"```

### 🔹 Tipos comunes de concatenación

| **Estructura** | **Ejemplo** | **Resultado** |
|-----------------|--------------|----------------|
| **Strings** | `"Hola " + "mundo"` | `"Hola mundo"` |
| **Listas o Arrays** | `[1,2] + [3,4]` | `[1,2,3,4]` |


### 🔹 Restricciones

Solo puedes concatenar tipos compatibles.
No puedes unir un número con un texto directamente.

Ejemplo (Python):

```python
"Edad: " + 25   # ❌ Error
"Edad: " + str(25)  # ✅ “Edad: 25”
```

JavaScript y Java hacen la conversión automáticamente.

Python exige que tú la hagas con str().

### 🔹 Sobre la coma (,)

No concatena, solo separa argumentos.

|Código|	Qué hace|
|-------|------------
|```print("Hola" + "mundo")```|	Une y muestra “Holamundo”
|```print("Hola", "mundo")``` |	Muestra ambos con un espacio entre ellos, pero no los une

### 💬 En JavaScript pasa igual:

```javascript
console.log("Hola" + "mundo"); // concatena
console.log("Hola", "mundo");  // muestra separado
```
### 💡 Idea final:

> Un programador no solo escribe código:<br>
> entiende qué representa cada cosa y cómo se relaciona.<br>
>
> Variables, funciones, clases, objetos, listas o arrays son solo herramientas.<br>
> Lo importante es comprender qué problema resuelven y por qué existen.
