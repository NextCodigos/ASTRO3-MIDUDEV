---
title: 'Contenido de la pagina'
layout: '../../layouts/Layout.astro'
---

# Esto es un ejemplo de Javascript

## Subtitulo

```javascript
function(){
  console.log('Hola mundo')
}

```
```
JavaScript Example
javascript
function(){
  console.log('Hola mundo')
}

```

# Uso de var, let y const

## var y let se pueden declarar sin iniciar:

* var gato;
* let carro;
* console.log(gato); // Salida: undefined
* console.log(carro); // Salida: undefined

## var se puede redeclarar:

```
var gato = 'Felix';
console.log(gato); // Salida: Felix
var gato = 'Bobby';
console.log(gato); // Salida: Bobby
```

## let no se puede redeclarar:
```
let perro = 'Tobby';
// let perro = 'Bobby'; // Error de sintaxis: El identificador 'perro' ya ha sido declarado
console.log(perro); // Salida: Tobby
perro = 'Bobby';
console.log(perro); // Salida: Bobby
```
## const no se puede declarar sin iniciar:
```
// const direccion;
const direccion = 'avenida Paseos';
console.log(direccion); // Salida: avenida Paseos

const no se puede reasignar:

// direccion = 'avenida Principal'; // TypeError: Asignación a una variable constante.
```

## Alcance (scope):
```
var: es visible en la función donde se declaró o globalmente.
let y const: son visibles en el bloque donde se declararon o globalmente.
Reglas para nombrar variables
No se pueden usar palabras reservadas (function, var, for, while, etc.).
No pueden empezar con un dígito.
Pueden empezar con una letra, guión bajo o $.
Para nombres complejos se usa notación de camello.
Tipos de datos en JavaScript
number:
javascript
let velocidad = 98.5;
console.log(typeof velocidad); // Salida: number
```


## string:
```
let userName = 'Sergio';
console.log(typeof userName); // Salida: string

boolean:
javascript
let isActive = true;
console.log(typeof isActive); // Salida: boolean

array (matrices):
javascript
let carros = ['Ford Mustang', 'Toyota Corolla', 'Honda Accord'];
console.log(typeof carros); // Salida: object

object:
javascript
let carro = { modelo: 'Ford Mustang', potencia: 300, velocidad: 200 };
console.log(typeof carro); // Salida: object

undefined:
javascript
let nombre;
console.log(typeof nombre); // Salida: undefined

null:
javascript
let edad = null;
console.log(typeof edad); // Salida: object

Ejemplo de uso de reduce:
javascript
const array = [1, 2, 3, 4, 5];

const sum = array.reduce(function(a, b){
    return a + b;
}, 0);

console.log(sum); // Salida: 15
```


## Tipo de Datos en JavaScript*/
```
1 number -(2^53 − 1) and (2^53 − 1)*/

let velocidad = 98.5;
console.log(typeof velocidad);

//2 string

let userName = 'Sergio';
console.log(typeof userName);

//3 boolean

let isActive = true;
console.log(typeof isActive);

//undefined, una variable cuyo valor aun no ha sido definido

let nombre;
console.log(typeof nombre);

//null, el valor de nada 

let edad = null;
console.log(typeof edad);

//BigInt (numeros muy grandes)

let z = 3n ** 55n;
console.log(typeof z);


//Symbol--representa un identificador unico

let clave = Symbol('Sym');
console.log(typeof clave);

//4 array (matrices)

let carros = ['Ford Mustang', 500, true];
console.log(typeof (carros));

//5 object
let carro = { modelo: 'Ford Mustang', potencia: 300, velocidad: 200 };
console.log(typeof carro);

```


## Copiado por referencia
```
let x = [2, 4];

let y = x;

y.push(5);

console.log(x);
console.log(y);
```




//////////////////////////////////////////
//////////////////////////////////////////

```
const actualizador = setInterval(function(){

//Definimos el tiempo de inicio en milisegundos

const inicioClase = new Date('March 1, 2021 10:00:00').getTime();
console.log(inicioClase);

//Definimos el tiempo de ahora en milisegundos

const tiempoActual = new Date().getTime();
console.log(tiempoActual);

//Calculamos la diferencia entre el inicio y el tiempo actual;

let tiempoRestante = inicioClase - tiempoActual;
console.log(tiempoRestante);
//Convertimos los milisegundos en segundos 1s = 1000 ms;

tiempoRestante /=1000;
console.log(tiempoRestante);
//Calculamos los dias restantes

const dias = Math.floor(tiempoRestante/(60*60*24));
console.log(dias);

//Calculamos las horas restantes

const horas = Math.floor((tiempoRestante%(60*60*24))/(60*60));
console.log(horas);


//Calculamos los minutos restantes

const minutos = Math.floor((tiempoRestante%(60*60))/(60));
console.log(minutos);
//Calculamos los segundos restantes

const segundos = Math.floor(tiempoRestante%(60));
console.log(segundos);

const contador = document.getElementById('contador');


//Agregamos los elementos HTML con el valor del tiempo al contenedor con el id contador

contador.innerHTML = `
<div>
    <span>${dias}</span>
    <span class="texto">Dias</span>
</div> 
<div>
    <span>${horas}</span>
    <span class="texto">Horas</span>
</div>
<div>
    <span>${minutos}</span>
    <span class="texto">Minutos</span>
</div>
<div>
    <span>${segundos}</span>
    <span class="texto">Segundos</span>
