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
