# MERN
es un conjunto de marcos/tecnologías utilizados para el desarrollo web de aplicaciones que consta de MongoDB, React JS, Express JS y Node JS

### MongoDB

MongoDB es una de las bases de datos NoSQL más sorprendentes que se conoce y está orientada a documentos. 
Una base de datos MongoDB se puede utilizar para almacenar los datos de la aplicación, 
cada registro es un documento que consta de pares clave-valor que son similares a los objetos JSON (JavaScript Object Notation). 
MongoDB es flexible y permite a sus usuarios crear esquemas, bases de datos, tablas, etc 
sin los requerimientos de una pesada base de datos SQL.

### Express JS

Express JS es un marco que se ha superpuesto en la parte superior de Node JS 
y se puede utilizar para crear el backend del sitio web con la ayuda de las estructuras y funciones de Node JS. 
Sin embargo, como Node JS está destinado a ejecutar JavaScript del lado servidor, pero no para desarrollar sitios web, 
Express JS está destinado justo a esto, a crear sitios web.

El marco proporciona un conjunto de herramientas para aplicaciones web, solicitudes y respuestas HTTP ,
enrutamiento y middleware para crear e implementar aplicaciones a gran escala y listas para la empresa.

con él se pueden desarrollar aplicaciones, puntos finales de API , sistemas de enrutamiento y marcos.


### React JS

React JS es básicamente una biblioteca creada por Facebook que se está utilizando ampliamente
para crear componentes de interfaz de usuario en la actualidad. 
Esto puede ayudarnos a crear interfaces de usuario atractivas para nuestras aplicaciones web de una sola página.

### Node.JS

Este es un entorno de ejecución para JavaScript que puede permitirle ejecutar JavaScript del lado servidor y no en un navegador.
Un interesante concepto a tener en cuenta en Node.js es el concepto de módulo, 
recursos que pueden ser más o menos simples o complejos en funcionalidad
y que contiene un código JavaScript que podemos reutilizar en toda nuestra aplicación.
Estos módulos tienen su propio contexto y no interfieren entre sí.
Esto es una notable ventaja pues podemos crear nuestro proyecto a medida sin complicaciones, 
sorpresas ni comportamientos inesperados.

---
# MONGOOSE

Mongoose funciona como una capa adicional sobre MongoDB a través de la cuál se implementan y automatizan muchas de las tareas habituales de trabajar con una base de datos.

Mongoose es una librería para Node.js que nos permite escribir consultas para una base de datos de MongooDB, con características como validaciones, construcción de queries, middlewares, conversión de tipos y algunas otras, que enriquecen la funcionalidad de la base de datos.

Mongoose es un ODM (Object Data Modeling) que permite realizar un mapeo de cada colección de tu base de datos MongoDB a través de esquemas. Estos te ayudarán a acceder a los datos, realizar consultas complejas y estandarizar la estructura de los mismos.

---

# AXIOS

es una biblioteca basada en promesas que permite a los desarrolladores realizar solicitudes a su propio servidor o a un servidor de terceros para obtener datos. 
Ofrece diferentes formas de realizar solicitudes, como GET, POST, PUT/PATCHy DELETE.

Axios es una librería  JavaScript que puede ejecutarse en el navegador y que nos permite hacer sencillas las operaciones como cliente HTTP, por lo que podremos configurar y realizar solicitudes a un servidor y recibiremos respuestas fáciles de procesar.

Después de alojada la web, cuando recibamos respuesta del servidor, se llamará a un callback configurada en then y en el momento que arroje un error, se correrá la misma función, pero definida por catch.

---

# API
(Interfaz de Programación de Aplicaciones): Una API es un conjunto de reglas, protocolos y herramientas que permiten a los desarrolladores de software interactuar con un servicio o plataforma. Básicamente, es una forma de permitir que diferentes aplicaciones o sistemas se comuniquen entre sí, sin que los desarrolladores tengan que preocuparse por la complejidad de cómo funciona internamente cada uno.

