checkpoint7
Ejercicio práctico:

## Cree una función JS que acepte 4 argumentos. 

Suma los dos primeros argumentos, luego los dos segundos y multiplícalos. Si el número creado es mayor que 50, la consola registra "¡El número es mayor que 50!". Si es más pequeño, la consola registra "¡El número es menor que 50!"

function LimiteCincuenta(a, b, c, d){
	let suma1 = (a + b);
  
  let suma2 = (c + d);
  
  if((suma1*suma2)>=50){
    console.log("¡El número es mayor que 50!");
  }
  else{
    console.log("¡El número es menor que 50!");
  }
	}

LimiteCincuenta(1, 2, 3, 4)

## ¿Qué diferencia a Javascript de cualquier otro lenguaje de programación?
La principal diferencia es que se trata de un lenguaje INTERPRETADO,
esto quiere decir que los programas de JavaScript son archivos de texto que se integran directamente en las páginas HTML,
y son es interpretado directamente por un navegador.

Lo que esto significa es que puede escribir código JavaScript, simplemente abrirlo en el navegador, 
y ese navegador puede analizar el código, interpretarlo y luego ejecutar el programa. 
Además a partir de 2009, es compatible con todos los navegadores.

Esto frente a otros lenguajes como Java, que son COMPILADOS, los cuales necesitan un compilador, que si puede ser leído por los navegadores. 
Desde su creación en 1995, como complemento para el navegador netscape, su idea ha sido la de agregar fácilmente programas a la páginas web, 
aunque hoy en día su uso se ha extendido a otros ámbitos, como las bases de datos, con mongoDB y couchDB, además de Node.js, 
que proporciona un entorno para la programación fuera del navegador.

Otra diferencia es que JavaScript es gestionado por ECMAScript, una organización sin ánimo de lucro. 
En Java, el control lo tiene Oracle, una empresa privada que lo gestiona en función de sus intereses.

Y finalmente, JavaScript es débilmente tipado: una misma variable puede contener primero un texto, 
luego un número, un array o un objeto. Esto, que parece una ventaja, 
también es fuente de posibles errores si no controlamos correctamente lo que ocurre en nuestro código. 
Java, el contrario, es fuertemente tipado, el tipo de dato que se le puede asignar a una variable es mucho más estricto y, 
una vez definidas, no se pueden cambiar.

## ¿Cuáles son algunos tipos de datos JS?
Los tipos de datos son la naturaleza del contenido de una variable o constante, y son importantes porque sin ellos, 
una computadora no puede resolver esto de manera segura:

let x = 10 + "hola";

Primero, hay que distinguir cuales son los tipos primitivos y los objetos. Los primeros, son datos que no tienen métodos.

Y por otra parte, un tipo objeto es capaz de almacenar múltiples valores como propiedades.

### De acuerdo con el último estándar ECMAScript, existen nueve tipos de datos:

PRIMITIVOS:

Undefined. representa una variable que no ha sido declarada o a la cual no se le ha asignado un valor.

Boolean. representa un valor lógico y puede tener dos valores, true o false.

Number. Valores numéricos

String. Cadenas de caracteres

BigInt. Valroes numéricos demasiado grandes para poder ser representados por number

Symbol

TIPO OBJETO:

Null. Representa la ausencia de cualquier valor

Object. Colección de datos definidos

Function. Objetos con la capacidad de ser ejecutables

Algunos ejemplos:

// Numbers:
let length = 16;

// Strings:
let color = "Yellow";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"Daniel", lastName:"Rodriguez"};

// Function:

const bucle = (x) => {
  if (x >= 10) return;
  bucle(x + 1);
};
Podemos utilizar la función typeof, que nos devuelve el tipo de dato de la variable que le pasemos por parámetro.

console.log(typeof text); // "String"

## ¿Cuáles son las tres funciones de String en JS?
Son varios los métodos o funciones de String, pero voy a describir las más interesantes:

-charAt(index)

devuelve el carácter en un índice (posición) especificado en una cadena. Hay que tener en cuenta que el primer carácter es 0, y el último -1

let text = "HELLO WORLD";

let letter = text.charAt(2);

#L

-indexOf(carácter,desde)

Devuelve la posición de la primera vez que aparece el carácter indicado por parámetro en un string. Si no encuentra el carácter en el string devuelve -1. El segundo parámetro es opcional y sirve para indicar a partir de que posición se desea que empiece la búsqueda.

let text = "Hello world, welcome to the universe.";

document.getElementById("demo").innerHTML = text.indexOf("e");

#1


-replace(searchValue, replaceValue)

sirve para reemplazar porciones del texto de un string por otro texto, por ejemplo, podríamos utilizarlo para reemplazar todas las apariciones del substring "xxx" por "yyy". El método no reemplaza en el string, sino que devuelve un resultante de hacer ese reemplazo.

let originalString = "The color of the sky changes throughout the day.";

	let newString = originalString.replace("color", "colour");
	console.log(newString);
