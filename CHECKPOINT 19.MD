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
con HTML creamos una propiedad y un método (post), el cual procesaría nuestro formulario al enviarle
con JS se selecciona este mismo formulario, se le añade un event handler, y ejecutamos la función para enviar el formulario
con REACT es diferente, creamos un estado, y a través de hooks vamos actualizando este valor a través de funciones. de manera que al enviar el formulario, no se actualiza en este momento, si no que ya se ha actualizado de forma dinámica a través de ciclo de vida de este.
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

### REF ELEMENT VS GET ELEMENT

https://www.freecodecamp.org/news/react-state-vs-ref-differences-and-use-cases/#:~:text=Refs%20are%20not%20directly%20linked,without%20affecting%20the%20user%20interface.
---
## Rich Text Editor Styles

### striptags Y truncate

### DROPDOWNS
---

## SLUGS


https://rohitmondallblog.hashnode.dev/usingslug-to-make-dynamic-and-user-friendly-urls-for-our-website
--
## DESESTRUCTURACION

---
## REDUX
Es una herramienta para el control del estado.
En el frontend moderno, tienes que juntar la continua variación de datos (mutabilidad), con la incertidumbre de cuando se producen (asincronismo), y eso es una combinación peligrosa.

Para apps pequeñas no es un problema, todos los frameworks modernos (Angular, React, Vue) proporcionan sus propios mecanismos para almacenar el estado, al margen de Redux.

¿Cuando me interesa Redux entonces? Pues una señal clara de que necesitas ayuda con la gestión de estados es cuando tienes una app tan grande que en un momento dado pierdes el control del cuándo, cómo y por qué de tu estado.

El propósito de Redux es hacer predecibles los cambios de estado, imponiendo ciertas restricciones sobre como y cuando pueden producirse las actualizaciones. Redux consigue que tu gestión de estado sea transparente y determinista, lo que entre otras cosas aporta…

Mejor comprensión de la evolución del estado en un momento dado
Facilidad para incorporar nuevas características a la app
Un nuevo abanico de herramientas de debugging (como el time travelling)
Capacidad de reproducir un bug
Mejoras en el proceso de desarrollo, pudiendo reiniciar la ejecución a partir de un estado concreto.
### REDUCERS
¿Qué son los reductores en Redux?
En Redux , los reductores son funciones puras que manejan la lógica del estado, aceptando el estado inicial y el tipo de acción para actualizar y devolver el estado, facilitando los cambios en los componentes de vista de React.
```
const initialState = {};
const Reducer = (state = initialState, action) => {
   // Write your code here
}
```
### THUNK
La palabra "thunk" es un término de programación que significa "un fragmento de código que realiza un trabajo diferido" . En lugar de ejecutar cierta lógica ahora , podemos escribir un cuerpo de función o código que se pueda usar para realizar el trabajo más tarde.

Específicamente para Redux, los "thunks" son un patrón de escritura de funciones con lógica interna que puede interactuar con los métodos y de una tienda de ReduxdispatchgetState .

El uso de procesadores requiere que se agregue el redux-thunkmiddleware a la tienda Redux como parte de su configuración.

Los thunks son un método estándar para escribir lógica asincrónica en aplicaciones Redux y se utilizan comúnmente para la obtención de datos. Sin embargo, se pueden utilizar para una variedad de tareas y pueden contener lógica sincrónica y asincrónica.

Una función de procesador es una función que acepta dos argumentos: el dispatchmétodo de tienda Redux y el getStatemétodo de tienda Redux. Las funciones de procesador no son llamadas directamente por el código de la aplicación. En cambio, se pasan a store.dispatch():
---
## HOC
HIGH ORDER COMPONENT
es una técnica avanzada en React para el reuso de la lógica de componentes. Los HOCs no son parte de la API de React. Son un patrón que surge de la naturaleza composicional de React.

> Mientras que un componente transforma props en interfaz de usuario, un componente de orden superior transforma un componente en otro.

Los HOCs son comunes en bibliotecas de terceros usadas en React, tales como connect en Redux y createFragmentContainer en Relay.

WITHROUTER es un HOC
https://v5.reactrouter.com/web/api/withRouter