Para integrar servicios de terceros, acceder a bases de datos, permitir la creación de aplicaciones móviles, y muchas otras cosas más. En resumen, una API es un conjunto de funciones, métodos y protocolos que permiten a los desarrolladores integrar sus aplicaciones o servicios con otros servicios o plataformas.
---

# API REST
(Application Programming Interface - Representational State Transfer)

es una implementación de la arquitectura de software REST que permite que las aplicaciones accedan y manipulen los recursos a través de una serie de operaciones estándar, como GET, POST, PUT y DELETE.
La API REST permite que las aplicaciones se comuniquen con los servidores web mediante solicitudes HTTP a recursos específicos y que se identifican mediante URIs (Uniform Resource Identifiers).

Una API REST es una API que utiliza los principios de REST para diseñar y exponer servicios web a través de la web. Esto significa que una API REST utiliza las URL y los métodos HTTP estándar de REST para exponer recursos y permitir que los desarrolladores accedan a ellos.

---

# JSON (JavaScript Object Notation)
es un formato que almacena información estructurada y se utiliza principalmente para transferir datos entre un servidor y un cliente.

Glosario
Jan 10, 2023

Deyimar A.

4min de lectura

¿Qué es JSON?

Hay dos elementos centrales en un objeto JSON: claves (Keys) y valores (Values).

Las Keys deben ser cadenas de caracteres (strings). Como su nombre en español lo indica, estas contienen una secuencia de caracteres rodeados de comillas.
Los Values son un tipo de datos JSON válido. Puede tener la forma de un arreglo (array), objeto, cadena (string), booleano, número o nulo.
Un objeto JSON comienza y termina con llaves {}. Puede tener dos o más pares de claves/valor dentro, con una coma para separarlos. Así mismo, cada key es seguida por dos puntos para distinguirla del valor.

Como resultado, la sintaxis literal del objeto JSON se ve así:

`{“key”:“value”,“key”:“value”,“key”:“value”.}`

Una API REST también utiliza el formato de intercambio de datos JSON (JavaScript Object Notation) para representar los datos que se intercambian entre el servidor y el cliente. JSON es un formato de intercambio de datos liviano y fácil de leer y escribir, que se utiliza ampliamente en las aplicaciones web modernas.

### Payload
  
El Payload son los datos que se transmiten en una comunicación. En el contexto de las API, el payload se refiere a los datos que se envían en el cuerpo de una solicitud HTTP o en la respuesta HTTP.

El payload se refiere a los datos que se envían en una solicitud o respuesta, generalmente en formato JSON o XML como ya se los he mostrado, también pueden ser archivos binarios.

### Request
 
Request hace referencia a la solicitud que un cliente envía al servidor para obtener o modificar datos en una API REST.

En una HTTP Request, el método HTTP indica la operación que se desea realizar sobre el recurso. Los métodos más comunes utilizados en la API REST son:

GET: para obtener información sobre un recurso existente.

POST: para crear un nuevo recurso o realizar una operación que no se ajusta a ningún otro método.

PUT: para actualizar completamente un recurso existente.

PATCH: para actualizar parcialmente un recurso existente.

DELETE: para eliminar un recurso existente.

### Response
 
Se refiere a la respuesta enviada por un servidor web después de recibir una solicitud HTTP Request de un cliente.

Una respuesta HTTP incluye un código de estado, cabeceras y un cuerpo.

### Authentication
 
La autenticación es un proceso fundamental en cualquier sistema de seguridad, es esencial para garantizar que solo los usuarios autorizados puedan acceder a los recursos protegidos por la API. El proceso de autenticación generalmente se realiza antes de permitir que un usuario o cliente acceda a una API.


---

# I18n

Se utiliza para para mostrar tu contenido en varios idiomas para apoyar el proceso de internacionalización de tu producto.
permite traducir mi aplicación a varios idiomas de manera sencilla y me proporciona componentes React fáciles de usar. Lo mejor de todo es que es muy flexible y funciona tanto en el servidor como en el cliente.

es un framework de internalización escrito en y para JavaScript.

