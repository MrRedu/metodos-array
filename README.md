# ¿Qué es un Array? 
Colección o **agrupación de elementos de cualquier tipo en una misma variable,** cada uno de ellos ubicado con referencia a la posición que ocupa dentro del mismo. <br>
### Creación:
```js
const carros = ['🚗', '🚓', '🚕', '🚐', '🚛']
```
### Estructura:
Los elementos del Array, están posicionados por *index/índice,* (a esto se le llama, *Indexación basada en cero/Indexación desde cero/Zero-based indexing*) esto quiere decir que el primer elemento, tiene la posición [0].
```js
carros[0] // '🚗'
carros[1] // '🚓'
...
carros[4] // '🚛'
```

## Métodos funcionales de los Array

Irónicamente comenzaremos la lista de métodos funcionales, con una propiedad *(no es un método)*. <br>

Esta propiedad es `.length`: Nos muestra la cantidad *(longitud del Array)* de elementos que posee dicho Array.
```js
const frutas = ['🍎', '🍈', '🍓', '🍇', '🍉']
frutas.length // 5
```

Método `.toString()`: Transforma todos los elementos del Array en una cadena de texto *(string).*
```js
const frutas = ['Manzana', 'Melón', 'Fresa', 'Mora', 'Sandía']
frutas.toString() // Manzana,Melón,Fresa,Mora,Sandía
```

Método `.join()`: Transforma todos los elementos del Array en una cadena de texto, pero con la característica que podemos definir el caracter que divida los elementos en dicho string.
```js
const frutas = ['Manzana', 'Melón', 'Fresa', 'Mora', 'Sandía']
frutas.join(' + ') // Manzana + Melón + Fresa + Mora + Sandía
```

Método `.sort()`: Ordena el Array (de manera ascendente en casos muy sencillos). El orden no es necesariamente [estable](https://en.wikipedia.org/wiki/Sorting_algorithm#Stability). El modo de ordenación por defecto responde a la posición del valor del string de acuerdo a su valor Unicode.
```js
const letras = ['D', 'H', 'F', 'G', 'E', 'B', 'A', 'C']
const numeros = [5, 428, 1, -5, 159.5, 42, 98]

letras.sort()       // ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']
numeros.sort()      // [-5, 1, 159.5, 42, 428, 5, 98]
```

Método `.reverse()`: Invierte el orden de un Array. *El primer elemento pasa a ser el último, el último pasa a ser el primero.*
```js
const arreglo = ['abc', 500, 'QWE', false]
arreglo.reverse() // [false, 'QWE', 500, 'abc']
```

Método `.concat()`: Permite juntar/concatenar dos Array.
```js
const frutas = ['Melón', 'Manzana', 'Sandía', 'Piña']
const fruits = ['🍈', '🍎', '🍉', '🍍']

frutas.concat(fruits)  // ['Melón', 'Manzana', 'Sandía', 'Piña', '🍈', '🍎', '🍉', '🍍']
```

Método `.push()`: Añade uno o más elementos al final del Array. Devolviendo la nueva longitud del Array.
```js
const colores = ['Amarillo', 'Magenta', 'Azul']
colores.push('Rosado', 'Rojo') // 5
```

Método `.pop()`: Elimina el último elemento del Array. Devolviendo el elemento que eliminó.
```js
const colores = ['Amarillo', 'Magenta', 'Azul']
colores.pop() // Azul
```

Método `.shift()`: Elimina el primer elemento del Array. Devolviendo el elemento que eliminó.
```js
const dias = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo']
dias.shift() // Lunes
```

Método `.unshift()`: Agrega uno o más elementos al inicio del Array. Devolviendo la nueva longitud del Array.
```js
const meses = ['Marzo', 'Abril', 'Mayo']
meses.unshift('Enero', 'Febrero') // 5
```

Método `.splice()`: Cambia el contenido de un Array eliminando (o no) elementos existentes y/o agregando nuevos elementos.
**Caso #1:**
```js
const personas = ['P1', 'P2', 'P3', 'P4', 'P5']
personas.splice(1, 2, 'P2-B', 'P3-B') // ['P1', 'P2-B', 'P3-B', 'P4', 'P5']
```
- Se entiende como: <br>

    A partir de la posición [1] *('P2')*,
    ```js
    personas.splice(1... 
    ```
    quiero reemplazar 2 elementos *('P2' y 'P3')*,
    ```js
    personas.splice(1, 2...
    ```
    por 'P2-B' y 'P3-B'
    ```js
    personas.splice(1, 2, 'PB-2', 'PB-3') // ['P1', 'P2-B', 'P3-B', 'P4', 'P5']
    ```
    
**Caso #2:**
```js
const personas = ['P1', 'P2', 'P3', 'P4', 'P5']
personas.splice(3, 0, 'P-KLJ', 'P-XIY') // ['P1', 'P2', 'P3', 'P-KLJ', 'P-XIY', 'P4', 'P5']
```
- Se entiende como: <br>

  A partir de la posición [3] *(P4)*,
  ```js
  personas.splice(3...
  ```
  quiero reemplazar 0 elementos,
  ```js
  personas.splice(3, 0...
  ```
  entonces añadiría `P-KLJ` y `P-XIY`
  ```js
  personas.splice(3, 0, 'P-KLJ', 'P-XIY') // ['P1', 'P2', 'P3', 'P-KLJ', 'P-XIY', 'P4', 'P5']
  ```

Método `.slice()`: Devuelve una copia de una parte del Array dentro de un nuevo Array empezando por inicio hasta fin (fin no incluido). *El array original no se modificará.*
```js
const letras = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I']
             //  0,   1,   2,   3,   4,   5,   6,   7,   8  <= Posiciones/índice de los elementos dentro del Array

// Si no especificamos el final
const resultadoLetrasDos = letras.slice(2) // ['C', 'D', 'E', 'F', 'G', 'H', 'I']

// Si especificamos el final
const resultadoLetrasTres = letras.slice(2, 5) // ['C', 'D', 'E']
```

Método `.includes()`: Comprueba si un valor específico está presente en el Array.
```js
const array = [1, 3, 5];
array.includes(2)      // false
array.includes(5)      // true
```

Método `.some()`: Comprueba si al menos uno de los elementos dentro del Array, cumple con la condición implementada por la función proporcionada.
```js
const array = [1, false, 5];
array.some((element) => element === false)        // true
array.some((element) => element > 25)             // false
```

Método `.find()`: Devuelve el valor del primer elemento del Array que cumple con la condición implementada por la función proporcionada.
```js
const array = [3, 8, 5];
array.find((element) => element > 1)                     // 3
array.find((element) => element > 4 && element < 7)      // 5
```




<br><br>
<br><br>
### 🚧 **¡En construción!** 🚧 . . . 👷🏻‍♀️🔨 . . .
