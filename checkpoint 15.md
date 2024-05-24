## ¿Qué es AXIOS?
*se instala con `npm i axios`

AXIOS es una biblioteca npm. es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos 
para que podamos representarlos en nuestra aplicación. la agregará a nuestro archivo `package.json` 
y luego, como hemos visto algunas veces antes. luego agregará el código de Axios directamente a nuestro módulo de nodo.

en react, es una herramienta que usamos para comunicarnos. hay que importarla (como un componente), y luego llamarla para generar el inicio de sesión.
enviando un objeto a un cliente, y devuelve si estas autorizado o no.
Se envían tres argumentos: 
- la url de la API
- la data, el email y el password
- el opcional "withcredentials"
  
AXIOS VS FETCH
Axios es una librería y Fetch es una herramienta nativa del navegador. Entonces fetch no genera dependencias, esto es positivo para algunos proyectos, por el contrario Axios es más sencillo de configurar, por lo tanto, axios es el más utilizado.


Entonces ese es el proceso que estamos haciendo ahora, estamos creando la capacidad de crear una sesión en el servidor para que el servidor envíe una cookie,
la almacene directamente en el navegador, y eso es qué se podrá usar para asegurarnos de que tengamos la capacidad de 
iniciar sesión o si no tenemos esa capacidad.

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
Es una EXTENSION DEL NAVEGADOR

brinda la capacidad de obtener una mejor visibilidad específica de React. Esto significa que puede ver los accesorios de su aplicación, su estado, puede ver los componentes secundarios, los componentes principales, puede ver el árbol de componentes completo y puede inspeccionar todos sus datos.

SON UTILES PARA seleccionar y visualizar los componentes de React que se están utilizando en la aplicación. Además, también permite ver el estado de los componentes, así como los props que se están pasando a cada uno de ellos, así como la identificación de errores. Sin estas herramientas, sería un proceso más complejo


---
## ¿Qué es un oyente de eventos? EVENT LISTENER

---
## DEBUGGER
Este depurador nos permite ejecutar el código paso a paso, puesto que se detiene cada vez que se encuentra con la palabra clave debugger. 
Si clicamos en el botón de continuar, la ejecución del código continuará hasta que se encuentre con la siguiente palabra clave debugger.

no es algo específico de React, está integrado directamente en JavaScript, por lo que puedes usarlo en cualquier tipo de aplicación que use JavaScript

Es útil si estamos interesados ​​en descubrir qué sucede en una sección particular de código. 

Si escribimos item en la consola, se nos mostrarán los datos del elemento actual de la lista. Dichos datos, serán aquellos que se introducieron en el servidor y a los que hemos llamado, es decir, los datos de la API. por ejemplo, pordemos `Extraer los nombres de los datos del API `
