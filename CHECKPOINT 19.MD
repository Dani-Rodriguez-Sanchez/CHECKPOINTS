## BINDING
Es una peculiaridad de los componentes de clase en React.

En componentes de clase, el valor que adopta this dentro de una función dependerá de cómo sea invocada dicha función. 
Cuando nuestra función es utilizada como manejador de eventos (event handler), el valor al que apunta this será undefined. 
¿Por qué? Las declaraciones y expresiones de clase (como por ejemplo nuestra función) se ejecutan en modo estricto,
bajo el cual se aplica el binding por defecto a undefined y no a la instancia del componente como cabría esperar.
Por tanto, el this en un event handler disparado fuera de nuestro componente de clase, perderá la referencia a la instancia a la que pertenece.

La solución pasa por “atar” manualmente el *this* a la instancia de clase en cada una de las funciones declaradas como métodos de clase. 

--
- ¿Cómo puedo pasar un controlador de eventos (como onClick) a un componente?
Pasa controladores de eventos y otras funciones como props a componentes hijos:

`<button onClick={this.handleClick}>`

- ¿Cómo enlazo una función a la instancia de un componente?
Hay varias maneras de asegurarte que las funciones tengan acceso a los atributos del componente como this.props y this.state, dependiendo de qué tipo de sintaxis o

`this.handleClick = this.handleClick.bind(this);`
---
## MODAL
Modal es un elemento UX común. Un modal es un cuadro de diálogo/ventana emergente que se muestra en la parte superior de la página actual. 

Un modal en React es un componente que se superpone a otro contenido en una página web. Es un elemento de la interfaz de usuario que se utiliza para mostrar contenido adicional o para solicitar la interacción del usuario. Los modales de React se utilizan habitualmente para mostrar formularios, mensajes u otro contenido interactivo.

incluye un título, un contenido y un botón de cierre. Ademas admite varias funciones, como el componente de fondo, la tecla de escape para cerrar el modal y la gestión del foco.

INSTALACION: debes instalar React Modal en tu proyecto React. Esto se puede hacer usando npm o yarn. Una vez instalado, puedes importar el modal a tu componente.
---
## STRIPTAGS Y TRUNCATE
- striptags:  Supongamos que se encuentra en una situación en la que desea permitir etiquetas de imagen o etiquetas en negrita, pero no desea ninguna otra. Esto le permite incluir en la lista blanca o negra los elementos con los que no desea trabajar. Esto es realmente útil, es una gran herramienta. Utilizo esto bastante cada vez que trabajo con contenido de tipo HTML que tal vez no quiera renderizar.

>Un ejemplo para el que personalmente tuve que usar esto es para una aplicación de redes sociales que estaba creando y que permitía a las personas escribir código HTML y usé un editor de texto enriquecido, pero no quería permitirles escribir JavaScript y el motivo de Esto se debe a que si permite que un usuario escriba código JavaScript, técnicamente podría secuestrar los navegadores de los usuarios, sus sesiones y podría hacer todo tipo de cosas que son muy malas desde una perspectiva de seguridad. no quería que pudieran inyectar su propio código JavaScript malicioso, por lo que use este tipo de etiqueta como striptags y dije que quiero que permita todo excepto scripts y eso funcionó y esa es una forma en que podría usar algunos de esos parámetros opcionales, pero en este caso, quiero eliminar cualquier tipo de etiqueta.
- truncate: en un generador de resumen Es una biblioteca bastante fácil de usar donde podemos simplemente envolver nuestro contenido dentro de este componente truncado aquí, pasar cuántas líneas,
---
## FORMULARIOS REACT

DIFERENCIA CON HTML
- con HTML creamos una propiedad y un método (post), el cual procesaría nuestro formulario al enviarlo
- con JS se selecciona este mismo formulario, se le añade un event handler, y ejecutamos la función para enviar el formulario
- con REACT es diferente, creamos un estado, y a través de hooks vamos actualizando este valor a través de funciones. de manera que al enviar el formulario, no se actualiza en este momento, si no que ya se ha actualizado de forma dinámica a través de ciclo de vida de este.

*Si eso es correcto!! igualmente puedes probar crear un formulario en react, y cuando escribes dentro de las cajas de texto, veras que no aparece el texto que escribes, tiene que obligatoriamente usar estados para poder hacer que el formulario funcione como se debe!!

