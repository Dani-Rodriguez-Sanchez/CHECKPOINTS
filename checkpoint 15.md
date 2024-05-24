## ¿Qué es Axios?
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
Axios es una librería y Fetch es una herramienta nativa del navegador. Entonces fetch no genera dependencias, esto es positivo para algunos proyectos, por el contrario Axios es más sencillo de configurar


Entonces ese es el proceso que estamos haciendo ahora, estamos creando la capacidad de crear una sesión en el servidor para que el servidor envíe una cookie,
la almacene directamente en el navegador, y eso es qué se podrá usar para asegurarnos de que tengamos la capacidad de 
iniciar sesión o si no tenemos esa capacidad.

## cookies en react

> son archivos de texto con pequeños datos, como un nombre de usuario y contraseña, que se utilizan para identificar tu ordenador cuando utilizas una red.

En el proceso de autentificación de REACT:

Se genera una cookie llamada `_devcamp_space_session` con un valor en concreto, es una clave secreta, asociada a un nombre de dominio.

Esta cookie es la que nos permite acceder a la aplicación, y es la que se crea cuando se realiza una petición de inicio de sesión. 
Esta cookie se almacena de forma automática en el navegador.

Cuando indicamos en el código withCredentials: true, lo que estamos haciendo es indicar que se envíe la cookie en la petición.

con nuestra respuesta, no solo recuperamos el estado creado, sino que también recibimos estas cookies, y estas cookies se colocarán automáticamente dentro de la sesión de su navegador. Esto significa que puedes salir de la computadora, puedes reiniciar, puedes hacer cualquier cosa y estas cookies aún se almacenarán en el navegador, son un par clave-valor.

## ¿Por qué son útiles las herramientas de desarrollo de React?


## ¿Qué es un oyente de eventos?


