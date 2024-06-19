## Qué es una función de desplazamiento infinito? o SCROLL INFINITO
- A nivel de usuario: Es un diseño que permite a los usuarios seguir viendo la información sin pausa, 
de manera que esta se va recargando mientras estos se desplazan hacia abajo. Es alternativa a la PAGINACION.
- A nivel de programación: es una función que carga un determinado número de elementos, y al llegar al final de la página 
carga y muestra más elementos. Se hace para evitar que la página se cargue excesivamente y se ralentice.
Entonces se agrega un CONTROLADOR DE DESPLAZAMIENTO, a traves de un `event listener`, necesitamos saber la posición en la que está el usuario, 
esto se hace con 3 elementos : altura de la ventana, altura del scroll, y altura total. 
Con la suma de los dos primeros sabremos la posición en la pagina respecto al total que es el tercero
Se utiliza el SPINNER DE CARGA para avisar al usuario de que la carga está en progreso.

## Spinner de carga

Es un pequeño ícono que gira a medida que ingresan tus datos, gira y eso te indica que la aplicación está funcionando. 

Util cuando se trata de una función de desplazamiento infinito, si no tienes alguna forma de decirle al usuario que hay más publicaciones, 
cuando se desplaza hasta el final de la página, lo que quiero es tener un poco de ícono aquí que comienza a girar para brindarles información para decir:
"tenemos más registros y estamos trabajando para conseguirlos ahora mismo".

## ¿Qué es un modal?

Es un **cuadro de diálogo** interectivo, que se superpone al contenido principal de la página.
Se instala como una librería externa

sirve para:
- Introducir los datos de un formulario
- Introducir datos para un inicio de sesión
- Aceptación de los terminos legales del servicio
- confirmar una acción (eliminar un elemento de un blog)

Se abren con un event listener, y se cierran con otro (clicando fuera o esc) o cuando termina su función

## Formularios. diferencia de comportamiento con html

un formulario permite que un usuario introduzca datos que luego serán enviados a nuestro servidor para ser procesados.
Los formularios en React son un tipo de elemento en esta librería de JavaScript que proviene del código HTML. Aun así, los formularios en React son un poco diferentes.

En nuestro post sobre el estado en React, te hemos mencionado que existen dos tipos de datos en esta librería de JavaScript: las propiedades o props y los estados. Entonces, lo que renderizamos y vemos en pantalla es el resultado de estos dos tipos de datos, es decir, de las props y del estado interno que tiene un componente. De este modo, todo lo que vemos en pantalla siempre es reflejo de los datos que estamos manejando en el código de nuestra aplicación. Ten muy presente esto, pues es lo que diferencia los formularios en React de los formularios en HTML.

Imaginemos que tenemos un formulario de perfil de usuario que estamos trabajando en HTML y JavaScript. Ahora, queremos acceder a este formulario para actualizar nuestro correo en la página de perfil. Para acceder a este formulario por debajo de la aplicación, seguro que habrá una llamada a la API que nos dice cuál es nuestro correo y nos permite sobrescribirlo. De esta forma, por un lado, tenemos el dato de nuestro correo, y por otro, estamos modificando nuestro correo.

Mientras estamos modificando nuestro correo, normalmente no tenemos este dato almacenado en ningún sitio. Al contrario: es cuando enviamos el formulario que se actualiza nuestro correo en el servidor y se guarda. En React, esto cambia un poco.

¿Cómo funcionan los formularios en React?
Existen dos maneras básicas de manejar formularios en React:

- La primera suele ser más fácil de entender, pues es similar a otros programas. Consiste en dejarle la responsabilidad al DOM. Esto quiere decir que dejamos que los inputs de los formularios trabajen solos de manera inicial. Luego, cuando necesitemos hacer un submit de los formularios y capturamos los valores que tienen estos inputs para poder mandarlos al API. A este método se le conoce como formularios no controlados.
- La segunda forma de manejar formularios en React y la mejor manera de hacerlo es al controlarlos. Cuando trabajamos con formularios de manera controlada, todo lo que veamos en pantalla lo vamos a tener en el estado. Es decir, si vemos algo en pantalla es porque está así en el estado. Con esto queremos decir que todo, incluso los valores que tenemos en los inputs de un formulario, van a ser parte de un estado.

## router. que es?

La aplicación Create React no incluye el enrutamiento de páginas.

React Router es la solución más popular.

React Router es una biblioteca estándar para enrutamiento en React . Permite la navegación entre vistas de varios componentes en una aplicación React, permite cambiar la URL del navegador y mantiene la interfaz de usuario sincronizada con la URL. Creemos una aplicación sencilla para React para comprender cómo funciona React Router. La aplicación contiene tres componentes: el componente de inicio , el componente Acerca de y el componente de contacto . 
Usaremos React Router para navegar entre estos componentes.
entonces tiene el comportamiento predeterminado en HTML que consiste en navegar a una nueva página cuando el usuario envía el formulario.

## estados de vida
los componentes poseen algo conocido como el ciclo de vida. Este ciclo de vida son una serie de funciones que se ejecutan en distintos momentos de la vida del componente y nos permiten realizar distintas acciones en estos momentos.
El ciclo de vida se puede dividir en 3 fases, el montado, actualización y desmontado del componente. Estas fases a su vez se dividen en varios métodos que puede tener el componente.

a — Montaje
Cuando se crea una instancia de un componente y se inserta en el DOM

b — Actualización
Cuando sufre algún cambio las propiedades (props) o el estado (state) del componente.

c — Desmontaje
Cuando el componente se elimina del DOM.


https://platzi.com/blog/ciclo-de-vida-de-un-componente-de-reactjs/

