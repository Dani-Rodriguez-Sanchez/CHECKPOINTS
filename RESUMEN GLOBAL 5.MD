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

