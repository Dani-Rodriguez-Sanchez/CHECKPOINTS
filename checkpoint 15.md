## ¿Qué es AXIOS?
*se instala con `npm i axios`, la agregará a nuestro archivo `package.json`, luego agregará el código de Axios directamente a nuestro node_module.

> AXIOS es una biblioteca npm que se utiliza para hacer solicitudes HTTP.
> es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos para que podamos representarlos en nuestra aplicación. 

en react, es una herramienta que usamos para comunicarnos. hay que importarla (como un componente), y luego llamarla para generar el inicio de sesión.
enviando un objeto a un cliente, y devuelve si estas autorizado o no.

Se envían tres argumentos: 
- la url de la API
- la data, el email y el password
- el opcional "withcredentials"
  
AXIOS VS FETCH
Axios es una librería externa, y Fetch es una herramienta nativa del navegador. Entonces fetch no genera dependencias, esto es positivo para algunos proyectos, por el contrario Axios es más sencillo de configurar, por lo tanto, axios es el más utilizado.
Axios maneja los resultados facilmente, y a través de `catch` capturamos los errores

Entonces ese es el proceso que estamos haciendo ahora, estamos creando la capacidad de crear una sesión en el servidor para que el servidor envíe una cookie,
la almacene directamente en el navegador, y eso es qué se podrá usar para asegurarnos de que tengamos la capacidad de 
iniciar sesión o si no tenemos esa capacidad.

SOLICITUDES HTTP
Las solicitudes HTTP son el **mecanismo mediante el cual las aplicaciones web se comunican con los servidores**. Pueden ser de diferentes tipos, como GET, POST, PUT y DELETE, cada uno con un propósito específico. Imagina que estás construyendo una aplicación que muestra el clima actual de una ciudad. Para obtener los datos actualizados, tu aplicación necesita enviar una solicitud GET al servidor del servicio de pronóstico del tiempo.

---
## COOKIES en react

> son archivos de texto con pequeños datos, como un nombre de usuario y contraseña, que se utilizan para identificar tu ordenador cuando utilizas una red.

En el proceso de autentificación de REACT:

Se genera una cookie llamada `_devcamp_space_session` con un valor en concreto, es una clave secreta, asociada a un nombre de dominio.

Esta cookie es la que nos permite acceder a la aplicación, y es la que se crea cuando se realiza una petición de inicio de sesión. 
Esta cookie se almacena de forma automática en el navegador.

Cuando indicamos en el código withCredentials: true, lo que estamos haciendo es indicar que se envíe la cookie en la petición.

con nuestra respuesta, no solo recuperamos el estado creado, sino que también recibimos estas cookies, y estas cookies se colocarán automáticamente dentro de la sesión de su navegador. Esto significa que puedes salir de la computadora, puedes reiniciar, puedes hacer cualquier cosa y estas cookies aún se almacenarán en el navegador, son un par clave-valor.

---
## ¿Por qué son útiles las herramientas de desarrollo de React? DEVELOPER TOOLS
Es una EXTENSION DEL NAVEGADOR. Se instala por ejemplo en chrome, yendo a chrome web store y buscar React Developer Tools o dar click aqui e instalarlas.

Da la capacidad de obtener una mejor visibilidad específica de React. Esto significa que puede ver los accesorios de su aplicación, su estado, puede ver los componentes además de que  puede ver el árbol de componentes completo y puede inspeccionar todos sus datos.

> SON UTILES PARA  ver la estructura de componentes, examinar las propiedades (props) y el estado (state) de cada componente, y realizar un seguimiento de cómo se comunican entre sí. así como la para la identificación de errores, que sin estas herramientas, sería un proceso más complejo

Es esencial para los desarrolladores, ya que puedes analizar la estructura de componentes, modificar el estado y las props, evaluar el rendimiento y realizar un seguimiento detallado del flujo de datos en tu aplicación React.

---
## ¿Qué es un oyente de eventos? EVENT LISTENER
Es una función Sirve PARA realizar acciones en el programa a través de EVENTOS del usuario. Se asocian acciones a los eventos del usuario.

