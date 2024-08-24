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
2lenguaje de programación orientado a objetos"
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

### Classes en Python?
  Python es un lenguaje de programación orientado a objetos. 
Casi todo en Python es un objeto, que es una entidad con sus propiedades y métodos. 
  Entonces una clase es un constructor de objetos, o un modelo para crearlos, además nos permite definir las propiedades y métodos que tendrá cualquier 
  objeto creado a partir de dicha clase.
  También las clases son una manera de organizar el código y así facilitar su mantenimiento, además de aprovechar la reutilización del código: 
  si tenemos que crear varios objetos que tengan las mismas propiedades y métodos, no tenemos que repetir el código, en su lugar, podemos crear 
  nuevos objetos a partir de la misma clase.

### instancia de una clase
A diferencia de la clase, un objeto define una clase particular, con unos atributos particulares para ese objeto. Es decir, el objeto es la instancia de la clase. Se puede crear usando () sobre la clase y pasando los argumentos de entrada separados por ,.

'mi_clase = MiClase("Hola")'

### ¿Qué método se ejecuta automáticamente cuando se crea una instancia de una clase?
METODO __init__

  Al crear una instancia de una clase (instanciar) se crea el objeto en la memoria del sistema operativo, ya que hasta que no se ejecuta el programa, no se crea en memoria.
  Existe un método especial que se ejecuta cuando creamos una instancia de un objeto. Este método es __init__ que nos permite asignar atributos y realizar operaciones 
  con el objeto en el momento de su creación. 

###  verbos de API: Get, Post, Put y Delete.
- GET : este método permite obtener información del servidor.
- POST : permite enviar información, ya sea para agregar información a una base de datos
- PUT: actualizar información. Generalmente se utiliza para gestionar información en la base de datos.
- DELETE : este método se utiliza para eliminar información de la base de datos.

### MongoDB
MongoDB es un programa de gestión de bases de datos NoSQL (Not only SQL) de código abierto. 

### SQL VS NOSQL

- SQL significa Lenguaje de Consulta Estructurado, evolucionando desde la década de 1970 hasta convertirse en un poderoso lenguaje para consultar datos estructurados. son relacionales, es decir, sus datos están relacionados entre sí y se almacenan como texto de manera estructurada en tablas 

- NoSQL es un sistema de base de datos más nuevo que no utiliza un lenguaje de consulta estándar pero emplea documentos JSON para el almacenamiento de datos. aparecen debido a la necesidad de flexibilidad para almacenar distintos tipos de información no estructurada
como documentos (PDF, Word, Excel…), emails, SMS, localizaciones geográficas, audio, vídeo, publicaciones de RRSS… 

Ambos son dos tipos de bases de datos que permiten el almacenamiento y acceso ordenado a los datos, tanto estructurados (SQL) como no estructurados (NoSQL).

### API?
  Una API (interfaz de programación de aplicaciones), es un conjunto de reglas y protocolos que permiten que dos sistemas informáticos o aplicaciones interactúen entre sí, 
  por ejemplo para recuperar datos de un servidor web. 
  En esencia, una API actúa como una capa o interfaz de comunicación que permite que diferentes sistemas se comuniquen entre sí.
  Para que sirve:
    1-En el desarrollo, para ahorrar tiempo y dinero, al poder utilizar piezas o funciones que otros ya han creado. El ejemplo es una plataforma de compras online.
    2-También cuando se quiere utilizar deliberadamente las funciones de determinado servicio para ofrecer ventajas a sus usuarios.
      Por ejemplo, cuando vas a comprar y pones la información de tu tarjeta, la web utiliza una API para enviarle esa información de forma remota a otro programa 
      que verifica si tus datos son correctos o es una tarjeta inventada. Una vez se verifica, este programa remoto le dice a la web que todo está en orden, y esta ya te emite tu orden de compra.
    3-Otro ejemplo clásico es el de las aplicaciones de terceros para conectarse a un servicio. Por ejemplo, redes sociales como Twitter o Reddit 
      permiten que se creen aplicaciones diferentes a las oficiales para conectarse a ellas. Estas aplicaciones necesitarán las API de las redes sociales 
      para poder mostrarte la información y los mecanismos internos que las hacen funcionar.

  Una interface API es JSON (JAVASCRIPT OBJETS NOTATION), es un formato ligero de intercambio de datos. El cual es fácil para los humanos leer y escribir, 
  y es fácil para las máquinas analizar y generar.

### Postman

  Es una aplicación que permite conectar Python con APIs externas, que facilita a los desarrolladores crear, compartir, probar y documentar API. 
  En suma, es una herramienta para testear cualquier API-
  Nos permite enviar solicitudes con diferentes métodos HTTP (es decir, GET, POST, PUT y DELETE) y podemos comprobar la respuesta del servidor. 
  Con esta herramienta, podemos probar fácilmente nuestra API enviando una solicitud de cliente y verificando la respuesta HTTP. 

### polimorfismo

  Es uno de los pilares básicos en la programación orientada a objetos, y significa que objetos de diferentes clases pueden ser accedidos
  utilizando el mismo interfaz, mostrando un comportamiento distinto (tomando diferentes formas) según cómo sean accedidos. Esto significa 
  que podemos llamar a un método exactamente igual a otro y el interprete automáticamente detectará a cual de ellos nos referimos según diversos parámetros.

### método dunder
  «double underscore methods» También llamados métodos especiales, o mágicos. Son métodos de Python que definen cómo se comportan los objetos de Python cuando se realizan operaciones comunes sobre ellos.
  Normalmente no son invocados directamente por el programador. Por ejemplo cuando haces una simple suma 2 + 2 se está invocando al método __add__ internamente.
  Estos métodos se definen claramente con guiones bajos dobles antes y después del nombre del método.
  Los más comunes son __init__ y __repr__
- __init__ permite definir los atributos y comportamientos iniciales de un objeto al momento de su creación. es un método especial en Python que se utiliza para inicializar los objetos de una clase.

- __repr__ se utiliza para devolver una representación de cadena legible de un objeto. 
  Este método se define dentro de una clase y se llama cuando se usa la función repr() en un objeto de esa clase. 
  Se espera que el resultado sea una cadena que contenga información relevante sobre el objeto y sus valores de atributo.

### decorador de python
  Los decoradores son funciones que modifican el comportamiento de otras funciones, les añaden funcionalidades (las decoran).
  En otras palabras, una función la cual toma como input una función y a su vez retorna otra función.
  Son útiles para reducir las líneas de código duplicadas, hacer nuestro código más legible, fácil de testear, y de mantener.