Igualmente busca la guía que se llama "Introduction to React Forms" justo antes del checkpoint 15 y te quedara mas claro!*

tomamos el estado, lo configuramos dinámicamente, miramos el evento, el objetivo y la propiedad del nombre. Así sabemos si es un correo electrónico o una contraseña. 
Y si te preguntas, ¿por qué seguiríamos todos estos pasos para aprender esto cuando simplemente podríamos construir un condicional? 
Bueno, imagina un formulario que tiene entradas, no querrás crear 10 condicionales diferentes.
estas tres líneas de código aquí son todo lo que necesitaba hacer para capturar el valor y actualizar el estado
```
handleChange(event) {
    this.setState({
      [event.target.name]: event.target.value
    });
  }
```

COMO QUEDARIA:
```
// login.js

import React, { Component } from "react";

export default class Login extends Component {
  constructor(props) {
    super(props);

    this.state = {
      email: "",
      password: ""
    };

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({
      [event.target.name]: event.target.value
    });
  }

  handleSubmit(event) {
    console.log("Handle submit", event);
  }

  render() {
    return (
      <div>
        <h1>LOGIN TO ACCESS YOUR DASHBOARD</h1>

        <form onSubmit={this.handleSubmit}>
          <input
            type="email"
            name="email"
            placeholder="Your email"
            value={this.state.email}
            onChange={this.handleChange}
          />

          <input
            type="password"
            name="password"
            placeholder="Your password"
            value={this.state.password}
            onChange={this.handleChange}
          />

          <div>
            <button type="submit">Login</button>
          </div>
        </form>
      </div>
    );
  }
}
```
---
## REFS
para acceder a los elementos del DOM, pero al acceder a estos elementos estamos también accediendo a toda su API. Esto nos da acceso a los distintos métodos y propiedades que pueden tener los elementos que insertamos.

Para acceder a un nodo DOM gestionado por React, primero importa el Hook useRef:

`import { useRef } from 'react';`

Luego, úsalo para declarar una ref dentro de tu componente

`const myRef = useRef(null);`

Finalmente, pasa la ref como el atributo ref a la etiqueta JSX en el que quieres obtener el nodo DOM:

`<div ref={myRef}>`

El Hook useRef devuelve un objeto con una sola propiedad llamada current. Inicialmente, myRef.current va a ser null. Cuando React cree un nodo DOM para este <div>, React pondrá una referencia a este nodo en myRef.current. Entonces podrás acceder a este nodo DOM desde tus controladores de eventos y usar las API de navegador integradas definidas en él.



### REF ELEMENT VS GET ELEMENT
Son hooks los dos

- `useState` está diseñado para administrar el estado de un componente, que representa datos que pueden cambiar con el tiempo y son importantes para la representación del componente. Puedes agregar el estado a tu componente importando el useState
- `useRef` se utiliza para crear referencias en los componentes de React. Una referencia es un objeto con una currentpropiedad que contiene un valor. Básicamente, hace referencia a un elemento DOM o a una instancia de un componente. Podemos leer y actualizar el valor accediendo a la propiedad actual.

https://www.freecodecamp.org/news/react-state-vs-ref-differences-and-use-cases/#:~:text=Refs%20are%20not%20directly%20linked,without%20affecting%20the%20user%20interface.

---

## Rich Text Editor Styles
Es una biblioteca, que proporciona un editor de texto enriquecido (RTE). Se usa para facilitar a los usuarios la edición de contenido, ofreciendo una experiencia de edición WYSIWYG (What You See Is What You Get)

vemos el ejemplo de DRAFT.JS, (Desarrollado y mantenido por Facebook) pero hay muchos mas. Draft.js proporciona un marco sólido y extensible para crear editores de texto enriquecido en React. Su arquitectura personalizable permite a los desarrolladores crear soluciones personalizadas, lo que lo hace adecuado para varios proyectos.

crearemos un editor de texto enriquecido, llamaremos a las dependencias clave y luego aplicaremos los estilos iniciales. implementemos el formulario y lo coloquemos directamente dentro del formulario de nuestro blog.
### striptags Y truncate

### DROPDOWNS
En diseño web se les denomina así a los menús desplegables.