</div>
`;
}, 1000);


console.log('test');

```

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FLUJO</title>
    <link rel="stylesheet" href="main.css">
</head>
<body>
    <header>
    <h1>RM Insurance Inc</h1>
   </header>
   
   <main>
        <section class="sec-1">
            <div class="container">
                <h1 id="tit" >Mejor Cuota en segundos</h1>
                <form action="">
                    <div>
                        <label for="genero">GENERO</label>
                        <select name="" id="genero">
                            <option value="hombre" >hombre</option>
                            <option value="mujer" >mujer</option>
                        </select> 
                    </div>           
                    <div>
                        <label for="edad">EDAD</label>
                        <input type="number" name="" id="edad" required>
                    </div>

                    <div>
                        <button type="button" onclick="generaCuota()">VER CUOTA</button> 
                    </div>
                 </form>  
                 <div id="cuota"></div>   
            </div>                           
        </section>

        <section class="sec-2">
            <img src="carro1.png" alt="carro">
        </section>
    </main>
    
    
    <script src="main.js"></script>
</body>
</html>

```


## Concepto #1 Truthy ---> Todos los valores son verdaderos al menos que se definan como falso ( excepto false, 0, "", null, undefined, y NaN */

```
// let x = 1;
// x = true;
// x = [];
// x ={};
// x = Infinity;
// x = 2n;
// x = NaN;
// x = 0;

/* Concepto #2 If else statement */

// if(x){
//     console.log('VERDADERO');
// }else{
//     console.log('FALSO');
// }

/* Concepto #3 Operador Ternario */
let edad = 16;
let trago = '';

// if(edad >=18){
//     trago = 'Cerveza';
// }else{
//     trago = 'Jugo de Manzana';
// }

// trago = (edad >=18) ? 'Cerveza' : 'Jugo de Manzana';
// console.log(trago);


/* Concepto #4 SWITCH*/

// let nivelDeSatisfaccion = 4;

// switch(nivelDeSatisfaccion){
//     case 1:
//         console.log('Muy Descontento');
//         break;
//     case 2:
//         console.log('No muy contento');
//         break;
//     case 3:
//         console.log('Contento');
//         break;
//     case 4:
//         console.log('Muy contento');
//         break;
//     default:
//         console.log('Muy descontento');
// }

/* Concepto #5 La expresion else if ...*/

const cat1A = 2500; //16-25 años, hombre
const cat1B = 2350; //16-25 años, mujer
const cat2A = 2000; // 26-39 años hombre
const cat2B = 1850; // 26-39 años mujer
const cat3A = 1500; // 40-85 años  hombre
const cat3B = 1250; // 40-85 pero menos de 86 años  mujer

const generaCuota = (genero, edad) => {
    
    //Declaramos las variables
    genero = document.getElementById('genero').value;
    edad = document.getElementById('edad').value;
    let msj = '';
    let precio = 0;

    //Chequeamos si se coloco el valor de la edad

    if(edad === ''){
        msj = 'Necesitamos su EDAD para generar una CUOTA';
    }

    //Generamos el mensaje para menores de 16 años

    else if(edad < 16){
        msj = 'Todavia no puede comprar seguro de auto';
    }
 

    //Generamos la cuota para mayores a 16 pero menores a 26;    
    
    else if((edad < 26) && (genero === 'hombre')){
        msj ='El precio de su poliza es: ';
        precio = cat1A;
    }else if((edad < 26) && (genero === 'mujer')){
        msj ='El precio de su poliza es: ';
        precio = cat1B;

    //Generamos la cuota para mayores de 25 pero menores a 40
    
    } else if((edad < 40) && (genero === 'hombre')){
        msj ='El precio de su poliza es: ';
        precio = cat2A;
    } else if((edad < 40) && (genero === 'mujer')){
        msj ='El precio de su poliza es: ';
        precio = cat2B;
    }
 
    //Generamos la cuota para mujeres y hombres entre 40 y 85 años
     else if(edad >=40 && edad <=85 && genero === 'hombre'){
         msj = 'El precio de su poliza es: ';
         precio = cat3A;
     }else if(edad >=40 && edad <=85 && genero === 'mujer'){
        msj = 'El precio de su poliza es: ';
        precio = cat3B;
    } 
  
    //Generamos el mensaje para el resto de los casos
    else {
        msj = 'Lo sentimos no tenemos poliza disponible';
    }
   
    
    //Declaramos la variable para tener acceso al div del mensaje

    const cuota = document.getElementById('cuota');

    //Mostramos el precio y el mensaje si es que el precio no es 0;
   
    if(precio !== 0){
        cuota.innerHTML = `
        <div>
            <span>${msj}</span>
            <span>${precio}</span>
        </div>
        `;
    } 
    //Mostramos solamente el mensaje cuando el precio es 0;
    else {
        cuota.innerHTML = `
        <div>
            <span>${msj}</span>
        </div>
        `;
    }
}

<style>

html{
    box-sizing: border-box;
    font-size: 62.5%;
}


*, *::before, *::after {
    box-sizing: inherit;
}
body{
    margin: 0;
    padding:0;
    background: url(fondo.png);
    /* overflow:hidden; */
}


header {
    min-height: 15vh;
    background-color: #3f3f3f; 
    display:flex;
    align-items:center;
    justify-content:center;   
}
h1{
    font-size: 3.5rem;
    color: #dfd7d7;
}

