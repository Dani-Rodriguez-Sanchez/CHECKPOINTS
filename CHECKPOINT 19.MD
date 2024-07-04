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
---

## SLUGS
El slug es una forma legible y válida para la URL de una publicación o página web. 
Es para la personalizacion y OPTIMIZACION DE LAS URL:
www.noticias.ltda/?p=8679 SIN SLUG
www.noticias.ltda/que-es-el-slug-y-por-que-optimizarlo-para-el-seo CON SLUG
debe ser el slug breve y descriptivo
Las URLs se muestran en los resultados del motor de búsqueda. No ingreses demasiada información, mantenla breve y descriptiva para que también sea fácil de recordar

https://rohitmondallblog.hashnode.dev/usingslug-to-make-dynamic-and-user-friendly-urls-for-our-website
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

Mejor comprensión de la evolución del estado en un momento dado
Facilidad para incorporar nuevas características a la app
Un nuevo abanico de herramientas de debugging (como el time travelling)
Capacidad de reproducir un bug
Mejoras en el proceso de desarrollo, pudiendo reiniciar la ejecución a partir de un estado concreto.
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

### THUNK

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
## REDUX DEVTOOLS
SON herramientas que están disponibles directamente en el navegador como extensiones de las DevTools nativas del navegador.

proporciona una consola para configurar nuestro entorno de desarrollo con Redux. Esta extensión ayuda a visualizar los movimientos y las modificaciones de estado en el software basado en Redux.

### REDUX DEVTOOLS VS REAC DEVELOPER TOOLS
---
## HOC
HIGH ORDER COMPONENT
es una técnica avanzada en React para el reuso de la lógica de componentes. Los HOCs no son parte de la API de React. Son un patrón que surge de la naturaleza composicional de React.

> Mientras que un componente transforma props en interfaz de usuario, un componente de orden superior transforma un componente en otro.

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
