# Uso de var, let y const

## Declaración de var y let sin inicializar:

```javascript
var gato;
let carro;
console.log(gato); // Salida: undefined
console.log(carro); // Salida: undefined
Redefinición de var:
javascript
￼Copy code
var gato = 'Felix';
console.log(gato); // Salida: Felix
var gato = 'Bobby';
console.log(gato); // Salida: Bobby
Imposibilidad de redefinir let:
javascript
￼Copy code
let perro = 'Tobby';
// let perro = 'Bobby'; // Error: El identificador 'perro' ya ha sido declarado
console.log(perro); // Salida: Tobby
perro = 'Bobby';
console.log(perro); // Salida: Bobby
No se puede declarar const sin inicializar:
javascript
￼Copy code
// const direccion;
const direccion = 'avenida Paseos';
console.log(direccion); // Salida: avenida Paseos
No se puede reasignar a const:
javascript
￼Copy code
// direccion = 'avenida Principal'; // TypeError: Asignación a una variable constante.
Alcance (scope):
var: es visible en la función donde se declaró o globalmente.
let y const: son visibles en el bloque donde se declararon o globalmente.
Reglas para nombrar variables:
No se pueden usar palabras reservadas (function, var, for, while, etc.).
No pueden empezar con un dígito.
Pueden empezar con una letra, guión bajo o $.
Para nombres complejos se usa notación de camello.
Tipos de datos en JavaScript:
number
string
boolean
array (matrices)
object
undefined
null
BigInt
Symbol
Ejemplo de uso de reduce:
javascript
￼Copy code
const array = [1, 2, 3, 4, 5];
const sum = array.reduce(function(a, b) {
    return a + b;
}, 0);
console.log(sum); // Salida: 15
Ejemplos de tipos de datos:
number:
javascript
￼Copy code
let velocidad = 98.5;
console.log(typeof velocidad); // Salida: number
string:
javascript
￼Copy code
let userName = 'Sergio';
console.log(typeof userName); // Salida: string
boolean:
javascript
￼Copy code
let isActive = true;
console.log(typeof isActive); // Salida: boolean
undefined:
javascript
￼Copy code
let nombre;
console.log(typeof nombre); // Salida: undefined
null:
javascript
￼Copy code
let edad = null;
console.log(typeof edad); // Salida: object
BigInt:
javascript
￼Copy code
let z = 3n ** 55n;
console.log(typeof z); // Salida: bigint
Symbol:
javascript
￼Copy code
let clave = Symbol('Sym');
console.log(typeof clave); // Salida: symbol
array (matrices):
javascript
￼Copy code
let carros = ['Ford Mustang', 500, true];
console.log(typeof carros); // Salida: object
object:
javascript
￼Copy code
let carroObj = { modelo: 'Ford Mustang', potencia: 300, velocidad: 200 };
console.log(typeof carroObj); // Salida: object
css
￼Copy code

Esta versión utiliza Markdown para organizar y resaltar diferentes partes del código, haciendo que sea más fácil de leer y entender.


