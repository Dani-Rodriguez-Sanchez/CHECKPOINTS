# CHECKPOINT 18

### SCROLL INFINITO

- A nivel de usuario: Es un diseño que permite a los usuarios seguir viendo la información sin pausa, 
de manera que esta se va recargando mientras estos se desplazan hacia abajo. Es alternativa a la PAGINACION.

- A nivel de programación: es una función que carga un determinado número de elementos, 
y al llegar al final de la página carga y muestra más elementos. Se hace para evitar que la página se cargue excesivamente y se ralentice. 
Entonces se agrega un CONTROLADOR DE DESPLAZAMIENTO, a traves de un event listener

### Spinner de carga
Es un pequeño ícono que gira a medida que ingresan tus datos, gira y eso te indica que la aplicación está funcionando.

Util cuando se trata de una función de desplazamiento infinito,

### modal?
Es un cuadro de diálogo interectivo, que se superpone al contenido principal de la página. Se instala como una librería externa

sirve para:

- Introducir los datos de un formulario
- Introducir datos para un inicio de sesión
- Aceptación de los terminos legales del servicio
- confirmar una acción (eliminar un elemento de un blog)
- Se abren con un event listener, y se cierran con otro (clicando fuera o esc) o cuando termina su función

### Formularios. diferencia de comportamiento con html
un formulario permite que un usuario introduzca datos que luego serán enviados a nuestro servidor para ser procesados.
Los formularios en React son un tipo de elemento en esta librería de JavaScript que proviene del código HTML.
Aun así, los formularios en React son un poco diferentes.

en REACT en vez de esperar a que el formulario sea enviado y luego reunir la información, creamos un estado y,
a cada tecla presionada, click en un checkbox etc.. actualizamos el estado, por lo que siempre estamos "escuchando" 
a los cambios en los inputs del formulario y, cuando finalmente se envía el formulario, 
no tenemos que reunir ninguna información, eso ya está hecho a través de la actualización dinámica del estado.
a través de los hooks, podemos ir actualizando el valor del usuario, con funciones actualizadoras

### estados de vida

los componentes poseen algo conocido como el ciclo de vida. Este ciclo de vida son una serie de funciones que se ejecutan en distintos momentos de la vida del componente y nos permiten realizar distintas acciones en estos momentos. El ciclo de vida se puede dividir en 3 fases, el montado, actualización y desmontado del componente. Estas fases a su vez se dividen en varios métodos que puede tener el componente.

a — Montaje Cuando se crea una instancia de un componente y se inserta en el DOM

b — Actualización Cuando sufre algún cambio las propiedades (props) o el estado (state) del componente.

c — Desmontaje Cuando el componente se elimina del DOM.

### MODAL
Modal es un elemento UX común. Un modal es un cuadro de diálogo/ventana emergente que se muestra en la parte superior de la página actual.

Un modal en React es un componente que se superpone a otro contenido en una página web. Es un elemento de la interfaz de usuario que se utiliza para mostrar contenido adicional o para solicitar la interacción del usuario. Los modales de React se utilizan habitualmente para mostrar formularios, mensajes u otro contenido interactivo.


---
# CHECKPOINT 19

### BINDING
Es una peculiaridad de los componentes de clase en React.

En componentes de clase, el valor que adopta this dentro de una función dependerá de cómo sea invocada dicha función. 

Cuando nuestra función es utilizada como manejador de eventos (event handler), el valor al que apunta this será undefined. ¿Por qué? Las declaraciones y expresiones de clase (como por ejemplo nuestra función) se ejecutan en modo estricto, bajo el cual se aplica el binding por defecto a undefined y no a la instancia del componente como cabría esperar. Por tanto, el this en un event handler disparado fuera de nuestro componente de clase, perderá la referencia a la instancia a la que pertenece.

La solución pasa por “atar” manualmente el this a la instancia de clase en cada una de las funciones declaradas como métodos de clase.
asegurarte que las funciones tengan acceso a los atributos del componente como this.props y this.state

this.handleClick = this.handleClick.bind(this);

### MODAL

Modal es un elemento UX común. Un modal es un cuadro de diálogo/ventana emergente que se muestra en la parte superior de la página actual.

Un modal en React es un componente que se superpone a otro contenido en una página web. Es un elemento de la interfaz de usuario que se utiliza para mostrar contenido adicional o para solicitar la interacción del usuario. Los modales de React se utilizan habitualmente para mostrar formularios, mensajes u otro contenido interactivo.

### HOOKS

