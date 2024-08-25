# CHECKPOINT 7 JAVASCRIPT

### QUE ES
JavaScript es un lenguaje de programación o de secuencias de comandos que te permite implementar funciones complejas en páginas web, 
cada vez que una página web hace algo más que sentarse allí y mostrar información estática para que la veas, 
muestra oportunas actualizaciones de contenido, mapas interactivos, animación de Gráficos 2D/3D, 
desplazamiento de máquinas reproductoras de vídeo, etc., puedes apostar que probablemente JavaScript está involucrado. 
Es la tercera capa del pastel de las tecnologías web estándar, dos de las cuales (HTML y CSS) 

### Qué diferencia a Javascript de cualquier otro lenguaje de programación?
La principal diferencia es que se trata de un lenguaje INTERPRETADO, 
esto quiere decir que los programas de JavaScript son archivos de texto que se integran directamente en las páginas HTML, 
y son es interpretado directamente por un navegador.

Lo que esto significa es que puede escribir código JavaScript, simplemente abrirlo en el navegador, 
y ese navegador puede analizar el código, interpretarlo y luego ejecutar el programa. Además a partir de 2009, es compatible con todos los navegadores.

Esto frente a otros lenguajes como Java, que son COMPILADOS, los cuales necesitan un compilador, 
que si puede ser leído por los navegadores. Desde su creación en 1995, como complemento para el navegador netscape, 
su idea ha sido la de agregar fácilmente programas a la páginas web, aunque hoy en día su uso se ha extendido a otros ámbitos,
como las bases de datos, con mongoDB y couchDB, además de Node.js, que proporciona un entorno para la programación fuera del navegador.

Otra diferencia es que JavaScript es gestionado por ECMAScript, una organización sin ánimo de lucro. 
En Java, el control lo tiene Oracle, una empresa privada que lo gestiona en función de sus intereses.

Y finalmente, JavaScript es débilmente tipado: una misma variable puede contener primero un texto,
luego un número, un array o un objeto. Esto, que parece una ventaja, también es fuente de posibles errores
si no controlamos correctamente lo que ocurre en nuestro código. Java, el contrario, es fuertemente tipado,
el tipo de dato que se le puede asignar a una variable es mucho más estricto y, una vez definidas, no se pueden cambiar.

### tipos de datos JS?
son la naturaleza del contenido de una variable o constante
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

### tres funciones de String
El objeto String se utiliza para representar y manipular una secuencia de caracteres.

Las cadenas son útiles para almacenar datos que se pueden representar en forma de texto.
1- Crear cadenas
Las cadenas se pueden crear como primitivas, a partir de cadena literales o como objetos, usando el constructor String():

2- Acceder a un caracter
Hay dos formas de acceder a un caracter individual en una cadena. La primera es con el método charAt():

3- Comparar cadenas
En JavaScript, solo usas los operadores menor que y mayor que:

### condicional?
Las condicionales te permiten tener un comportamiento dinámico en las aplicaciones, 
en las cuales a veces se hace necesario romper la secuencia lineal 
y crear ramas que nos permitan tomar diferentes caminos en el código dependiendo de ciertas condiciones.

El if...else es un tipo de instrucción condicional que ejecutará un bloque de código

cuando la condición de la instrucción if sea verdadera TRUE, y si la condición es falsa FALSE,

se ejecutará el bloque else.

###  operador ternario?
El operador ternario una alternativa al condicional if/else de una forma mucho más compacta y breve, que en muchos casos resulta más legible.

Sin embargo, hay que tener cuidado, porque su sobreutilización puede ser contraproducente y producir un código más difícil de leer.

El operador condicional (ternario) es el único operador en JavaScript que tiene tres operandos.

condición ? expr1 : expr2

### palabra clave "this" en JS
Es una palabra clave de JavaScript, que tiene una valor flexible, y se usa para representar o llamar al objeto que dicha función está modificando.

Hace referencia al objeto en cuestión cuando se encuentra dentro de una variable, y si se encuentra solo, se refiere al objeto global.

const ejemplo = { color: azul, func: function ( ) { return this.color; }, };

console.log (ejemplo.func()); #azul

This en funciones:

No puedes saber el valor que tendrá la variable "this" al ver el código de una función, porque depende de cómo te hayan invocado a esa función.

---

# CHECKPOINT 8

### tipo de bucles hay en JS

Los bucles son útiles para repetir un mismo código varias veces, como por ejemplo iterar los elementos de una lista.

Los tipos de bucles que hay son FOR y WHILE.

- FOR.
Crea un bucle con una duración definida por sus expresiones.

Sintaxis básica:

for (begin; condition; step) { 
  // ... elemento a ejecutar...
}

- WHILE Y DO/WHILE
Tiene un funcionamiento diferente, ya que recorre un código mientras que una condición sea verdadera (true). Do while hace lo mismo, pero el código se ejecuta al menos una vez antes de la condición.
Sintaxis básica:

while (condition) {
  // code block to be executed
}

