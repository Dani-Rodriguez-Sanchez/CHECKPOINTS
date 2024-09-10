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
