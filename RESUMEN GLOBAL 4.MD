# REACT



## DEFINICION
ReactJS es una de las librerías más populares de JavaScript para el desarrollo de aplicaciones móviles y web. 
Creada por Facebook, React contiene una colección de fragmentos de código JavaScript reutilizables utilizados para crear interfaces de usuario (UI) llamadas componentes

### VENTAJAS DE USO DE REACT
Una de las mayores ventajas de usar React es que puedes infundir código HTML con JavaScript.

- 1. Fácil de usar
Los desarrolladores con conocimientos de JavaScript pueden aprender a utilizar React en muy poco tiempo, ya que se basa en JavaScript plano y en un enfoque basado en componentes.

- 2. Admite componentes Java reutilizables
React te permite reutilizar componentes que han sido desarrollados en otras aplicaciones. Como React JS es de código abierto, es posible pre-construir componentes, lo que reduce el tiempo de desarrollo de aplicaciones web complejas.

- 3. Facilita la redacción de los componentes
Gracias a la integración de JSX, es más fácil escribir componentes de React: los usuarios pueden crear objetos de JavaScript combinados con tipografía y etiquetas HTML. JSX también simplifica la renderización de múltiples funciones, lo que mantiene el código sencillo sin reducir las capacidades de la aplicación.

- 4. Alto rendimiento
Como comentamos anteriormente, el virtual DOM permite a ReactJS actualizar el árbol del DOM de la forma más eficiente posible. Al almacenar el virtual DOM en la memoria, React elimina el exceso de re-renderización que puede perjudicar el rendimiento.


## JSX
JSX es una extensión de la sintaxis de JavaScript utilizada en la creación de elementos de React. Los desarrolladores la emplean para incrustar código HTML en objetos JavaScript.

## DOM VS VIRTUAL DOM
Modelo de Objetos del Documento (DOM) presenta una página web en una estructura de árbol de datos. 
ReactJS almacena árboles DOM virtuales en la memoria. 
Al hacerlo, React puede aplicar actualizaciones a partes específicas del árbol de datos, lo que es más rápido que volver a renderizar la totalidad del árbol DOM.

## Componentes y Props
ReactJS divide la interfaz de usuario en piezas aisladas y reutilizables de código conocidas como componentes. 
Los componentes de React funcionan de forma similar a las funciones de JavaScript, ya que aceptan entradas arbitrarias denominadas propiedades o props.

## Gestión de Estado
`La gestión de estado consiste en asegurar que la UI muestre correctamente el estado actual de la aplicación y es un pilar fundamental en frontend.`
Un estado es un objeto JavaScript que representa una parte de un componente. 
Cambia cada vez que un usuario interactúa con la aplicación, renderizando una nueva interfaz de cliente para reflejar las modificaciones.

La gestión de estados se refiere a la práctica de gestionar los estados de la aplicación React. 
Incluye el almacenamiento de datos en librerías de gestión de estados de terceros y la activación del proceso de re-renderización cada vez que los datos cambian.

Una librería de gestión de estados facilita la comunicación y el intercambio de datos entre los componentes. 
Actualmente existen varias librerías de gestión de estados de terceros, siendo Redux y Recoil las dos más populares.

## REDUX
Para para administrar el estado de una aplicación de forma predecible.

Redux actúa como un almacén centralizado que contiene y administra el estado de una aplicación o sus componentes. Esta centralización simplifica la gestión del estado, haciéndolo más organizado y accesible. funciona como la biblioteca oficial de enlaces de interfaz de usuario de Redux. Facilita la integración perfecta de React y Redux, lo que permite una experiencia de desarrollo más natural y eficiente.

Tres conceptos básicos de Redux

#### STORE : => Contiene el estado de la aplicación. Hay una tienda para toda la aplicación. => Las responsabilidades de la tienda Redux incluyen contener el estado de la aplicación, permitir el acceso al estado a través de getState(), habilitar actualizaciones de estado a través de dispatch(action)y registrar oyentes a través de subscribe(listener).

#### ACTION : => Las acciones son la única forma en que su aplicación puede interactuar con la tienda Redux. => Describen cambios en el estado. => Llevan información desde su aplicación a la tienda Redux en forma de objetos JavaScript simples. => Las acciones tienen una propiedad 'tipo' que indica el tipo de acción que se está realizando. => En Redux, un creador de acciones crea una acción, que es una función que devuelve la acción. Las acciones describen que algo pasó, pero no especifican cómo cambió el estado de la aplicación en respuesta. Esto es trabajo de los reducers.

