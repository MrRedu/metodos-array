# ¿Qué es un Array? 
Colección o **agrupación de elementos de cualquier tipo en una misma variable,** cada uno de ellos ubicado con referencia a la posición que ocupa dentro del mismo. <br>
### Creación:
```
const cars = ['🚗', '🚓', '🚕', '🚐', '🚛']
```
### Estructura:
Los elementos del Array, están posicionados por *index/índice,* esto quiere decir que el primer elemento, tiene la posición [0]
```
cars[0] // '🚗'
cars[1] // '🚓'
...
cars[4] // '🚛'
```

## Métodos funcionales de los Array

Irónicamente comenzaremos la lista de métodos funcionales, con una propiedad *(no es un método)*. <br>

Esta propiedad es `.length`: Nos muestra la cantidad de elementos que posee dicho array.
```
const frutas = ['🍎', '🍈', '🍓', '🍇', '🍉']
frutas.length // 5
```

Método `.toString()`: Transforma todos los elementos del Array en una cadena de texto *(string)*
```
const frutas = ['Manzana', 'Melón', 'Fresa', 'Mora', 'Sandía']
frutas.toString() // Manzana,Melón,Fresa,Mora,Sandía
```

Método `.join()`: Transforma todos los elementos del Array en una cadena de texto, pero con la característica que podemos definir el caracter que divida los elementos en dicho string.
```
const frutas = ['Manzana', 'Melón', 'Fresa', 'Mora', 'Sandía']
frutas.join(' + ') // Manzana + Melón + Fresa + Mora + Sandía
```

Método `.sort()`: Ordena el Array de forma ascendente.
Método `.reverse()`: Ordena el Array de forma descendente.
```
const letras = ['K', 'Z', 'Q', 'Y', 'L', 'B', 'A', 'C']
const numeros = [5, 428, 1, -5, 159.5, 42, 98]

letras.sort()       // ['A', 'B', 'C', 'K', 'L', 'Q', 'Y', 'Z']
numeros.sort()      // [-5, 1, 159.5, 42, 428, 5, 98]

letras.reverse()    // ['Z', 'Y', 'Q', 'L', 'K', 'C', 'B', 'A']
numeros.reverse()   // [98, 5, 428, 42, 159.5, 1, -5]
```
**** investigar el reverse()