### FILE READER. 
Para añadir imagenes a un rich text editor styles.
no podemos simplemente incrustar un archivo de imagen directamente en nuestra cadena de texto. Lo que debemos hacer es tomar la imagen y convertirla en algo que pueda almacenarse como texto y luego podemos incrustarla junto con nuestras etiquetas de párrafo y todo lo demás.
imagenes BASE64 Es basicamente una madera de codificar un archivo binario (una imagen) como un archivo de texto (que se puede leer). De esa manera puedes transmitir la imagen como si fuera simplemente texto. El base 64 encode solo usa los caracteres a-z A-Z 0–9. Se usa para transmitir datos en un soporte que solo soporta el código ASCII visible,

JavaScript tiene una herramienta llamada biblioteca FileReader o módulo FileReader. nos permite hacer es crear esta instancia de FileReader y luego podemos trabajar con ella y luego podemos hacer que realice esta base64. Toma un archivo, en este caso toma una imagen, y luego realizará el procesamiento y la codificación por nosotros.

### PROMESAS
una promesa requiere dos argumentos. Primero se necesita una resolución y luego un rechazo. CON una función de flecha gruesa y luego dentro de aquí, aquí es donde realmente la llamamos.
---

## SLUGS
El slug es una forma legible y válida para la URL de una publicación o página web. 
Es para la personalizacion y OPTIMIZACION DE LAS URL:
`www.noticias.ltda/?p=8679 SIN SLUG`
`www.noticias.ltda/que-es-el-slug-y-por-que-optimizarlo-para-el-seo CON SLUG`

debe ser el slug breve y descriptivo
Las URLs se muestran en los resultados del motor de búsqueda. No ingreses demasiada información, mantenla breve y descriptiva para que también sea fácil de recordar

https://rohitmondallblog.hashnode.dev/usingslug-to-make-dynamic-and-user-friendly-urls-for-our-websiteç

En REACT:
`<Route path="/blog/:slug">`
creamos una nueva ruta para las publicaciones del blog con la ruta /blog/:slug. La :slugparte es un marcador de posición para el slug de cada publicación del blog. Por ejemplo, si el slug de una publicación del blog es how-to-bake-a-cake, la URL sería /blog/how-to-bake-a-cake.

--

## DESESTRUCTURACION
Utilizando la desestructuración de objetos podemos separar en variables las propiedades que teníamos en el objeto
```
const user = {
  name: "Manz",
  role: "streamer",
  life: 99
}

const { name, role, life } = user;

console.log(name);
console.log(role, life);
```
En este ejemplo, separamos las propiedades name, role y life en variables individuales, «sacándolas» de user.

Es una expresión que te permite extraer o “destructurar” datos desde estructuras de datos como arreglos, objetos, mapas y sets y crear nuevas variables con ese dato en particular. Te permite extraer propiedades de un objeto, items de un arreglo de una manera “sencilla” y de una sola vez.


## REDUX
> Es una biblioteca de gestión de estados
En el frontend moderno, tienes que juntar la continua variación de datos (mutabilidad), con la incertidumbre de cuando se producen (asincronismo), y eso es una combinación peligrosa.

https://medium.com/@diego.coder/implementando-redux-en-react-js-redux-toolkit-86b82219584a
https://www.youtube.com/watch?v=QEsukdXFxxs

Para apps pequeñas no es un problema, todos los frameworks modernos (Angular, React, Vue) proporcionan sus propios mecanismos para almacenar el estado, al margen de Redux.

¿Cuando me interesa Redux entonces? Pues una señal clara de que necesitas ayuda con la gestión de estados es cuando tienes una app tan grande que en un momento dado pierdes el control del cuándo, cómo y por qué de tu estado.

El propósito de Redux es hacer predecibles los cambios de estado, imponiendo ciertas restricciones sobre como y cuando pueden producirse las actualizaciones. Redux consigue que tu gestión de estado sea transparente y determinista, lo que entre otras cosas aporta…

- Mejor comprensión de la evolución del estado en un momento dado
- Facilidad para incorporar nuevas características a la app
- Un nuevo abanico de herramientas de debugging (como el time travelling)
- Capacidad de reproducir un bug
- Mejoras en el proceso de desarrollo, pudiendo reiniciar la ejecución a partir de un estado concreto.

---
#### REDUX. QUE ES

es una librería de GESTION DE ESTADO para aplicaciones JavaScript en el lado del Frontend. Su función principal es facilitar la gestión y actualización de la información que se comparte entre diferentes componentes de la aplicación de manera predecible y eficiente.

