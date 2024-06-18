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