No es específico de React sino que es general en programación web. Al igual que los eventos HTML DOM, React puede realizar acciones basadas en eventos del usuario.
React tiene los mismos eventos que HTML: hacer clic, cambiar, pasar el mouse, etc.

PREVENTDEFAULT
La diferencia es que en React no puedes retornar `false` para prevenir el comportamiento por defecto. Debes, explícitamente, llamar `preventDefault`.
REACT proporciona un método en el objeto de evento llamado apropiadamente preventDefault para evitar el comportamiento predeterminado.
esto puede indicarle al navegador que no realice ninguna acción predeterminada que el evento normalmente desencadenaría. es particularmente útil cuando se trata de formularios porque a menudo desea garantizar cierta validación de datos, realizar administración de estado o manejar el envío de datos de forma asincrónica, lo que requiere que suprima el comportamiento de envío de formulario predeterminado de una recarga del navegador.


Los eventos de React están escritos en la sintaxis de camelCase: `onClick`
Los controladores de eventos de React están escritos entre llaves: `onClick={shoot}`  en lugar de `onclick="shoot()"`.

Por ejemplo, podríamos tener un botón en una página web y agregar un oyente de eventos para detectar cuándo se hace clic en ese botón, y en respuesta, realizar alguna acción, como mostrar un mensaje o cambiar el contenido de la página.
```
return (
    <button onClick={(event) => shoot("Goal!", event)}>Take the shot!</button>
  );
}
```

DOM (modelo de objetos de documento)
El DOM da una representación del documento como un grupo de nodos y objetos estructurados que tienen propiedades y métodos. Esencialmente, conecta las páginas web a scripts o lenguajes de programación.
El DOM fue diseñado para ser independiente de cualquier lenguaje de programación particular, hace que la presentación estructural del documento sea disponible desde un simple y consistente API.

---
## DEBUGGER
Este depurador nos permite ejecutar el código paso a paso, puesto que se detiene cada vez que se encuentra con la palabra clave debugger. 
Si clicamos en el botón de continuar, la ejecución del código continuará hasta que se encuentre con la siguiente palabra clave debugger.

no es algo específico de React, está integrado directamente en JavaScript, por lo que puedes usarlo en cualquier tipo de aplicación que use JavaScript

Es útil si estamos interesados ​​en descubrir qué sucede en una sección particular de código. 
Si escribimos item en la consola, se nos mostrarán los datos del elemento actual de la lista. Dichos datos, serán aquellos que se introducieron en el servidor y a los que hemos llamado, es decir, los datos de la API. por ejemplo, pordemos `Extraer los nombres de los datos del API `

---
## MIXINS
permite crear código CSS que se reutilizará en todo el sitio web. un mixin es una clase que contiene métodos que pueden ser utilizados por otras clases sin necesidad de heredar de ella.
Los mixins son una forma de compartir comportamiento entre diferentes componentes de React. Son una forma de reutilización de código, un método para compartir funcionalidad entre varios componentes.
POR EJEMPLO, para los estilos

---
## VARIABLES SASS

> En React, a veces es posible que necesitemos actualizar dinámicamente el estilo debido a la interacción del usuario y al cambio en el DOM. En el caso de las variables SCSS, podemos actualizar dinámicamente las variables SCSS usando ReactJS.


Un gran uso de SASS es almacenar los distintos colores utilizados en su aplicación como variables. Luego se puede hacer referencia a estas variables en otros archivos .scss o, en este caso, directamente en sus componentes de React.

A continuación se muestra un ejemplo de cómo crear una variable de color:
```
// _colors.scss 
$colorprimario: #1d6dd3;
```
Este archivo se puede importar fácilmente a cualquier otro archivo .scss haciendo:
```
@import '_colores';
h1 {color: $colorprimario}
```
Pero si desea extraer este color para usarlo directamente en un componente de React, deberá realizar las siguientes actualizaciones:
```
// Cambiar el nombre de _colors.scss a _colors.module.scss 
$primaryColor: $1d6dd3;
:exportar { 
  primario: $colorprimario; 
}
```