---

# MIDDLEWARE

Para las llamadas asíncronas a un API.

el middleware es un código que se ejecuta entre el framework que recibe una solicitud, y el framework que genera una respuesta.
Proporciona un punto de extensión para terceros entre el envío de una acción y el momento en que alcanza el reductor. La gente utiliza Redux middleware para el registro de eventos, informes de fallos, para mantener las llamadas a una API asíncrona, enrutamiento y más.

---

# REDUX

Para para administrar el estado de una aplicación de forma predecible.

Redux actúa como un almacén centralizado que contiene y administra el estado de una aplicación o sus componentes. Esta centralización simplifica la gestión del estado, haciéndolo más organizado y accesible.
funciona como la biblioteca oficial de enlaces de interfaz de usuario de Redux. Facilita la integración perfecta de React y Redux, lo que permite una experiencia de desarrollo más natural y eficiente.

Tres conceptos básicos de Redux

- STORE  :
=> Contiene el estado de la aplicación. Hay una tienda para toda la aplicación.
=> Las responsabilidades de la tienda Redux incluyen contener el estado de la aplicación, permitir el acceso al estado a través de getState(),
habilitar actualizaciones de estado a través de dispatch(action)y registrar oyentes a través de subscribe(listener).

- ACTION :
=> Las acciones son la única forma en que su aplicación puede interactuar con la tienda Redux.
=> Describen cambios en el estado.
=> Llevan información desde su aplicación a la tienda Redux en forma de objetos JavaScript simples.
=> Las acciones tienen una propiedad 'tipo' que indica el tipo de acción que se está realizando.
=> En Redux, un creador de acciones crea una acción, que es una función que devuelve la acción.
Las acciones describen que algo pasó, pero no especifican cómo cambió el estado de la aplicación en respuesta. Esto es trabajo de los reducers.

- REDUCER :
=> Realiza transiciones de estado en función de acciones.
=> Los reductores especifican cómo cambia el estado de la aplicación en respuesta a las acciones enviadas a la tienda.
=> Un reductor es una función que acepta el estado actual y una acción como argumentos, y devuelve el siguiente estado de la aplicación.

---
# MUI (Material-User Interface)
Material UI es una biblioteca de componentes React de código abierto que implementa Material Design de Google. Es completa y se puede usar en producción de manera inmediata.

es una tecnología  para diseñar atractivas y dinámicas interfaces de usuario para aplicaciones móviles o sitios web empresariales.
Con la biblioteca MUI React, puedes agregar componentes MUI a tus aplicaciones React y cambiar sin problemas entre MUI CSS/JS y MUI React incluso dentro de la misma aplicación.

Material UI es el design system de Google. Es muy identificable y bonito, aunque demasiado reconocible.
Es una biblioteca de componentes: cajas, diálogos, botones, etc

---
# FORMIK Y YUP
Formik y Yup para crear formularios robustos y fáciles de validar en React

FORMIK es la biblioteca de formularios de código abierto más popular del mundo para React

Formik está diseñado para gestionar formularios con validación compleja con facilidad. Formik admite la validación sincrónica y asincrónica a nivel de formulario y a nivel de campo. Además, viene con soporte integrado para la validación a nivel de formulario basada en esquema a través de Yup.

YUP 
La validación de datos se debe realizar tanto en el frontend como en el backend.
Yup es una biblioteca de validación de esquemas que facilita la definición y validación de la estructura y los tipos de datos en aplicaciones de React. Proporciona una forma declarativa y fácil de definir reglas de validación utilizando una amplia gama de métodos predefinidos y la capacidad de crear validaciones personalizadas.

---
# QUILL 
ES un editor de texto enriquecido.
Para permitir a los usuarios crear contenido atractivo, como publicaciones de blogs y páginas web que incorporan varias opciones de formato y la posibilidad de insertar imágenes. Al integrar un editor de texto enriquecido en su aplicación web, ofrece a los usuarios una interfaz intuitiva que fomenta la creatividad y mejora la experiencia general del usuario.