main{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction:row;
    flex-wrap: wrap;   
    width:80%;
    margin:auto;
    padding-top:100px; 
    color:#3f3f3f;
     
}





button{
    display: inline-block;
    width: 150px;
    height: 40px;
    border: none;
    border-radius: 5px;
    background-color: orange;
    color: #fff;
    font-size: 1.7rem;
    font-weight: bold;
    cursor: pointer;
    transition: 300ms;
}

button:focus{
    outline:none;
}
button:hover{
font-size: 1.8rem;

}

form div{
    margin-bottom:30px;
    font-size: 1.8rem;
    width:300px;
    text-align:left;
}

form input{
    width: 115px;
    height:25px;
    font-size: 1.8rem;
    border-color:orange;
    border-radius: 5px;
    border-width: 2px;
    text-align:center;
    border-style: solid;
    background-color: transparent;
}
form select{
    width: 90px;
    font-size: 1.8rem;
    border-color:orange;
    border-radius: 5px;
    background-color: transparent;
    border-width: 2px;

}

form input:focus, select:focus{
        outline:none;
    }


#cuota{
    font-size: 2rem;
    width:300px;
    text-align:left;    
    height: 130px;
    
}
#cuota div{
    background-color: #3f3f3f; 
    border-radius:5px;
    color: #dfd7d7;
    font-weight: 500;
    padding:10px;
}

img{
    width:400px;
    height:auto;
}

#tit{
    padding-top:50px;
    font-size:2.7rem;
    color:#3f3f3f;
    font-weight: 600;
}

</style>

```



## Funcion -->  instrucciones que realizan una tarea o calculan un valor*/
 
 * Declaracion de una funcion sin return
 ```
 function imprimeMensaje() {
    console.log('Hola soy una funcion!');
}

imprimeMensaje();

/*Declaracion de una funcion con return*/

function calculaPromedioDeTresNumeros(num1, num2, num3){
    let promedio = (num1 + num2 +num3)/3;
    //  return 'El promedio es: ' + promedio + ' dolares';
    return `El promedio es: ${promedio} dolares`;
   }
   console.log(calculaPromedioDeTresNumeros(35, 10, 9));
   


   /* Asignar la funcion a una variable */
const calcula = calculaPromedioDeTresNumeros;
console.log(calcula(45, 35, 62));
   
   /*Expresion de una funcion */
   // const calculaArea = function(ancho, alto) {
   //     const area = ancho * alto;
   //     return area;
   // }

   // console.log(calculaArea(25, 10));

       
   /*Funciones de tipo Flecha*/
       const calculaArea = (ancho, alto) =>{
           const area = ancho * alto;
           return area;
       }

       console.log(calculaArea(25, 10));
       
   /*Funciones flecha con un solo parametro y sola expresion */
       
       const multiplicaNumero = x => x ** 3;
       console.log(multiplicaNumero(10));
       
   /*Funcion como Parametro */
   
   const avisaUsuario = (fun, x) =>{
       alert(fun(x));
   }
   
   const saludaUsuario = (nombre = 'Amigo') => {
       return `Hola ${nombre}`;
   }
   
   avisaUsuario(saludaUsuario, 'Sergio');

   /*El concepto de hoisting


   Al ejecutar un fragmento de código, el motor de JavaScript crea el contexto de ejecución global.
   El contexto tiene 2 fases: creación y ejecución.

   Durante la fase de creación, el motor de JavaScript mueve las declaraciones de variable y función a la parte superior de su contexto (scope).

   En JavaScript  el hoisting funciona solamente con las declaraciones*/


console.log(aprendeLasFunciones(false));


```



## CICLOS IMPLEMENTADOS CON FOR 

```
// for (let i = 1; i <=4; i++) {
//     console.log(`iteracion ${i}`);
// }
// console.log('Fin del ciclo');


/*CICLOS AL REVES*/
// for (let i = 4; i >= 1; i--) {
//     console.log(`iteracion ${i}`);
// }
// console.log('Fin del ciclo');


/*CICLOS ANIDADOS*/
// for (let i = 1; i <= 4; i++) {
//     console.log(`Empieza iteracion ${i}`);
//     for (let j = 0; j < 4; j++) {
//         console.log(j);
//     }
// }
// console.log('Fin del ciclo');

/* WHILE*/

let x = 1;
while (x <= 4) {
    console.log(`Iteracion ${x}`);
    x++;
}
console.log('Fin de While');


/*DO WHILE*/

let y = 5;

do {
    console.log(`Iteracion ${y}`);
    y++;

} while (y <= 4);

const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];

// modifier = (array, element) => {
//     let newArray = [...array];
//     newArray.push(element);
//     return newArray;
// }


// console.log('la nueva');
// console.log(modifier(artists, "xxx"));

// console.log('vieja');
// console.log(artists);

let newArray = [... artists];
console.log(newArray);
newArray.push(5);
console.log(newArray);
console.log(artists);

```


## ARRAYS
```
const ejemploArray = [25, 'Ford Mustang', true, [1, 0]];

/*CAMBIAR ARRAYS*/

ejemploArray[1] = 'Charger';
console.log(ejemploArray);

// ejemploArray = [];


/* ACCEDER ELEMENTOS*/

// let x = ejemploArray[3][0];
// console.log(x);

/*RECORRER LOS ARRAYS*/

const carros = ['honda accord', 'ford mustang', 'toyota corolla', 'fiat 500'];


/* METODO #1 */