#### REDUCER : => Los reducers son funciones que definen cómo debe cambiar el estado de la aplicación en respuesta a las acciones. 
Realiza transiciones de estado en función de acciones. => Los reductores especifican cómo cambia el estado de la aplicación en respuesta a las acciones enviadas a la tienda.
=> Un reductor es una función que acepta el estado actual y una acción como argumentos, y devuelve el siguiente estado de la aplicación.

### ROUTER

la librería estándar de React para el enrutamiento, proporciona múltiples formas de navegación programática segura entre componentes, sin necesidad de que el usuario haga clic en un enlace.

React Router es una colección de componentes para navegación, que puedes integrar en tus apps de React.

Con esta colección de componentes puedes modificar la URL de tu página web, reemplazar componentes dependiendo de la dirección en la que se encuentre el usuario y mucho más.


### diferencia entre enrutamiento estático y enrutamiento dinámico?

las rutas estáticas se declaran al iniciar la app, cuando se ejecuta por primera vez la aplicación, a partir de ahí, las rutas no pueden cambiarse en tiempo de ejecución.

Por otro lado, las rutas dinámicas pueden, efectivamente, cambiar durante la ejecución del programa, como su nombre lo indica, de manera dinámica.

###  React Native?

React Native es un framework JavaScript de código abierto construido sobre la librería React. Los desarrolladores lo utilizan para crear aplicaciones React multiplataforma para iOS y Android.

React Native utiliza interfaces de programación de aplicaciones (APIs) nativas para renderizar componentes de interfaces de usuario móvil en Objective-C (iOS) o Java (Android).

---
# CHECKPOINT 14

### módulo de nodo
 se instalac con: npm install [nombre-del-módulo].
Con este comando, se puede agregar cualquier módulo o biblioteca disponible en el registro de npm a un proyecto de Node.js.

NVM. Node Version Manager. es un administrador de versiones que le permite instalar y cambiar entre diferentes versiones de Node.js en una sola máquina.

NODE  es un entorno de ejecución usado para ejecutar código JavaScript en los servidores. Permite ejecutar JavaScript sin necesidad de un navegador web. 

