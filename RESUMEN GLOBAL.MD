# CHECKPOINT 1 GENERALIDADES CSS

###SCSS
es un preprocesador CSS

### SCSS vs CSS
CSS lo puede interpretar cualquier navegador, y SCSS tiene que ser procesado para que pueda ser convertido a CSS y ser leído

### variable SCSS
contiene código CSS, creado al inicio del proyecto. Se usa para acortar el código
$/ .elementos { background-color: $main-color; 

### SCSS Mixin
bloques de código reutilizables, dentro de ellos pueden contener variables, u otros mixins.
``` @mixin texto-resaltado{   font-size: 25px;   font-weight: bold;   border: 1px solid blue; }```

`.elemento{   @include texto-resaltado; }`

### Unidad fraccionaria (fr) 
significa que cada unidad se dividirá proporcionalmente al valor del (fr). Y es una opción al uso de tantos por ciento o de pixeles. Por ejemplo: .elementos { display: grid; grid-template-columns: 1fr 1fr 2fr; }  Significa que dentro del grid de tres elementos, los dos primeros son iguales en tamaño, y el tercero es el doble de cada uno de los anteriores

## CSS GRID VS CSS FLEXBOX
Flexbox se creó para diseños de una dimensión, en una fila o una columna. En cambio CSS Grid Layout se pensó para el diseño bidimensional, en varias filas y columnas al mismo tiempo.

---
# CHECKPOINT 2
### justify-content:
Sirve para controlar el alineamiento de los items en la caja flexbox a lo largo de su eje
principal.
- FLEX-START alinea los items de izquierda a derecha
- FLEX-END de igual manera pero de derecha a izquierda
- SPACE-BETWEEN alinea los items ordendamente a lo largo del eje
- SPACE-AROUND alinea los items de igual manera y con un espacio igual entre ellos

### flex-direction
Es para definir la dirección en la que se alinean los items
- ROW es el valor por defecto, y los alinea en filas, ordenándolos de izquierda a derecha
- ROW REVERSE igual, pero de derecha a izquierda
- COLUMN alinea los items en columnas de izquierda a derecha
- COLUMN REVERSE igual pero de derecha a izquierda

### diseño UX/UI
diferenciando entre experiencia de usuario, en la que se define la
estructura. E interface de usuario, en la cual se define un estilo y contenido adecuado al
producto.

---
# CHECKPOINT 3 PYTHON

## QUE ES
es un lenguaje de programación ampliamente utilizado en las aplicaciones web, el desarrollo de software etc.
los sitios web deben interactuar con las bases de datos, comunicarse con otros sitios web y proteger los datos cuando se los envía a través de la red. 
Python es útil para escribir código del lado del servidor debido a que ofrece muchas bibliotecas que constan de código preescrito para crear funciones de backend complejas

### Replit 
es una plataforma basada en la nube que actúa como un entorno de desarrollo integrado (IDE). A diferencia de muchos IDEs tradicionales que requieren instalación en tu máquina, Replit opera directamente desde tu navegador web. Ya sea que uses Chrome, Firefox o cualquier otro navegador, puedes acceder a tu código, proyectos y archivos con facilidad.

### 4 tipos de datos en Python
Los tipos básicos son: String, Number(int y float), List, y Boolean

### convención de nomenclatura debemos usar para las variables
Hay 3 reglas: 
1 -solo puede contener letras(mayúsculas y minúsculas), numeros, y guiones bajos(_) 
2 -solo puede comenzar con letra o guión bajo, núnca con números 
3 -Hay que evitar el uso de palabras reservadas, como True, False, def, else... *además son “case-sensitive”, con lo que por ejemplo diferencia entre Cadena y cadena

### comentarios en Python
Lo ideal es que el mismo código se explique a si mismo, mediante los nombres adecuados. No son útiles para explicar la funcionalidad, ya que esta puede cambiar, aunque si lo son para ayudar a comprender el diseño del código a otros programadores o nosotros mismos en el futuro. Además deben ser frases concisas, fáciles de entender, limitados en su número, y actualizados

### aplicaciones monolíticas y de microservicios

Las aplicaciones monoliticas funcionan desde un único código base, mientras que las basadas en microservicios, cada uno de ellos funciona para lograr una única característica. La implementación y el desarrollo de las monolíticas es más sencilla, aunque también es más complejo su mantenimiento. -En caso de surgir algún problema, las de microservicios limitarían el error al servicio concreto, mientras que el resto de la aplicación seguiría funcionando, siendo así también más rápido de Identificar. -Además las monolíticas son más rápidas, ya que los servicios no necesitan comunicarse *Por lo tanto, no hay una opción general más indicada que otra, si no que dependerá del tipo de proyecto elegir el sistema adecuado
---
# CHECKPOINT 4

### lista y una tupla
ambas son contenedores de datos en una variable, y su estructura es parecida, se diferencian en que las tuplas son inmutables, mientras que las listas si se pueden modificar. Además mientras que las listas se declaran con el símbolo corchete [], las tuplas se declaran con paréntesis ().

### orden operaciones  PEMDAS
Paréntesis, exponenetes, multiplicación, división, adición y sustracción

### diccionario Python
Es un método para almacenar en una variable datos clave-valor. 

### operador de asignación
Se utilizan para asignar valores a variables, puede ser desde el signo igual =, que es el más básico, y operadores aritméticos, , / , % , +, -
---
# CHECKPOINT 5

### condicional
Es una estructura de control, que  permite condicionar la ejecución de uno o varios bloques de sentencias al cumplimiento de una o varias condiciones.

### IF-ELSE
se utiliza para ejecutar tanto la parte verdadera como la falsa de la condición.

### diferentes tipos de bucles en python? ¿Por qué son útiles?

Un bucle es una estructura de control que repite un bloque de instrucciones, son útiles para automatizar la ejecución del código. 
Hay dos tipos: los bucles FOR y los bucles WHILE.

A grandes rasgos, se utilizan los primeros cuando sabemos de antemano cuantas veces se repetirá el programa, y el segundo cuando no lo conocemos.
- WHILE-permite ejecutar una sección de código repetidas veces, mientras una condición determinada se cumpla. Cuando se deje de cumplir, se saldrá del bucle y se continuará la ejecución normal. 
Por lo tanto el while tiene dos partes:
La condición que se tiene que cumplir para que se ejecute el código.
El bloque de código que se ejecutará mientras la condición se cumpla.

- FOR-Mientras que en el while la condición era evaluada en cada iteración para decidir si volver a ejecutar o no el código, en el for no existe tal condición, sino un iterable que define las veces que se ejecutará el código.
	for i in range(0, 4): 

### argumento en Python

Es una parte de las funciones, que tendrán un nombre, argumentos de entrada, un código a ejecutar, y unos parámetros de salida.
Estos argumentos pueden ser de nombre o de posición.

### función de Python Lambda

También se llaman funciones anónimas, porque se definen sin un nombre. 
Es una herramienta que permite recoger una función simple en una variable, y pasarla de forma muy sencilla a otras funciones. 
Su potencial radica en que la sintaxis condensada, que nos permite escribir funciones simples en tan solo una línea.
SINTAXIS:
lambda arguments : expression

### paquete pip

PIP es un programa de instalación de módulos externos de Python. 
Son librerías o bibliotecas de código, compartidas por otros programadores, en código abierto, y son útiles para ahorrar escribir mucho código, o simplemente realizar una tarea particular de la manera más sencilla. 

---
# CHECKPOINT 6