for (let i = 0; i < carros.length; i++) {
    console.log(carros[i]);
}

/*METODO 2*/

// for (let carro of carros) {
//     console.log(carro);
// }

/*METODO 3 forEach*/

// let cambiaLetra = (string) => {
//     let letraModificada = string.toUpperCase();
//     console.log (letraModificada);
// }

// carros.forEach(cambiaLetra);

carros.forEach ((carro) => {
     console.log(carro.toUpperCase());    
});




/*METODOS PRINCIPALES*/

/*pop() saca el ultimo elemento*/

console.log(carros.pop());

/* shift() saca el primer elemento*/
console.log(carros.shift());

/* push() agrega un elemento al final*/

carros.push('ford explorer');
console.log(carros);

/*unshift() agrega un elemento al principio de la matriz*/
carros.unshift('camaro');
console.log(carros);


/*splice() borra o agrega un elemento de acuerdo con el indice especificado*/

carros.splice(0, 0, 'ford focus');
console.log(carros);


```





## Variable para acceder el elemento input

```
const newPassword = document.getElementById('newPassword');
newPassword.addEventListener('keyup', checkPassword);
  
// Helper
function toggleClass(element, condition){
  if(condition){
    element.classList.add('valid');
  }else {
    element.classList.remove('valid');
    element.classList.add('invalid');
  }
}