#"The colour of the sky changes throughout the day."

-toUpperCase()

convierte una cadena a letras mayúsculas. ToLowerCase() hace los mismo pero las convierte en minúsculas

let text = "Hello World!";
let result = text.toLowerCase();

#HELLO WORLD!

-toString()
se usa para convertir objetos en cadenas.

let text = "Hello World!";
let result = text.toString();

#Hello World!

## ¿Qué es un condicional?

Las condicionales te permiten tener un comportamiento dinámico en las aplicaciones, en las cuales a veces se hace necesario romper la secuencia lineal y crear ramas que nos permitan tomar diferentes caminos en el código dependiendo de ciertas condiciones.

El if...else es un tipo de instrucción condicional que ejecutará un bloque de código

cuando la condición de la instrucción if sea verdadera TRUE, y si la condición es falsa FALSE,

se ejecutará el bloque else.

if (true) {
console.log("Hola Mundo");
} else {
console.log("Adios Mundo");
}
En vez de utilizar true o false como condición, también podemos utilizar una expresión que evalúe la condición misma

if (1 == 1) {
  console.log("Hola Mundo");
}
-La sintaxis básica de if

(==) igual. devuelve TRUE si los operandos son iguales

(!=) no igual. Devuelve true si los operandos no son iguales.

(===)estrictamente igual. Devuelve true si los operandos son iguales y del mismo tipo.

(>=)mayor o igual. Devuelve true si el operando izquierdo es mayor o igual que el derecho.

Un ejemplo:

var num = 8;

if (num < 10) {
  console.log("El número es menor a 10");
} else {
  console.log("El número es igual o mayor a 10");
}
Estas condicionales pueden ser anidadas:

var num = 8;
if (num < 10) {
console.log("El número es menor a 10");
} else {
if (num > 10) {
console.log("El número es mayor a 10");
} else {
console.log("El número es igual a 10");
}
}
Aunque una alternativa al anidamiento es el (else if), que equivale a decir “de lo contrario que”

if (<primera condición>) {
// código que se ejecuta si <primera condición> se cumple
} else if (<segunda condición>) {
// código si <primera condición> NO se cumple, pero <segunda condición> se cumple
} else if (<tercera condición>) {
// código si <primera condición> y <segunda condición> NO se cumplen, pero <tercera condición> sí se cumple
} else {
// código si ninguna de las condiciones se cumple
}
## ¿Qué es un operador ternario?

El operador ternario una alternativa al condicional if/else de una forma mucho más compacta y breve, que en muchos casos resulta más legible.

Sin embargo, hay que tener cuidado, porque su sobreutilización puede ser contraproducente y producir un código más difícil de leer.

El operador condicional (ternario) es el único operador en JavaScript que tiene tres operandos.

condición ? expr1 : expr2

Como ejemplo, primero escribo la versión larga en la que vamos a mostrar un mensaje en pantalla diciendo si alguien aprueba o suspende un examen basándonos en su puntuación:

let puntacion = 5;
if (puntacion >= 6) {
alert('Aprobado');
}
else {
alert('suspenso');

y con la versión abreviada se vería así:

let puntacion = 5;
alert ( puntuacion >= 6 ? 'aprobado' : 'suspenso' );
¿Cuál es la diferencia entre una declaración de función y una expresión de función?\


Una función tiene la capacidad de recibir información y luego realiza todo tipo de procesos, para dar un resultado de salida.

Las funciones de JavaScript se definen con la functionpalabra clave.

Puede utilizar una declaración de función o una expresión de función .

\

Declaración de función:

function doStuff() {};

VS

Expresión de función:

const doStuff = function() {}

\

-Una declaración de función, declara una función con una palabra clave de función.

function dosParametros(paramA, paramB) {

// Conjunto de declaraciones

}

-una expresión de función es una función que se almacena dentro de una variable.

Pueden ser anónimas

var saludo = function () {

return ' Hola de nuevo ' ;

};

## ¿Qué es la palabra clave "this" en JS?
Es una palabra clave de JavaScript, que tiene una valor flexible, y se usa para representar o llamar al objeto que dicha función está modificando.

Hace referencia al objeto en cuestión cuando se encuentra dentro de una variable, y si se encuentra solo, se refiere al objeto global.

const ejemplo = {
color: azul,
func: function ( ) {
return this.color;
},
};

console.log (ejemplo.func());
#azul

This en funciones:

No puedes saber el valor que tendrá la variable "this" al ver el código de una función, porque depende de cómo te hayan invocado a esa función.

Si la función se ejecuta como global, "this" será el propio objeto global.
function miFuncion() {
  console.log(this);
}
miFuncion();
Si la función se ejecuta como método de un objeto, entonces "this" es el objeto que está recibiendo este método.

let miObjeto = {
  prop: 'valor',
  metodo: function() {
    console.log(this);
  }
}
miObjeto.metodo();
Por lo cual, el valor de "this" dentro de una función no depende de cómo se define esa función, sino de cómo se invoca.

\