Los React Hooks son herramientas que te permiten usar estados y otras funciones de React sin escribir componentes de clase. Están diseñados para simplificar tu código y facilitar el intercambio de lógica entre componentes.

REF ELEMENT VS GET ELEMENT
Son hooks los dos

- useState está diseñado para administrar el estado de un componente, que representa datos que pueden cambiar con el tiempo y son importantes para la representación del componente. Puedes agregar el estado a tu componente importando el useState

- useRef se utiliza para crear referencias en los componentes de React. Una referencia es un objeto con una currentpropiedad que contiene un valor. Básicamente, hace referencia a un elemento DOM o a una instancia de un componente. Podemos leer y actualizar el valor accediendo a la propiedad actual.


### REFS

proporcionan una forma de acceder a los nodos DOM o elementos React creados en el método de renderizado

Las referencias se crean utilizando React.createRef()elementos de React y se adjuntan a ellos mediante el ref atributo.
Las referencias se asignan normalmente a una propiedad de instancia cuando se construye un componente para que se pueda hacer referencia a ellas en todo el componente.

### Operaciones asincrónicas⏳
En JavaScript, muchas operaciones tardan en completarse, como realizar solicitudes de red, leer o escribir archivos o ejecutar tareas que consumen mucho tiempo. Estas operaciones son asincrónicas, lo que significa que no bloquean el hilo principal de ejecución. Sin un manejo adecuado, pueden generar código complejo y propenso a errores.

### PROMISES
Las promesas son un concepto fundamental en JavaScript para gestionar operaciones asincrónicas

.then()y .catch()💡
Las promesas están equipadas con métodos .then()y .catch(). Puede adjuntar estos métodos a una promesa para manejar los resultados cuando se resuelve o para detectar errores cuando se rechaza. Este enfoque separa claramente el código de manejo de errores y éxito, lo que mejora la organización del código.
tienen un manejo de errores integrado a través del .catch()método, 

```

const myPromise = new  Promise ( ( resolve, reject ) => { 
  // El código asincrónico va aquí 
  // Si la operación tiene éxito, llama a resolve con un resultado 
  // Si la operación falla, llama a reject con un error
 });
```

### REDUX

Es una biblioteca de gestión de estados En el frontend moderno, tienes que juntar la continua variación de datos (mutabilidad), con la incertidumbre de cuando se producen (asincronismo), y eso es una combinación peligrosa.

¿Cuando me interesa Redux entonces? Pues una señal clara de que necesitas ayuda con la gestión de estados es cuando tienes una app tan grande que en un momento dado pierdes el control del cuándo, cómo y por qué de tu estado.

El propósito de Redux es hacer predecibles los cambios de estado, imponiendo ciertas restricciones sobre como y cuando pueden producirse las actualizaciones. Redux consigue que tu gestión de estado sea transparente y determinista, lo que entre otras cosas aporta…

- Mejor comprensión de la evolución del estado en un momento dado
 -Facilidad para incorporar nuevas características a la app
 -Un nuevo abanico de herramientas de debugging (como el time travelling)
 -Capacidad de reproducir un bug
 -Mejoras en el proceso de desarrollo, pudiendo reiniciar la ejecución a partir de un estado concreto.

### ELEMENTOS DE REDUX:
- STORE El almacén es un objeto que contiene todo el estado de la aplicación. Es INMUTABLE
- ACTIONS Las acciones son objetos que describen un cambio en el estado. pueden llevar datos adicionales (como información sobre el cambio) en su propiedad payload.
- REDUCERS Los reductores son funciones puras que toman el estado actual y una acción y devuelven un nuevo estado. Los reductores definen cómo debe cambiar el estado en función del tipo de acción recibida. Deben ser inmutables y no tener efectos secundarios.

### GESTION DE ESTADO
Es el proceso de manejar y controlar la información que cambia en una aplicación web mientras los usuarios interactúan con ella, el estado puede incluir datos como información del usuario, preferencias, datos de visualización, detalles del formulario, autenticación y más. La gestión del estado es esencial porque las aplicaciones modernas son cada vez más interactivas y dinámicas. Los usuarios pueden interactuar con diferentes partes de la aplicación, realizar acciones y esperar que la interfaz responda en tiempo real. Para lograr esto, es necesario tener un método eficiente y organizado para mantener y actualizar el estado.



### Rich Text Editor Styles
Es una biblioteca, que proporciona un editor de texto enriquecido (RTE). Se usa para facilitar a los usuarios la edición de contenido, ofreciendo una experiencia de edición WYSIWYG (What You See Is What You Get)
