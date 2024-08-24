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


