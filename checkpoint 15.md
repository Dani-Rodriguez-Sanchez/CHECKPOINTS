## ¿Qué es Axios?
AXIOS es una biblioteca npm. es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos 
para que podamos representarlos en nuestra aplicación. Se instala con npm install axios. la agregará a nuestro archivo `package.json` 
y luego, como hemos visto algunas veces antes. luego agregará el código de Axios directamente a nuestro módulo de nodo.

en react, es una herramienta que usamos para comunicarnos. hay que importarla (como un componente), y luego llamarla para generar el inicio de sesión.
enviando un objeto a un cliente, y devuelve si estas autorizado o no.
Se envían tres argumentos: 
- la url de la API
- la data, el email y el password
- el opcional "withcredentials"
  
*`axios trabaja con promesas`


Entonces ese es el proceso que estamos haciendo ahora, estamos creando la capacidad de crear una sesión en el servidor para que el servidor envíe una cookie,
la almacene directamente en el navegador, y eso es qué se podrá usar para asegurarnos de que tengamos la capacidad de 
iniciar sesión o si no tenemos esa capacidad.

## PROMESAS EN REACT
