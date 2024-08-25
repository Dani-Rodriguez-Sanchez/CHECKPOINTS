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
# CHECKPOINT 9

### paquete NPM?
npm es el gestor de paquetes de Node.js
Es un programa que se instala en tu computadora y que te permite tanto instalar paquetes de Node.js, como otros paquetes de terceros.
agrupacion de codigos que se usa para añadir funcionalidad adicional a la app, que se instala y se usa en javascript
Cada paquete incluye un archivo package.json que contiene informacion y dependencias

### gestión de errores
TRY Y CATCH

Aunque el código esté libre de errores, se pueden generar, ya que las aplicaciones de JS no son entidades independientes, por ejemplo puede haber problemas con los servidores.
Por esto es interesante configurar la gestión de errores, así avisaremos al usuario y a nosotros mismos, de que hay algo que no va bien.

try { Block of code to try } catch(err) { Block of code to handle errors }
Con try definirmo el bloque de código a probar, y con catch ejecutamos algo si ocurre el error.

### MOMENT JS

una biblioteca de javascript . sirve para poder trabajar con números y fechas.
Se instala a través de npm, en la seccion de dependencias de package.json. Y se puede configurar su formato, de manera que podemos crear strings con formatos personalizados, de año, mes, dia, etc. además de poder realizar cálculos a través de funciones en las que incluimos moment

se crea una variable = moment ('string con fecha', 'formato de fecha'); llamamos a la variable

### Lodash?
es una biblioteca de JavaScript 

Ayuda a trabajar con matrices, cadenas, objetos, números, etc.

en lugar de escribir funciones repetitivas, las tareas se pueden realizar con un solo línea de código

Proporciona varias funciones incorporadas para colecciones, matrices, para manipular objetos y otros métodos de utilidad que podemos usar directamente en lugar de escribirlos desde cero.

Se puede importar al código de varias maneras, a traves de consola, podemo importar toda la librería, o metodos especificos. También se puede incluir en el html, incluyendo una secuencia de comendos en el encabezado.

Ejemplo: la función Reduce. Que retorna el valor acumulado de una colección.
_.reduce(colección, iterado, acumulador)

---
# CHECKPOINT 10 GIT

### GIT 

Es un software de Control de Versiones, esto son los cambios que se producen sobre el código de un proyecto. Nos da herramientas para gestionar esas modificiones, hacer más fácil la administración de las distintas versiones de cada producto desarrollado. Nos permite organizar las modificaciones a través de ramas, lo que facilita la gestión de paquetes de gran tamaño. Lo iniciamos con git.init

### GITHUB 

Es una plataforma destinada a alojar el código de las aplicaciones de cualquier desarrollador, es propiedad de microsoft y es de código abierto, hay otras como Gitlab,y Bitbucket, Es repositorio, ya que el código de los proyectos que sean abiertos puede ser descargado y revisado por cualquier usuario. Además permite a los desarrolladores colaborar en proyectos en línea, al poderse realizar seguimiento de proyectos por varios usuarios.

### GITIGNORE 

Es una herramienta que se utiliza para especificar, mediante un archivo de texto se le dice a Git qué archivos o carpetas ignorar en un repositorio de un proyecto. Es útil, por motivos de seguridad, para evitar que archivos confidenciales o claves queden expuestos en los repositorios

---
# CHECKPOINT 11

### ramas de git
Las ramas le permiten trabajar en diferentes partes de un proyecto sin afectar la rama principal, es una bifurcación para crear un nuevo camino en la que probar una funcionalidad previamente a incluirla en el código principal.
Cuando se completa el trabajo, se puede fusionar una rama con el proyecto principal. Incluso puedes cambiar entre ramas y trabajar en diferentes proyectos sin que interfieran entre sí. permite crear nuevas ramas de un proyecto para probar ideas, aislar nuevas características, o experimentar sin impactar al proyecto principal.

### git init 
Crea un nuevo repositorio de Git. Puede utilizarse para convertir un proyecto existente y sin versión en un repositorio de Git, o para inicializar un nuevo repositorio vacío

### git branch
El comando git branch en Git permite enumerar, crear, cambiar el nombre y eliminar branch.
- git branch -d <branch> - elimina el branch indicado, evitando la eliminación si están presentes commit no fusionados
- git branch -D <branch> - elimina el branch indicado sin comprobar la presencia de commit no fusionados
- git branch -m <branch> - cambia el nombre del branch actual
- git branch -a - enumera branch remotos

### git checkout 
cambia entre ramas o restaura los archivos del árbol de trabajo (working tree)