//Funcion Principal
function checkPassword(){
// Condicion#1 La contraseña tiene 6 caracteres

const element1 = document.getElementById('length');
let isLengthValid = false;
if(newPassword.value.length > 5){
  isLengthValid = true;
}
toggleClass(element1, isLengthValid);

// Condicion#2 La contraseña tiene al menos un digito

const element2 = document.getElementById('digit');
let hasOneDigit = false;
let digitos = /[0-9]/;

if(newPassword.value.match(digitos)){
  hasOneDigit = true;
}
toggleClass(element2, hasOneDigit);

 
// Condicion#3 La primera letra es mayuscula
const element3 = document.getElementById('uppercase');
let isUpperCase = false;
let letras = /[A-Za-z]/;

if(newPassword.value.match(letras) && (newPassword.value.charAt(0)=== newPassword.value.charAt(0).toUpperCase())){
  isUpperCase = true;
}

toggleClass(element3, isUpperCase);


  // Condicion#4 Los primeros y los ultimos tres caracteres no se repiten
   const element4 = document.getElementById('pattern');
   let isPatternValid = false;

   if(newPassword.value.substr(0, 3) !== newPassword.value.substr(newPassword.value.length - 3)){
     isPatternValid = true;
   }

   toggleClass(element4, isPatternValid);


// Condicion#5 La contraseña no tiene espacios
const element5 = document.getElementById('space');
let hasNoSpace = false;

if(newPassword.value.replace(' ', '') === newPassword.value) {
  hasNoSpace = true;
}

toggleClass(element5, hasNoSpace);
 

// Condicion#6 La contraseña  tiene un caracter especial

const element6 = document.getElementById('character');
let hasSpecialCharacter = false;
let caracteres = /[!?@#&]/;

if(newPassword.value.match(caracteres)){
  hasSpecialCharacter = true;
}
toggleClass(element6, hasSpecialCharacter);

}

<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-BmbxuPwQa2lc/FVzBcNJ7UAyJxM6wuqIj61tLrc4wSX0szH/Ev+nYRRuWlolflfl" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.4.0/font/bootstrap-icons.css">
    <link rel="stylesheet" href="./main.css">

    <title>Strings</title>
  </head>
  <body class="bg-dark">
    <header class="bg-primary py-4 mb-5"></header>

    <form class=" mt-4 p-5 bg-light border" id="formulario">

        <h2 class= "text-secondary">Requisitos mínimos</h2>

        <ul id="mensaje">
            <li id="length">6 carácteres</li>
            <li id="digit">un dígito</li>
            <li id="uppercase">primera letra mayúscula</li>
            <li id="pattern">los primeros y los últimos 3 cáracteres no se pueden repetir</li>
            <li id="space">sin espacio</li>
            <li id="character">un cáracter especial (!?@# &amp;)</li>
        </ul>

        <div class="mb-4">    
            <input type="text" class="form-control" id="newPassword" placeholder="Contraseña">    
        </div>

 
 
        <div class="mb-4">
            <button type="button" class="btn btn-primary w-100 fs-5">Cambiar</button>
        </div>


        <div class="text-center">
            <a href="index.html">Regresar a la página anterior</a>
        </div> 


   
    </form>




    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta2/dist/js/bootstrap.bundle.min.js" integrity="sha384-b5kHyXgcpbZJO/tY9Ul7kGkf1S0CWuKcCD38l8YkeH8z8QjE0GmW1gYU5S9FOnJ0" crossorigin="anonymous"></script>

    <script src="main.js"></script>


  </body>
</html>

```



## Casi todo en JavaScript es un objeto (salvo los valores primitivos)

```
// Un objeto  es una coleccion de clave-valor
// edad:26
// id: 0001
```


## 1. Crear un objeto (Constructor)*/
```
// let carro = new Object();
// console.log(typeof(carro));

/*2. Evita crear objetos de tipo String, Boolean, Number */

let frase = new String('Objetos');
console.log(typeof(frase));
frase2 = 'Objetos';
frase === frase2 ? console.log('son iguales') : console.log('no lo son'); 

/*3. Crear un objeto con Object Literal(valores declarados literalmente en el codigo)*/

const car = {
    nombre: 'Ford',
    modelo: 'Mondeo',
    color: 'blanco',
    potencia: 0,
    produccion: 2014,
    

    /* Setter*/
    set cambiaPotencia(nuevaPotencia){
        if (typeof nuevaPotencia === 'number'){
          this.potencia = nuevaPotencia;
        } else {
          console.log('Potencia es un numero');
        }
      },
    
    /*Getters */
    get getPotencia() {
    if(this.potencia){
        return this.potencia;
    }else {
        return 'No tenemos informacion.';
    }
    },

    /*Metodos*/

    calculaAntiguedad() {
       let year = new Date().getFullYear();
       return  year - this.produccion;
    }


};

/*4 Acceder las propiedades un objeto */

console.log(car.nombre);
console.log(car['nombre'])

/*5 Cambiar los valores de las propiedades*/

 car.nombre = 'Fiat';
 console.log(car.nombre);

 console.log(car.calculaAntiguedad());

 /*6 Usando el setter y el getter*/

//  car.cambiaPotencia = 500;
 console.log(car.getPotencia);

 /*7 Destructured assignment */
// let x = car.color;
// console.log(x);
//  let {color} = car;
//  console.log(color);


 /*8 Factory Functions */

 const estudianteFactory = (nombre, edad) => {
    return { 
      nombre: nombre,
      edad: edad, 
      imprimeNombre() {
        console.log(nombre);
      } 
    }
  };

  const estudiante_01 = estudianteFactory('Jose', 25);
  console.log(typeof(estudiante_01));
  estudiante_01.imprimeNombre();


```

```


function cambiaColor(element){
  element.style.backgroundColor = 'red';
}


// #1 Metodo getElementById

// const seccion = document.getElementById('principal');
// cambiaColor(seccion);


// #2 Metodo getElementsByClassName

// const cajas = Array.from(document.getElementsByClassName('caja'));
// console.log(cajas);
// cajas.forEach(cambiaColor);


// #3 Metodo QuerySelectorAll
// const  cajas = document.querySelectorAll(' .caja');
// console.log(cajas);
// cajas.forEach(cambiaColor);


// #4 Metodo QuerySelector
const caja = document.querySelector('#body .titulo');
// console.log(caja);
cambiaColor(caja);

//Uso de parentElement

// let elementoBody = caja.parentElement.parentElement;
// cambiaColor(elementoBody);

//Uso del metodo closest()

// let seccion = caja.closest('#body');
// cambiaColor(seccion);


```





## #1 Cambios en el Estilo*/

## 1a) El atributo style*/

```
// const seccion = document.querySelector('#principal');
// seccion.style.border = '3px solid red';
// seccion.style.backgroundColor = '#f3f3f3';

/* 2b) el metodo setProperty()*/

// const primerDiv = seccion.firstElementChild;
// primerDiv.style.setProperty('background-color', 'red'); 

/* 3c) La propiedad classList*/

// primerDiv.classList.add('activado');
// primerDiv.classList.remove('activado');

// const toggleClass = () => {
//   primerDiv.classList.toggle('activado');
// }

/* #2 Cambios en el marcado*/

/* 2a) La Propiedad innerText*/

// primerDiv.innerText = 'cambio de Texto';


/* 2b) La propiedad innerHTML*/

// const valor = 251;

// primerDiv.innerHTML = 
// `<ul class="lista">
// <li>Precio: ${valor}</li>
// <li>Cantitad:</li>
// <li>Monto Total:</li>
// </ul>`;

/* #3 createElement(), appendChild(), removeChild() */

// const ultimoDiv = document.createElement('div');
 
// ultimoDiv.id = 'caja'; 
 
// ultimoDiv.innerHTML = 'Ultimo Div';
 
// seccion.appendChild(ultimoDiv);

// seccion.removeChild(ultimoDiv);

```


## EVENTOS EN JAVASCRIPT

```
/* Variables*/
const carro = document.querySelector('.carro');
const boton = document.querySelector('.boton');

/*handler Functions */

const achicar = () => {
  carro.style.transform = 'scale(0.6)';
};

const agrandar = () => {
  carro.style.transform = 'scale(1.2)';
};

const correr = () => {
  carro.style.left = '700px';
  achicar();
};

const retroceder = () => {
  carro.style.left = '0px';
  agrandar();
};
/* Agregar Eventos directamente al Elemento*/

// boton.onclick = achicar;
// carro.onmouseenter = achicar;
// carro.onmouseleave = agrandar;
/*metodo addEventListener*/

// boton.addEventListener("click", () => {
//   carro.style.left = "700px";
// });
// boton.addEventListener("mousedown", correr);
// boton.addEventListener("mouseup", retroceder);

document.addEventListener('keydown', correr);
document.addEventListener('keyup', retroceder);

/*Event Target (Todos los eventos en javaScript son objetos de tipo EVENT)*/

const cambiaColor = (event) => {
  event.target.style.backgroundColor = '#3f3f3f';
};

const seccion = document.querySelector('section');
seccion.addEventListener('mouseenter', cambiaColor);

seccion.removeEventListener('mousenter', cambiaColor);


```



/*********************************/
## CONCEPTO#1 ==> CODIGO SINCRONO
/********************************/
```
//Tradicionalmente, JavaScript es single-threaded (de un solo hilo)
//thread(hilo ) --> proceso que la aplicacion puede usar para completar tareas)
//En JavaScript sincrono, las tareas se ejecutan en secuencia (1, 2, 3, 4, etc.)

//Ejemplo de JavaScript sincrono

// let numeroFinal = 0;
// for (let i = 0; i < 500000000; i++) {
//   numeroFinal += 5;
// }

// console.log(numeroFinal);
// document.body.style.background = 'red';
// console.log('ultima tarea');

/*********************************/
/*CONCEPTO#2 ==> CODIGO ASINCRONO*/
/*********************************/

//JavaScript asincrono nos permite ejecutar tareas simultaneamente
//Hay tres tecnicas para implementar JavaScript asincrono:

//a)async callbacks
//b)promises
//c)async await

/***************************/
/*CONCEPTO#3 ==> CALLBACKS*/
/**************************/

//callbacks son funciones que se pasan como parametro adentro de otras funciones
//y se invocan adentro de la funcion principal para completar alguna tarea

//A) synchronous callbacks (se ejecutan inmediatamente y son bloqueadoras)

// const generaNumero = () => {
//   return Math.floor(Math.random() * 10);
// };

// const imprimeNumero = (callback) => {
//   let numero = callback();
//   console.log(numero);
// };

// imprimeNumero(generaNumero);

//B) asynchronous callbacks (se ejecutan cuando algo pasa)

// const bajaVideo = (url, callback) => {
//   console.log(`Bajando video de ... ${url} `);
//   setTimeout(() => {
//     console.log(`Video de ${url} descargado`);
//     callback(url);
//   }, 0);
// };

// const procesaVideo = (url) => {
//   console.log(`Procesando video de ${url}`);
// };

// let url = 'https://youtu.be/gisEHxRQIto';
// bajaVideo(url);
// procesaVideo(url);
// bajaVideo(url, procesaVideo);

/**************************/
/*CONCEPTO#4 ==> PROMISES*/
/*************************/

// 4.1 Promises son Objetos que representan el resultado eventual de una operacion asincrona

// El objeto PROMISE puede tener 3 estados:
// a) PENDING (pendiente) --> la promesa todavia no se cumplio
// b) RESOLVED (resuelta) --> la promesa se cumplio
// c) REJECTED (rechazada) ---> la promesa no se cumplio

//4.2 Construccion de una PROMESA
// let teHasPortadoBien = false;

// const siMePortoBien = new Promise((resolve, reject) => {
//   if (teHasPortadoBien) {
//     const telefono = {
//       modelo: 'iPhone12',
//       capacidad: '128GB',
//       color: 'rojo',
//     };
//     resolve(telefono);
//   } else {
//     reject('te has portado mal');
//   }
// });
//4.3 Uso (consumo) de PROMISES

//Antes de usar la promesa hay que definir dos funciones callback (handlers)
// success handler --> implementa la logica si es que la promesa se cumplio
// failure handler --> implementa la logica si es que la promesa no se cumplio

// const promesaCumplida = (resolvedValue) => {
//   console.log(`Te regalo tu nuevo ${resolvedValue.modelo}`);
// };
// const promesaRota = (rejectedValue) => {
//   console.log(`No te compro nada porque ${rejectedValue}`);
// };

// siMePortoBien.then(promesaCumplida, promesaRota);

// const pideRegalo = () => {
//   siMePortoBien.then(promesaCumplida).catch(promesaRota);
// };

// pideRegalo();
//4.4  CHAINING DE PROMISES

// const chequeaComportamiento = (comportamiento) => {
//   return new Promise((resolve, reject) => {
//     if (comportamiento) {
//       const telefono = {
//         modelo: 'iPhone12',
//         capacidad: '128GB',
//         color: 'rojo',
//       };
//       resolve(telefono);
//     } else {
//       reject('te has portado mal');
//     }
//   });
// };

// const grabaVideo = (telefono) => {
//   const mensaje = `Grabo video para TicToc con mi ${telefono.modelo} nuevo`;
//   return Promise.resolve(mensaje);
// };

// let comportamiento = true;
// chequeaComportamiento(comportamiento)
//   .then((resolvedValue) => {
//     return grabaVideo(resolvedValue);
//   })
//   .then((resolvedValue) => {
//     console.log(resolvedValue);
//   })
//   .catch((errorMensaje) => {
//     console.log(errorMensaje);
//   });
//4.5  PROMISE ALL
//A. Promise.all() toma como argumento un array de promesas y retorna UNA SOLA PROMESA
//B. si hay una promesa que no se cumple, Promise.all se rechaza con la razon especificada
//C. si todas las promesas se cumplen, Promise.all se resuelve con
//   un array que contiene los valores especificados en resolve de cada promesa
//D. Promise.all() se usa cuando el orden de las promesas no importa

const chequeaComportamiento = (comportamiento) => {
  return new Promise((resolve, reject) => {
    if (comportamiento) {
      const telefono = {
        modelo: 'iPhone12',
        capacidad: '128GB',
        color: 'rojo',
      };
      resolve(telefono);
    } else {
      reject('te has portado mal');
    }
  });
};

const chequeaCalificacion = (calificacion) => {
  return new Promise((resolve, reject) => {
    if (calificacion > 85) {
      resolve('Buen trabajo');
    } else {
      reject('Tienes que estudiar mejor');
    }
  });
};

// const mePorteBien = chequeaComportamiento(true);
// const estudieBien = chequeaCalificacion(90);
// const promesas = [mePorteBien, estudieBien];

// Promise.all(promesas)
//   .then((values) => {
//     console.log(values[0].modelo);
//   })
//   .catch((error) => {
//     console.log(error);
//   });
```

/****************************/
## CONCEPTO#5 ==> async await
/****************************/
```
//async await es azucar sintactico para trabajar mas facil con promises

async function pideTelefonoNuevo(comportamiento, calificacion) {
  try {
    const promesas = await Promise.all([
      chequeaComportamiento(comportamiento),
      chequeaCalificacion(calificacion),
    ]);
    console.log(promesas[0].modelo);
  } catch (error) {
    console.log(error);
  }
}

pideTelefonoNuevo(true, 75);


```

//////////////////////////////////////////

```
const carros = [
  {
    modelo: 'Ford Mustang',
    millaje: 25000,
    motor: 5.0,
    produccion: 2017,
    precio: 25000,
  },

  { modelo: 'Honda Accord', millaje: 10000, produccion: 2021, precio: 20000 },

  { modelo: 'Mini Cooper', millaje: 15000, produccion: 2005, precio: 5000 },
];

/* 1. Metodo Map*/

/*El metodo ejecuta una funcion para cada elemento del array creando un nuevo array con los resultados*/

// const modelos = carros.map((carro) => carro.modelo);
// console.log(modelos);

// const preciosEuro = carros.map((carro) => carro.precio * 0.85);
// console.log(preciosEuro);

//no se debe usar map en los siguientes casos:

//A.  no hace falta crear un nuevo array
//B. la callback no retorna nada

/* 2. Metodo Filter*/

//El metodo filter al igual que map
//crea un nuevo array colocando los elementos
//que pasan algun criterio

// const carrosNuevos = carros.filter(
//   (carro) => carro.produccion > 2010 && carro.millaje < 30000
// );

// console.log(carrosNuevos);

/* 3. Metodo Reduce*/

/*El metodo reduce ejecuta una funcion(reducer)
sobre cada elemento del array
devolviendo un solo valor*/

const num = [0, 1, 2, 3, 4];

// const suma = num.reduce((total, valorCorriente) => {
//   console.log(`Total: ${total}`);
//   console.log(`valorCorriente: ${valorCorriente}`);
//   return total + valorCorriente;
// }, 0);

// console.log(suma);

const funcionReductora = (millajeInicial, valorCorriente) =>
  millajeInicial + valorCorriente.millaje;

let x = carros.reduce(funcionReductora, 0);
console.log(x);

```


## 1) En una aplicacion WEB los datos JSON se reciben como una cadena
```
const cars = `[
   {
      "modelo": "ford mustang",
      "produccion": 2010,
      "millaje": 12000
  
   },
  
   {
      "modelo": "honda accord",
      "produccion": 2021,
      "millaje": 4560
   },
  
   {
      "modelo": "volkswagen Golf",
      "produccion": 2016,
      "millaje": 58200
   }
  
  ]
`;


   console.log(typeof cars);

   //2) Para convertir la cadena en un objeto JavaScript usa el metodo parse

   const jsonData = JSON.parse(cars);
   console.log(typeof jsonData);

   //3) Despues el objeto se puede manipular como cualquier otro objeto 

   const carrosNuevos = jsonData.filter(
  (carro) => carro.produccion > 2010 && carro.millaje < 30000
);

console.log(carrosNuevos);

//4) Para convertir los datos en una cadena usa el metodo stringify

const newCars = JSON.stringify(carrosNuevos);
console.log(typeof newCars);

//5 Modificar un archivo JSON (node)

const fs = require('fs');

//a) creamos un nuevo objeto
const carroNuevo = {
    modelo: 'Mini Cooper',
    produccion: 2022,
    millaje: 500
}


const newCar = JSON.stringify(carroNuevo);

fs.writeFile('cars.json', newCar, (error)=>{
   if(error) throw error;
   console.log('Informacion recibida');
});

```




## Informacion del REST COUNTRIES API
```
const url = 'https://restcountries.com/v2/name/';


//Variables para seleccionar los elementos de la pagina

const busqueda = document.querySelector('#input');
const envio = document.querySelector('#submit');
const respuesta = document.querySelector('#respuesta');



//Funcion para mostrar el resultado

const muestraResultados = (res) => {    
const capital = res[0].capital;
respuesta.innerHTML = `<p>${capital}</p>`;

}


//Funcion para async GET Request

const recibeInfo = async () => {

    const buscaPais = busqueda.value;
    const endpoint = `${url}${buscaPais}`;

    try {
        const response = await fetch(endpoint, {cache: 'no-cache'});
        if(response.ok){
            const jsonResponse = await response.json();

            //funcion para mostrar la informacion
            muestraResultados(jsonResponse);
        }

    } catch (error) {
        console.log(error);
    }
}

envio.addEventListener('click', recibeInfo);
```
//////////////////////////////////////////

```

const formulario = document.querySelector('#formulario');



/*Funcion para extraer todos los datos del formulario y convertirlos en formato JSON */

const procesaTodo = (event) => {
 /*Para una accion predeterminada del evento*/
 event.preventDefault();
 /*constructor que crea un objeto de tipo FormData */
const datos = new FormData(event.target);

 /* El método Object.fromEntries() transforma una lista de pares con [clave-valor] en un objeto.*/
const datosCompletos = Object.fromEntries(datos.entries());
console.log(JSON.stringify(datosCompletos));

}

```
```

/*Funcion Para Extraer un solo dato del formulario */

const procesaDatos = (event) => {
    /*Para una accion predeterminada del evento*/
    event.preventDefault();

    /*constructor que crea un objeto de tipo FormData */
    const datos = new FormData(event.target);

    /*El metodo get retorna el valor associado con la clave del objeto FormData */
    const correo = datos.get('email');   
    console.log({correo});

}

formulario.addEventListener('submit', procesaTodo);

```

//////////////////////////////////////////

<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <link rel="stylesheet" href="./main.css">
    <title>FetchAPI</title>
  </head>
  <body>
    

    <section class="container mt-4" style="max-width: 400px" id="contenedor-formulario">

      <div class="text-center text-white" id="titulo-formulario">      
        <h2 class="p-3">Contactos</h2>  
      </div>


      <form  id="formulario">
        <div class="mb-3">
          <input type="email" class="form-control" id="email"  name="email" placeholder="nombre@ejemplo.com">
        </div>

        <div class="mb-3">
          <input type="input" class="form-control" id="nombre" name ="nombre" placeholder="Adrian Mendoza">
        </div>


        <div class="mb-3">
          <input type="tel" class="form-control" id="tel" name="telefono" placeholder="Teléfono">
        </div>


        <div class="mb-3">
          <button id="btn" type="button" class=" btn btn-danger w-100 fs-5 mb-3">Enviar Mensaje</button>
        </div>
 
      </form>
   
     <div class ="text-light " id="respuesta"></div>
    

    </section> 
  
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
    <script src="./main.js"></script>


  </body>
</html>


```


const btn = document.querySelector('#btn');
const formulario = document.querySelector('#formulario');
const respuesta = document.querySelector('#respuesta');

/*Funcion para sacar los datos del Formulario con FormData (ve la leccion anterior)*/

const getData = () => {
  const datos = new FormData(formulario);
  const datosProcesados = Object.fromEntries(datos.entries());
  formulario.reset();
  return datosProcesados;
}



/*Funcion para colocar los datos en el Servidor */

const postData = async () => {
 
  /*Crea un objeto con la informacion del formulario*/
   const newUser = getData();

   try{
    const response = await fetch('http://localhost:3000/users', {
    /*especifica el metodo que se va a usar*/
    method: 'POST',
    /*especifica el tipo de informacion (JSON)*/
    headers: {'Content-Type': 'application/json'},
    /*coloca la informacion en el formato JSON */
    body: JSON.stringify(newUser)
    });
    

    if(response.ok){
        const jsonResponse = await response.json();

        /* Codigo a ejecutarse con la respuesta*/

        const {email, nombre, telefono} = jsonResponse;

        respuesta.innerHTML = 
        `<ul> 
           ¡Exito! Se guardó la siguiente información:
          <li>${email}</li> 
          <li>${nombre}</li> 
          <li>${telefono}</li>
        </ul>`
       
    }
   
   }catch(error){
     console.log(error);
   }
   
}




btn.addEventListener('click', (event) => {
  event.preventDefault();
  postData();
  
})


db.json
{
  "users": [
    {
      "email": "trt",
      "nombre": "tret",
      "telefono": "tretr",
      "id": 1
    },
    {
      "email": "",
      "nombre": "",
      "telefono": "",
      "id": 2
    }
  ]
}

```

## El Concepto de las Clases*/

## En JavaScript Las clases son una plantilla general para crear objetos.*/

```
let estudiante_01 = {
    name: 'Sergio',
    nivel: 2,
    carrera: 'programacion',
}


/*En Lugar de crear miles de objetos que representen diferentes estudiantes, uno podria definir una clase generica Estudiante */

/* Las clases son una HERRAMIENTA para crear objetos similares*/


/*#2 Declaracion de una clase */

class Estudiante {
    #llave;
    constructor(nombre, carrera) {
        this._nombre = nombre;
        this._carrera = carrera;
        this.#llave = 1230001;
    }
      generaID(){
        return Math.floor(Math.random()*10*this.#llave);
      }

    get nombre(){
        return this._nombre;
    }

    set nombre(valor) {
        this._nombre = valor;
    }
    
    
}

/*#3 Instanciar una clase*/

const estudiante01 = new Estudiante ('Sergio',  'programacion');
// console.log(estudiante01.generaID());
console.log(estudiante01.nombre);
console.log(estudiante01.nombre = 'Miguel');
const estudiante02 = new Estudiante ('Adrian', 'administracion de sistemas');




/*#4 Invocar los Metodos*/
// estudiante_01.name = 'Miguel';

// console.log(estudiante01.generaID());


/*#5 Herencia*/

/*Se puede crear una clase generica (superclass)*/
/* Y despues crear clases mas especificas(subclases)
que van a heredar las propiedades y los metodos*/

class EstudianteParcial extends Estudiante {
    constructor(nombre, carrera, tiempo) {
        super(nombre, carrera);
        this._tiempo = tiempo;
    }

    get tiempo (){
        return this._tiempo;
    }

 
    set tiempo (valor) {
         this._tiempo = valor;
    }
}

const estudiante03 = new EstudianteParcial('Miguel', 'medicina', 'parcial');


console.table(estudiante03);

/*Metodos Estaticos */

/*Metodos no disponibles en instancias de clases
se invocan directamente desde la clase principal */
console.log(estudiante01.generaID());


// estudiante_03.tiempo = 'parcial';
// console.log(estudiante_03.tiempo)


```