### NPM
Node Package Manager 
Viene incluido con Node.js y se instala automáticamente. Maneja la instalación de paquetes, la gestión de versiones y la resolución de dependencias dentro de un proyecto node.js. NPM lee el archivo `package.json.
Asi con Node se permite que cientos de desarrolladores puedan compartir paquetes de software entre distintos proyectos.

npm se compone de al menos dos partes principales.

- Un repositorio online para publicar paquetes de software libre para ser utilizados en proyectos Node.js
- Una herramienta para la terminal (command line utility) para interactuar con dicho repositorio que te ayuda a la instalación de utilidades, manejo de dependencias y la publicación de paquetes.

`npm install` descargará el módulo desde el registro público de npm y lo colocará en la carpeta node_modules de nuestro proyecto.
Además, actualizará automáticamente el archivo package.json y el archivo package-lock.json con la nueva dependencia.

### dependencias. que son?

(son elementos para que una aplicación se ejecute), en desarrollo, son bibliotecas, módulos, o paquetes. En react, están dentro de la carpeta node_modules, y hay que llamarlas desde package.json, indicando nombre y versión. Se instalan después con npm install. Y en app.js hay que importarlas con “import moment from 'moment'”

### dos tipos de componentes de react

Componentes: Son como funciones, fragmentos de código independientes y reutilizables. Aceptan entradas (props), y devuelven elementos de react. Cada una tiene su propia lógica y su propósito es renderizar algo. se almacenan en src/components Dos tipos: FUNCIONALES, Y DE CLASE:

#### FUNCIONAL. son similares a las funciones de JavaScript que reciben propiedades (props) y devuelven elementos de React para su renderización. (un ReactNode puede ser un elemento html, un string, un booleano, entre otros tipos de datos.). Son las más simples y concretos, ya que solo reciben y retornan

#### DE CLASE. se crean utilizando clases de JavaScript, que extienden (amplian) la clase React.Component proporcionada por el propio React. son clases simples (compuestas por múltiples funciones que agregan funcionalidad a la aplicación). requiere que lo extiendas desde React. Componente y cree una función de renderizado que devuelva un elemento de React.

### PROPS

(son las propiedades de un componente) Es una manera de pasarle información dinámica a un componente, esto da dinamismo al sistema, ya que un mismo prop, puede dar lugar a diferentes resultados con diferentes instancias, y además da la posibilidad de reutilizar componentes También es una manera de pasar información entre componentes, de padre a hijo

### Con qué tipo de Componente utilizamos un Constructor?

CONSTRUCTOR: es un método utilizado para inicializar el estado de un objeto en una clase. 
Por lo tanto utilizamos el componente de tipo clase. 

Las utilidades del constructor son inicializar el estado local del componente asignando un objeto a this.state. Y para vincular eventos SUPER . 
no se puede acceder a este objeto.props directamente desde el principio, 
lo que puede provocar errores, entonces transferimos el valor de un accesorio a la función super() desde el constructor(). 
Cuando llamas a la función super(), se llama al constructor de la clase principal, que en el caso de React es React.Component. 

### SLUG
(o permalink) se usa como convenio para aquellas URLs que tienen partes customizadas, que podrían ser parámetros. En este caso, el slug sería el nombre del proyecto, la habilidad o la empresa.

---

# CHECKPOINT 15

## AXIOS 
es una biblioteca npm. es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos para que podamos representarlos en nuestra aplicación. 

Se instala con npm install axios. la agregará a nuestro archivo package.json y luego, luego agregará el código de Axios directamente a nuestro módulo de nodo.
```
AXIOS es una biblioteca npm que se utiliza para hacer solicitudes HTTP. es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos para que podamos representarlos en nuestra aplicación.
```
### AXIOS VS FETCH 

Axios es una librería externa, y Fetch es una herramienta nativa del navegador.

Entonces fetch no genera dependencias, esto es positivo para algunos proyectos, por el contrario Axios es más sencillo de configurar, por lo tanto, axios es el más utilizado. 
Axios maneja los resultados facilmente, y a través de catch capturamos los errores

###SOLICITUDES HTTP 

Las solicitudes HTTP son el mecanismo mediante el cual las aplicaciones web se comunican con los servidores. Pueden ser de diferentes tipos, como GET, POST, PUT y DELETE, 

### COOKIES en react
son archivos de texto con pequeños datos, como un nombre de usuario y contraseña, que se utilizan para identificar tu ordenador cuando utilizas una red.

### DEVELOPER TOOLS

Es una EXTENSION DEL NAVEGADOR. Se instala por ejemplo en chrome, yendo a chrome web store y buscar React Developer Tools o dar click aqui e instalarlas.

Da la capacidad de obtener una mejor visibilidad específica de React. Esto significa que puede ver los accesorios de su aplicación, su estado, puede ver los componentes además de que puede ver el árbol de componentes completo y puede inspeccionar todos sus datos.
```
SON UTILES PARA ver la estructura de componentes, examinar las propiedades (props) y el estado (state) de cada componente, y realizar un seguimiento de cómo se comunican entre sí. así como la para la identificación de errores, que sin estas herramientas, sería un proceso más complejo
```

### EVENT LISTENER
Es una función Sirve PARA realizar acciones en el programa a través de EVENTOS del usuario. Se asocian acciones a los eventos del usuario.

Al igual que los eventos DOM HTML, React puede realizar acciones basadas en eventos del usuario.

React tiene los mismos eventos que HTML: hacer clic, cambiar, pasar el mouse, etc.


No es específico de React sino que es general en programación web. Al igual que los eventos HTML DOM, React puede realizar acciones basadas en eventos del usuario. React tiene los mismos eventos que HTML: hacer clic, cambiar, pasar el mouse, etc.
`onClick`

### DEBUGGER

Este depurador nos permite ejecutar el código paso a paso, puesto que se detiene cada vez que se encuentra con la palabra clave debugger. Si clicamos en el botón de continuar, la ejecución del código continuará hasta que se encuentre con la siguiente palabra clave debugger.

### MIXINS
permite crear código CSS que se reutilizará en todo el sitio web. 
un mixin es una clase que contiene métodos que pueden ser utilizados por otras clases sin necesidad de heredar de ella. 
Los mixins son una forma de compartir comportamiento entre diferentes componentes de React. Son una forma de reutilización de código, un método para compartir funcionalidad entre varios componentes. POR EJEMPLO, para los estilos

### VARIABLES SASS

En React, a veces es posible que necesitemos actualizar dinámicamente el estilo debido a la interacción del usuario y al cambio en el DOM. En el caso de las variables SCSS, podemos actualizar dinámicamente las variables SCSS usando ReactJS.

Un gran uso de SASS es almacenar los distintos colores utilizados en su aplicación como variables. Luego se puede hacer referencia a estas variables en otros archivos .scss o, en este caso, directamente en sus componentes de React.

Por ejemplo, para crear una variable de color:
---
# CHECKPOINT 16

### ROUTER
Se usa porque REACT por si solo no permite el enrutamiento. Es un componente, y hay que agregarlo asi: npm i -D react-router-dom necesita una estructura de carpetas, y luego a través de una función.

En React, el contenido de la página es creado a partir de nuestros componentes. Así que lo que hace React Router es interceptar la petición que se envía al servidor
y luego inyectar el contenido dinámicamente desde los componentes que hemos creado.

### Qué es una solicitud POST?

en REACT lo estamos usando como metodo HTTP. Es lo opuesto a GET, este envia información, y no necesita THEN como Get se usa para ENVIAR datos a la API.

Es asíncrona, lo que significa que hay dos momentos cruciales en la ejecución: el momento en el que inicias la llamada y el momento en que recibes una respuesta (o un tiempo de espera).

En el módulo lo hemos usado para crear nuevos items en el portfolio

### HIGH ORDER COMPONENT

un componente de orden superior es una función que toma un componente y devuelve un nuevo componente. permiten reutilizar la lógica de los componentes en varios componentes.
En React, un componente de orden superior es una función que toma un componente como argumento y devuelve un nuevo componente que envuelve el componente original.

### SYNTHETIC EVENTS

En un sitio web HTML normal, tenemos lo que se llama DOM, es el Modelo de Objetos de Documento.

pero en React, tenemos lo que se llama DOM virtual, lo que significa que no estamos interactuando con el DOM como lo haría con un sitio web HTML normal, y eso es por razones de rendimiento.

no estamos trabajando con eventos reales, estamos trabajando con eventos sintéticos que están destinados a dar la misma sensación que trabajar con un evento normal,
ese es el comportamiento natural de React, tiene muchas funciones agradables y de alto rendimiento por las que React es realmente conocido, 
es una de las razones clave por las que la gente usa React.

### COOKIE VS TOKEN

HTTP no tiene estado. Cada solicitud es independiente y no contiene ningún contexto sobre las solicitudes anteriores. 
Entonces ¿cómo gestionamos las solicitudes que se realizan después de superar la autorización? Aquí es donde entran en juego las Cookies de Sesión y JWT (Json Web Token).

Ambas son herramientas para la AUTENTIFICACION DE USUARIOS. El proceso de autorización valida si dicho usuario o dispositivo tiene permisos para acceder a un recurso específico.

A diferencia de las cookies, los tokens de sesión no se almacenan en el dispositivo del usuario, sino en el servidor o en un servicio de terceros. 
El servidor genera un token único y aleatorio para cada usuario y lo envía al navegador como parte de la respuesta

---

# CHECKPOINT 17

### HANDLER
event handling: controladores de eventos. determinan qué acción ocurrirá cada vez que se active un evento. Esto podría ser un clic en un botón o un cambio en una entrada de texto. hacen posible que los usuarios interactúen con su aplicación React

### REFS Y DOM
sobre la manera en que REACT se relaciona con el DOM: react trabaja con un Dom virutal, 
pero hay veces que necesitamos interactuar directamente con el DOM y eso es lo que hacen los REFS lo hemos utilizado para poder borrar los archivos tan pronto como se hayan cargado exitosamente. 
es útil para trabajar con bibliotecas de terceros. para utilizar en casos que no podamos solucionar con props, state y funciones. 
permite acceder a los elementos del DOM o a los elementos react creados en el método render.

### CRUD

CRUD (Create, Read, Update, and Delete) para muchas aplicaciones, es el conjunto completo de funcionalidad, significa crear, leer, actualizar y eliminar. En REACT se puede aplicar para el manejo de datos en la API o localmente.

los métodos HTTP (POST, GET, PUT y DELETE) se corresponden a las operaciones CRUD CONJUNTO DE OPERACIONES DE CRUD que son las siguientes:

- Crear: crear una publicación o agregar la fila de la tabla, agregar datos a la página web o crear contenido. CREATEUSER POR EJEMPLO. EN HTTP POST
- Leer: leer o recuperar datos de una página web. EN HTTP GET
- Actualización: actualizar o editar contenido existente en la página web EN HTTP PUT
- Eliminar: eliminar y eliminar la entrada o contenido/publicación de la página web EN HTTP DELETE

