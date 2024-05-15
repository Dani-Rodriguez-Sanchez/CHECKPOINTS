## ¿Cuál es el comando para instalar un módulo de nodo?
npm install [nombre-del-módulo]. Con este comando, se puede agregar cualquier módulo o biblioteca disponible en el registro de npm a un proyecto de Node.js.


- NVM. Node Version Manager. es un administrador de versiones que le permite instalar y cambiar entre diferentes versiones de Node.js en una sola máquina.
- NPM  Viene incluido con Node.js y se instala automáticamente. Maneja la instalación de paquetes, la gestión de versiones y la resolución de dependencias dentro de un proyecto node.js. NPM lee el archivo `package.json.
- NODE  es un entorno de ejecución usado para ejecutar código JavaScript en los servidores. Permite ejecutar JavaScript sin necesidad de un navegador web. 

INSTALACION: 
instalaria HOMEBREW, 
despues: brew install nvm. 
Una vez instalado nvm, instalamos node: nvm install node. 
Luego para elegir la version: nvm ls-remote
para instalar la elegida: nvm install 16
para usar la elegida: nvm use 16
para definiarla como default: nvm alias default 16
para ver que version tenemos funcionando: node -v

* El comando para instalar un módulo en Node.js utilizando el gestor de paquetes npm es npm install [nombre-del-módulo].
* El comando npm install descargará el módulo desde el registro público de npm y lo colocará en la carpeta node_modules de nuestro proyecto.
* Además, actualizará automáticamente el archivo package.json y el archivo package-lock.json con la nueva dependencia.
  
## que son dependencias?

(son elementos para que una aplicación se ejecute), en desarrollo, son bibliotecas, módulos, o paquetes.
En react, están dentro de la carpeta node_modules, y hay que llamarlas desde package.json, indicando  nombre y versión. Se instalan después con npm install. Y en app.js hay que importarlas con “import moment from 'moment'”

## ¿Cuáles son los dos tipos de componentes de react?

Componentes: 
Son como funciones, fragmentos de código independientes y reutilizables. Aceptan entradas (props), y devuelven elementos de react. Cada una tiene su propia lógica y su propósito es renderizar algo.
se almacenan en src/components
Dos tipos: FUNCIONALES, Y DE CLASE:

FUNCIONAL.  son similares a las funciones de JavaScript que reciben propiedades (props) y devuelven elementos de React para su renderización.
(un ReactNode puede ser un elemento html, un string, un booleano, entre otros tipos de datos.). Son las más simples y concretos, ya que solo reciben y retornan

DE CLASE. se crean utilizando clases de JavaScript, que extienden (amplian) la clase React.Component proporcionada por el propio React. 
son clases simples (compuestas por múltiples funciones que agregan funcionalidad a la aplicación). requiere que lo extiendas desde React. Componente y cree una función de renderizado que devuelva un elemento de React.

## ¿Por qué usamos accesorios en React?
PROPS? (son las propiedades de un componente)
Es una manera de pasarle información dinámica a un componente, esto da dinamismo al sistema, ya que un mismo prop, puede dar lugar a diferentes resultados con diferentes instancias, y además da la posibilidad de reutilizar componentes
También es una manera de pasar información entre componentes, de padre a hijo


## ¿Qué es JSX?
Es una extensión del lenguaje de JS, que permite escribir de manera similar al HTML
En React, JSX es una parte integral de React, que permite a los desarrolladores escribir el marcado y la lógica de estos componentes en un único archivo.
JSX se transforma en JavaScript normal antes de ejecutarse en el navegador. La sintaxis de JSX por sí misma no puede ser leída o ejecutada por un navegador, para hacerlo, es necesario convertir la sintaxis de JSX en instrucciones válidas del lenguaje.
Esta transformación se realiza mediante una herramienta llamada transpilador. El transpilador más popular para JSX es Babel.

##¿Qué es el STATE?
El STATE es un objeto que contiene datos que pueden cambiar en el tiempo. En React, el estado se usa para controlar los cambios en la interfaz.
Es un objeto, incorporado a los componentes de react.
es donde se almacenan los valores de propiedad (interacciones) que pertenecen a ese componente.
Cuando el state objeto cambia, el componente se vuelve a renderizar.
El stateobjeto se inicializa en el constructor
El stateobjeto puede contener tantas propiedades como quieras
Es inmutable, pero se puede establecer un nuevo valor
*Como prop, afecta al renderizado del componente, pero este se define dentro del propio componente.

## ¿Con qué tipo de Componente utilizamos un Constructor?
CONSTRUCTOR: es un método utilizado para inicializar el estado de un objeto en una clase.
Por lo tanto utilizamos el componente de tipo clase.
Las utilidades del constructor son inicializar el estado local del componente asignando un objeto a this.state. Y para vincular eventos
SUPER . no se puede acceder a este objeto.props directamente desde el principio, lo que puede provocar errores, entonces transferimos el valor de un accesorio a la función super() desde el constructor(). Cuando llamas a la función super(), se llama al constructor de la clase principal, que en el caso de React es React.Component. 

## LINK VS NAVLINK
¿Cuál es la diferencia respecto a NavLink?
Son enlaces que nos permitan navegar entre las diferentes rutas. O, dicho de otra manera, cómo ligar dichas rutas a elementos de la interfaz de usuario para poder navegar a las diferentes páginas de nuestra aplicación.
A priori puede parecer que ambos elementos funcionan de la misma forma, y en cierto modo, así es. Sin embargo, NavLink tiene una funcionalidad extra y es que, entre otras cosas, añade la clase ACTIVE (esto lo vemos en el inspector de JS) al elemento que se está visitando. Esto es muy útil para, por ejemplo, añadir un estilo diferente a la ruta que se está visitando. Por no hablar de que permite modificar el nombre de la clase para que en vez de ser active sea el nombre que nosotros queramos.

## SLUG
(o permalink) se usa como convenio para aquellas URLs que tienen partes customizadas, que podrían ser parámetros.
En este caso, el slug sería el nombre del proyecto, la habilidad o la empresa.

## ¿Qué es Axios?
AXIOS es una biblioteca npm. es un conjunto de código JavaScript, que nos permite llamar a API y luego acceder a los datos para que podamos representarlos en nuestra aplicación.
Se instala con npm install axios.
la agregará a nuestro archivo package.json y luego, como hemos visto algunas veces antes. luego agregará el código de Axios directamente a nuestro módulo de nodo.