#### GESTION DE ESTADO
Es el proceso de manejar y controlar la información que cambia en una aplicación web mientras los usuarios interactúan con ella, el estado puede incluir datos como información del usuario, preferencias, datos de visualización, detalles del formulario, autenticación y más.
La gestión del estado es esencial porque las aplicaciones modernas son cada vez más interactivas y dinámicas. Los usuarios pueden interactuar con diferentes partes de la aplicación, realizar acciones y esperar que la interfaz responda en tiempo real. Para lograr esto, es necesario tener un método eficiente y organizado para mantener y actualizar el estado.

#### PRINCIPIOS DE REDUX:
- UNICA FUENTE DE VERDAD El estado de toda la aplicación se almacena en un solo objeto, Siendo asi facilmente accesible
- ESTADO INMUTABLE l estado en Redux es inmutable, lo que significa que no se puede modificar directamente. En lugar de ello, cuando se necesita realizar cambios en el estado, se crea una nueva versión del estado con los cambios aplicados. Esto ayuda a evitar efectos secundarios y simplifica el seguimiento de los cambios.
- CAMBIOS SOLO MEDIANTE ACCIONES Las únicas formas en que el estado puede cambiar en Redux es mediante el envío de “acciones”. Las acciones son objetos simples que describen qué tipo de cambio debe realizarse en el estado. Estas acciones son manejadas por “reductores”, que son funciones puras que toman el estado actual y una acción, y devuelven un nuevo estado.


#### ELEMENTOS DE REDUX:

- STORE El almacén es un objeto que contiene todo el estado de la aplicación. Es INMUTABLE
- ACTIONS Las acciones son objetos que describen un cambio en el estado. pueden llevar datos adicionales (como información sobre el cambio) en su propiedad *payload*.
- REDUCERS Los reductores son funciones puras que toman el estado actual y una acción y devuelven un nuevo estado. Los reductores definen cómo debe cambiar el estado en función del tipo de acción recibida. Deben ser inmutables y no tener efectos secundarios.

```
const initialState = {};
const Reducer = (state = initialState, action) => {
   // Write your code here
}
```
---
#### INSTALACION 
`> npm install @reduxjs/toolkit react-redux `
---
## MIDDLEWARE
permiten agregar funcionalidad a los Stores de Redux.
un middleware es una función, esta función va a recibir como parámetro una versión reducida del Store, con solamente los métodos dispatch y getState.
Sirve para muchas tareas diferentes, registrar datos, capturar errores, despachar promesas, cambiar rutas,

---
### THUNK
redux-thunkEs el middleware más comúnmente utilizado para trabajar con lógica sincrónica y asincrónica fuera de los componentes.

> Redux-thunk te permite escribir creadores de acciones que retornan una función en vez de un objeto de acción típico. Entonces, el thunk puede ser usado para retrasar el envío de una acción hasta que se cumpla una línea de código asíncrona

> un redux-thunk está compuesto de un “creador thunk” (creador de acciones asincrónicas) y “el mismo thunk” el cual es la función que devuelve el “creador Thunk” y acepta el dispatch y setState como argumentos.

```
const INCREMENTAR_CONTADOR = 'INCREMENTAR_CONTADOR';

function incrementar() {
  return {
    type: INCREMENTAR_CONTADOR
  };
}

function incrementarAsync() {
  return dispatch => {
    setTimeout(() => {
      // Es posible invocar acciones sincrónicas o asicrónicas con "dispatch"
      dispatch(incrementar());
    }, 1000);
  };
}
```

Redux-Thunk mejora las capacidades de Redux al proporcionar un mecanismo sencillo y eficiente para gestionar acciones asincrónicas. Permite a los desarrolladores escribir código limpio, predecible y fácil de mantener, al tiempo que garantiza la integridad de la gestión del estado de la aplicación.

La palabra "thunk" es un término de programación que significa "un fragmento de código que realiza un trabajo diferido" . En lugar de ejecutar cierta lógica ahora , podemos escribir un cuerpo de función o código que se pueda usar para realizar el trabajo más tarde.

Específicamente para Redux, los "thunks" son un patrón de escritura de funciones con lógica interna que puede interactuar con los métodos y de una tienda de ReduxdispatchgetState .

El uso de procesadores requiere que se agregue el redux-thunkmiddleware a la tienda Redux como parte de su configuración.

