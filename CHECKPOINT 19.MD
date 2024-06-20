## BINDING
Es una peculiaridad de los componentes de clase en React.

En componentes de clase, el valor que adopta this dentro de una función dependerá de cómo sea invocada dicha función. 
Cuando nuestra función es utilizada como manejador de eventos (event handler), el valor al que apunta this será undefined. 
¿Por qué? Las declaraciones y expresiones de clase (como por ejemplo nuestra función) se ejecutan en modo estricto,
bajo el cual se aplica el binding por defecto a undefined y no a la instancia del componente como cabría esperar.
Por tanto, el this en un event handler disparado fuera de nuestro componente de clase, perderá la referencia a la instancia a la que pertenece.

La solución pasa por “atar” manualmente el this a la instancia de clase en cada una de las funciones declaradas como métodos de clase. 
--
- ¿Cómo puedo pasar un controlador de eventos (como onClick) a un componente?
Pasa controladores de eventos y otras funciones como props a componentes hijos:

`<button onClick={this.handleClick}>`

- ¿Cómo enlazo una función a la instancia de un componente?
Hay varias maneras de asegurarte que las funciones tengan acceso a los atributos del componente como this.props y this.state, dependiendo de qué tipo de sintaxis o

`this.handleClick = this.handleClick.bind(this);`