### git pull
para obtener y descargar contenido de un repositorio remoto y actualizar inmediatamente la working copy del repositorio local para que coincida con ese contenido.

### git push 
se utiliza para cargar cambios locales en un repositorio remoto. De esta manera, los commit locales se ponen a disposición de otros colaboradores del proyecto, quienes pueden recuperarlos a través de una búsqueda e incorporarlos a sus respectivos repositorios locales.

### git fetch 
es descargar commit, ramas y etiquetas desde un repositorio remoto al repositorio local. 

### Git merge 
sirve para volver a unir una rama bifurcada

### Git commit
realiza una foto de los cambios hasta ese momento, a través de los commit, que son confirmaciones , como hitos dentro del proyecto. Estos commit se realizan en local(no interactuan en remoto hasta que se lo digamos)
*Identifica los cambios hechos en un entorno de trabajo. Luego con git push, los podemos trasladar al repositorio global o remoto.
Git commit -m (añadimos un mensaje con info sobre que se ha cambiado y por que).

### git merge conflict

surgen cuando dos personas cambian las mismas líneas en un archivo, o si un desarrollador elimina un archivo mientras otro lo modifica. Git marcará el archivo como en conflicto y detendrá el proceso de fusión

### comando para crear un repositorio git?
git add
se creará un nuevo subdirectorio .git en tu directorio de trabajo actual. También se creará una nueva rama principal.
Lo más lógico sería crear un directorio donde crearlo, con cd..., y estando ahí dentro git init

### DOM?
DOCUMENT OBJECT MODEL Modelo de Objetos de Documento ( DOM )
*es la representación de datos de los objetos que componen la estructura y el contenido de un documento en la web.

es una representación orientada a objetos de una página web, donde cada elemento de la página, como un botón, una imagen o un texto, se representa como un objeto con su propio conjunto de propiedades y métodos.
Se representa como un arbol de nodos.

* Nodo es un objeto que representa una parte del documento.

### detector de eventos
*es un “escuchador” para asignar una acción a un evento cuando se produzca
*los objetos que pueden lanzar eventos tienen el método addEventListener()
---
# CHECKPOINT 11

### ¿Por qué usamos ramas de git?
Las ramas le permiten trabajar en diferentes partes de un proyecto sin afectar la rama principal, 
es una bifurcación para crear un nuevo camino en la que probar una funcionalidad previamente a incluirla en el código principal.
Cuando se completa el trabajo, se puede fusionar una rama con el proyecto principal. 
Incluso puedes cambiar entre ramas y trabajar en diferentes proyectos sin que interfieran entre sí. 
permite crear nuevas ramas de un proyecto para probar ideas, aislar nuevas características, o experimentar sin impactar al proyecto principal.

Podemos ver las ramas con: 
git branch
Y creamos con:
git checkout -b (nombre)

### comando para crear un repositorio git?
git add
se creará un nuevo subdirectorio .git en tu directorio de trabajo actual. También se creará una nueva rama principal.
Lo más lógico sería crear un directorio donde crearlo, con cd..., y estando ahí dentro git init

### ¿Qué es un conflicto de fusión?
suceden cuando fusionas ramas que tienen confirmaciones de cambios contrapuestas, 
y Git necesita tu ayuda para decidir qué cambios incorporar en la fusión final.

### Git branch
muestra todas las ramas, y en que rama nos encontramos, con un asterisco al lado.
Puede servir para renombrar una rama

### Git push y git pull
git push sirve para empujar el commit, es decir, pasar de una rama local en el ordenador a un repositorio remoto. 
El comando es git add. Con git status vemos los 
Git pull es lo contrario: descargar las modificaciones en nuestro ordenador en local.

### Pull vs fetch. 
Git fetch copia los cambios al repositorio local, mientras que pull los copia directamente al directorio de trabajo. 
Es una unión de git merge y git fetch

### Git merge 
sirve para volver a unir una rama bifurcada

### git checkout
permite navegar entre ramas

### commit
realiza una foto de los cambios hasta ese momento, a través de los commit, que son confirmaciones , como hitos dentro del proyecto. Estos commit se realizan en local(no interactuan en remoto hasta que se lo digamos)
*Identifica los cambios hechos en un entorno de trabajo. Luego con git push, los podemos trasladar al repositorio global o remoto.
Git commit -m (añadimos un mensaje con info sobre que se ha cambiado y por que).

### selector de consultas?
*sirve para localizar elementos en el DOm
Es una herramienta para hacer consultas en el DOM

---