Los thunks son un método estándar para escribir lógica asincrónica en aplicaciones Redux y se utilizan comúnmente para la obtención de datos. Sin embargo, se pueden utilizar para una variedad de tareas y pueden contener lógica sincrónica y asincrónica.

Una función de procesador es una función que acepta dos argumentos: el dispatchmétodo de tienda Redux y el getStatemétodo de tienda Redux. Las funciones de procesador no son llamadas directamente por el código de la aplicación. En cambio, se pasan a store.dispatch():
---
## REDUX TOOLKIT 
La biblioteca principal de Redux no tiene opiniones definidas. Te permite decidir cómo quieres manejar todo, como la configuración de la tienda, qué contiene tu estado y cómo quieres construir tus reductores.Esto es bueno en algunos casos, porque te da flexibilidad, pero esa flexibilidad no siempre es necesaria.

el objetivo de Redux Toolkit es ayudar a simplificar los casos de uso comunes de Redux. No pretende ser una solución completa para todo lo que pueda querer hacer con Redux, pero debería simplificar mucho el código relacionado con Redux que necesita escribir (o, en algunos casos, eliminar por completo parte del código escrito a mano).

exporta varias funciones individuales que puedes usar en tu aplicación y agrega dependencias en otros paquetes que se usan comúnmente con Redux (como Reselect y Redux-Thunk).
incluye: configureStore(), createReducer() etc
---
## REDUX DEVTOOLS
El módulo redux-devtools-extension nos ayudará a filtrar todo lo que pase por el store y así poder verlo desde la consola de desarrolladores de Redux

SON herramientas que están disponibles directamente en el navegador como extensiones de las DevTools nativas del navegador.

proporciona una consola para configurar nuestro entorno de desarrollo con Redux. Esta extensión ayuda a visualizar los movimientos y las modificaciones de estado en el software basado en Redux.

### REDUX DEVTOOLS VS REAC DEVELOPER TOOLS
---
## HOC
HIGH ORDER COMPONENT
Los componentes de orden superior son útiles para abstraer una lógica compartida utilizada por muchos componentes (Los componentes en React permiten la reutilización de código y evitan la repetición de código)
es una técnica avanzada en React para el reuso de la lógica de componentes. Los HOCs no son parte de la API de React. Son un patrón que surge de la naturaleza composicional de React.

https://deadsimplechat.com/blog/higher-order-componets-in-react/

> Mientras que un componente transforma props en interfaz de usuario, un componente de orden superior transforma un componente en otro.

https://legacy.reactjs.org/docs/higher-order-components.html

Los HOCs son comunes en bibliotecas de terceros usadas en React, tales como connect en Redux y createFragmentContainer en Relay.

WITHROUTER es un HOC
https://v5.reactrouter.com/web/api/withRouter
---
## ASINCRONISMO

> es realizar acciones o tareas sin esperar que un proceso anterior se realice,
> programación asíncrona es una técnica que permite a tu programa iniciar una tarea de larga duración y seguir respondiendo a otros eventos mientras esa tarea se ejecuta, en lugar de tener que esperar hasta que esa tarea haya terminado. Una vez que dicha tarea ha finalizado, tu programa presenta el resultado.

Redux, por su naturaleza puramente funcional, esta pensado para realizar tareas síncronas:

`(state, action) => newState`
Sin embargo, debido a como funciona JS lo más común es trabajar de forma asíncrona, por ejemplo hacer una petición AJAX a una API es asíncrono y luego de esto seguramente vamos a querer modificar el Store en base a la respuesta.

Para esto se usan las acciones asíncronas, hay varias formas de trabajar con acciones asíncronas en Redux, una es hacerlo a mano, otra opción es usar es usar distintos middlewares.

La gran ventaja de usar **middlewares** que nos solucionen esto es que si en muchas partes vamos a usar acciones asíncronas (y es muy probable que pase) nos ahorramos mucho trabajo cada vez que despachamos la acción.
---
## REACT HTML PARSER
Una utilidad para convertir y analizar
cadenas HTML en componentes React 

html-react-parser Este analizador funciona tanto en el lado del servidor como del cliente y convierte una cadena HTML en uno o más elementos React.
El uso es el siguiente:
```
import parse from 'html-react-parser';
const MyComponent = () => {
 const htmlString = '<div>A simple HTML string</div>';
return <div>{parse(htmlString)}</div>
}
```