### diferencias entre const, let y var?
Las tres se usan para la declaración de variables, aunque tienen alguna diferencia.

- VAR eras las más usadas antes de la llegada de ES6. Las variables creadas con var se pueden volver a declarar y modificar. Tiene ámbito global cuando se declara fuera de la función, y local cuando está situada dentro.

var x = 10;

- LET es la preferible para la declaración de variables. Su alcance es sólo dentro del bloque de la función, dentro de los {}, significa que no estará disponible fuera de él. A diferencia de VAR, puede modificarse pero no volver a declararse, es decir, no puedes declarar la misma variable varias veces.
let x = 10; 

- CONST 
tiene similitudes con LET, pero no puede modificarse ni volver a declararse. Aunque no es inmutable, ya que si declaras un objeto o array con Cont, puedes modificar sus propiedades.

const cars = ["Saab", "Volvo", "BMW"];

###  función de flecha

Es una forma de definir una función. es una manera de simplificar código, dando lugar a una sintaxis más sencilla y fácil de leer, que en el caso de funciones simples puede ser definida en una sola línea. De hecho se prescinde de return, incluso se puede no incluir las {}.
Puede aceptar ningún argumento, uno, o varios. Además de la palabra THIS, con la peculiaridad de que en este caso, this, hereda las condiciones del ámbito principal, mientras que en una función normal variaría dependiendo donde se escriba la función.

### la deconstrucción variable

La deconstrucción de variables es una técnica que permite extraer limpiamente valores de un array y asignarlos a nuevas variables. Consigue que el código sea menos repetitivo, y cumplir el principio de programación DRY (don´t repeat yourself)

Entonces podríamos hacer algo así, donde se asigna en orden los dos elementos del array perfil, accedemos a ellos, y los asignamos a nuevas variables con nombres independientes.

### operador de spread JS?

Es un operador nos permite copiar rápidamente todo o parte de una array u objeto existente en otra array u objeto. Su sintaxis será tres puntos seguidos de algún tipo de palabra (...word)

Su utilidad es poder distribuir los elementos de un iterable (cadena de texto, array) dentro de uno nuevo.

En este ejemplo, se combinan los elementos de una array, dentro de otra nueva a través de la definición de la nueva incluyendo ...delante del nombre de la emisora.

let frutas = ['Manzana', 'Pera', 'Platano'];

### OOP?
Object Oriented Programming

Es un estilo o paradigma de programación basado en clases y objetos. Estos últimos agrupan datos (propiedades) y métodos (acciones) dentro de sí mismo. Por ser un paradigma, dependiendo del tipo de proyecto, tendremos que elegir entre utilizar una programación basada en funciones (recomendable para códigos pequeños), y otra orientada a objetos, con clases y métodos (en los proyectos que requieren una arquitectura más sólida y mantenible en el tiempo).

La clase es como una representación de un conjunto, la instancia de una clase es lo que realmente tiene el código propio. En este sentido, podemos tener varias instancias de una sola clase, como podemos tener copias únicas de una sola versión original.

Un objeto también se llama instancia de clase, ya que se crea mediante la instanciación, que consiste en crear un nuevo objeto a partir de una plantilla o molde predefinido. Esto se realiza por dos métodos, ESTÁTICO, y de INSTANCIA, se diferencian en cómo se accede a ellos y cómo se utilizan.

### promesa JS
Como concepto, es algo que, en principio pensamos que se cumplirá, pero queremos anticiparnos, y crear ciertos escenarios: se cumple, no se cumple, o queda en un estado pendiente.

Debido a la naturaleza asíncrona de JS, que en resumen significa que las instrucciones no son necesariamente ejecutadas una después de otra. Entonces, cuando nos comunicamos con una API externa, puede suceder que necesitemos que una tarea se ejecute antes que otra.
Por ejemplo, podemos necesitar que Twitter nos muestre unos elementos primero, y decidir que otros pueden tardar mas en caso que tarden más tiempo en cargar.

En JS, una promesa es un objeto que representa la finalización o falla de una tarea asíncrona y su valor resultante.

### Qué hacen async y await por nosotros?
Es una sintaxis especial para trabajar con promesas de una forma más confortable y fácil de escribir.

ASYNC hace que una función devuelva una Promesa, y AWAIT hace que la función suspenda la ejecución, y espere una promesa resuelta antes de continuar, sólo se puede usar dentro de la función async.

Por la naturaleza asíncrona de JS, necesitamos considerar el orden en el que se devuelven las funciones, ya que de no ser así lo que sucediese más rápido sería el que regresase primero, y esto puede no ser lo que necesitemos,y nos encontraríamos con un error. Entonces por ese motivo necesitamos la función async y await, para definir el orden en el que se llaman y devuelven las funciones.

Son una evolución de las funciones CALLBACK, las cuales se pasan como argumento a otra función y se ejecutan después de que se haya completado alguna operación. Pero su uso excesivo puede generar código complejo, y por ello ASYNC/AWAIT, es una alternativa más moderna para simplificar esta programación.

---
