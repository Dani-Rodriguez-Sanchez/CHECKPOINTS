# REACT

# CHECKPOINT 14

## DEFINICION
ReactJS es una de las librerías más populares de JavaScript para el desarrollo de aplicaciones móviles y web. 
Creada por Facebook, React contiene una colección de fragmentos de código JavaScript reutilizables utilizados para crear interfaces de usuario (UI) llamadas componentes

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
Es una librería de gestión de estado.
El propósito de Redux es hacer predecibles los cambios de estado, imponiendo ciertas restricciones sobre como y cuando pueden producirse las actualizaciones. 
Redux consigue que tu gestión de estado sea transparente y determinista.

Los principios fundamentales de Redux:

- Fuente única de verdad: En Redux hay un único objeto que almacena el estado de toda la aplicación. Esto ayuda a la hora de trabajar con apps universales, así como a la hora de debugar y de reiniciar el desarrollo en un punto concreto de ejecución.
- Inmutabilidad, el estado es read-only. Ninguna interacción puede cambiarlo directamente. Lo único que puedes hacer para conseguirlo es emitir una acción que expresa su intención de cambiarlo.

- Funciones puras: Usa funciones puras (a mismos inputs, mismos outputs) para definir como cambia el estado en base a una acción. En Redux estas funciones se conocen como reducers y al ser puras, su comportamiento es predecible.

### REDUCERS


### ROUTER

la librería estándar de React para el enrutamiento, proporciona múltiples formas de navegación programática segura entre componentes, sin necesidad de que el usuario haga clic en un enlace.

