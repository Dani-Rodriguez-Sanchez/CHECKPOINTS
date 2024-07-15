## CRA VS VITE

- Create React App. 
abreviado como CRA, es una herramienta desarrollada por Facebook para ayudar a los desarrolladores a configurar un proyecto de React 
desde cero de manera rápida y sencilla. CRA ofrece una configuración predefinida que es adecuada para la mayoría de los proyectos de React.
Esto significa que puedes comenzar a codificar de inmediato sin tener que preocuparte por las configuraciones iniciales.

- VITE. es una herramienta más reciente que ha ganado popularidad rápidamente en el mundo del desarrollo web con React. 
Desarrollada por Evan You, el creador de Vue.js, Vite promete una experiencia de desarrollo aún más rápida y eficiente que CRA.
Vite es conocido por su velocidad de desarrollo sobresaliente. Utiliza la compilación en tiempo real y el reemplazo de módulos (module replacement) 
para proporcionar una experiencia de desarrollo prácticamente instantánea.

DIFERENCIAS:
* Velocidad de desarrollo: con vite Gracias a su enfoque en el reemplazo de módulos y la compilación en tiempo real, los cambios se reflejan de inmediato en la aplicación. En cambio, Create React App, aunque ofrece una velocidad de desarrollo decente, no puede igualar la velocidad de Vite debido a su enfoque más tradicional.
* Configuración: Create React App brinda una configuración predeterminada que es fácil de usar para proyectos estándar de React. Sin embargo, si necesitas realizar configuraciones personalizadas específicas, puede requerir un poco más de esfuerzo y comprensión de las configuraciones de Webpack. Por otro lado, Vite destaca por su configuración mínima y su enfoque basado en estándares como ESM.
* Compatibilidad con proyectos existentes: si estás trabajando en un proyecto de React existente, Create React App puede ser una opción más cómoda, ya que está diseñado para ser compatible con proyectos ya en marcha. Puedes migrar tu proyecto a CRA sin demasiados problemas y continuar trabajando en él. En contraste, Vite está más orientado a proyectos nuevos. Si bien es posible migrar proyectos existentes a Vite, puede requerir un poco más de trabajo.
* Comunidad y ecosistema: Create React App ha existido durante más tiempo y tiene una comunidad establecida. Esto significa que puedes encontrar una gran cantidad de recursos, documentación y complementos desarrollados por la comunidad para ayudarte en tu proyecto. Vite, aunque más nuevo, también ha crecido rápidamente y tiene una comunidad en crecimiento.

ENTONCES: 
- Si buscas la máxima velocidad de desarrollo y estás dispuesto a aprender una nueva forma de trabajar, Vite es una excelente elección.

- Si estás trabajando en un proyecto existente de React o prefieres una configuración más tradicional, Create React App sigue siendo una opción sólida. Ten en cuenta que, si estás empezando con React y deseas una introducción suave al desarrollo web, Create React App

---
## REACT NATIVE
React Native, es un framework de código abierto creado por Meta Platforms, Inc.​ Se utiliza para desarrollar aplicaciones para Android, ​ Android TV, ​ iOS, macOS, ​ tvOS, Web, ​ Windows​ y UWP​ al permitir que los desarrolladores usen React con las características nativas de estas plataformas.

React Native usa el mismo paradigma fundamental de construcción de bloques de UI (componentes visuales con los que interacciona el usuario) que las aplicaciones nativas reales de Android e iOS, pero gestiona la interacción entre los mismos utilizando las capacidades de JavaScript y React.

https://www2.deloitte.com/es/es/pages/technology/articles/que-es-react-native.html
---
## REACT ANIMATE HEIGHT
https://www.npmjs.com/package/react-animate-height

> Componente React sin dependencias para animar la altura mediante transiciones CSS. Deslice un elemento hacia arriba y hacia abajo o anímelo a una altura específica. La opacidad del contenido también se puede animar de forma opcional (consulte animateOpacityla propiedad a continuación).
QUICK START:

Get it from npm

`$ npm install --save react-animate-height`

Import and use it in your React app.
```
import React, { useState } from 'react';
import AnimateHeight from 'react-animate-height';

const Example = () => {
  const [height, setHeight] = useState(0);

  return (
    <div>
      <button
        aria-expanded={height !== 0}
        aria-controls="example-panel"
        onClick={() => setHeight(height === 0 ? 'auto' : 0)}
      >
        {height === 0 ? 'Open' : 'Close'}
      </button>

      <AnimateHeight
        id="example-panel"
        duration={500}
        height={height} // see props documentation below
      >
        <h1>Your content goes here</h1>
        <p>Put as many React or HTML components here.</p>
      </AnimateHeight>
    </div>
  );
};
```
### GIT DIFF
sirve para Mostrar cambios entre el árbol de trabajo y el índice o un árbol, cambios entre el índice y un árbol, cambios entre dos árboles, cambios resultantes de una fusión, cambios entre dos objetos blob o cambios entre dos archivos en el disco.
En suma, da una vista más detallada de los cambios.

git diff es un comando multiusos de Git que, cuando se ejecuta, lleva a cabo una función para establecer las diferencias en los orígenes de datos de Git. Dichos orígenes de datos pueden ser confirmaciones, ramas y archivos, entre otras posibilidades. 

Gracias a este comando, no solo obtienes una visión general de tu repositorio, sino que además puedes identificar más rápidamente las fuentes de errores en el código en caso de problemas. La sintaxis de git diff es siempre la misma. El comando tiene el siguiente aspecto:
`git diff`

ejemplo:
https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/git-diff/

### INTERFACES

Básicamente, se trata de un lugar donde declaras todas tus variables antes de usarlas en el archivo real.
---
## JavaScript String substring()
El substring()método de Stringvalores devuelve la parte de esta cadena desde el índice inicial hasta el índice final excluido, o hasta el final de la cadena si no se proporciona ningún índice final.
```
const str = 'Mozilla';

console.log(str.substring(1, 3));
// Expected output: "oz"

console.log(str.substring(2));
// Expected output: "zilla"
```

https://www.w3schools.com/jsref/jsref_substring.asp
Muchos lenguajes han eliminado eso porque a veces es bastante innecesario, excepto para operaciones de gran escala que intentan desarrollar bibliotecas como esta.
---
## MEDIA QUERIES
Este gancho de React detecta coincidencias con una consulta de medios CSS. Permite la representación de componentes en función de si la consulta coincide o no.
La cadena de consulta de medios puede ser cualquier consulta de medios CSS válida, por ejemplo '(prefers-color-scheme: dark)'.
```
import * as React from 'react';
import useMediaQuery from '@mui/material/useMediaQuery';

export default function SimpleMediaQuery() {
  const matches = useMediaQuery('(min-width:600px)');

  return <span>{`(min-width:600px) matches: ${matches}`}</span>;
}
```

---
## FR

en CSS, La unidad relativa fr en CSS o unidad de medida fr la introduce el sistema de posicionamiento CSS Grid. Esta unidad representa una fracción del contenedor. Entonces, 1fr representa una fracción, 2fr dos fracciones… La unidad relativa fr en CSS o unidad de medida fr es relevante para la creación de la cuadrícula en CSS Grid, llamada como grid fr, porque con ella podemos definir las medidas, tanto de las columnas como de las filas, en proporción con las demás.

Esto quiere decir que, por ejemplo, en vez de darle a una columna una unidad de medida absoluta, como lo son los píxeles, podemos asignarle una fracción del ancho total de las columnas.

## FETCH
fetch y AXIOS son herramientas de peticiones HTTP. 
> Axios es una librería y Fetch es una herramienta nativa del navegador

la principal diferencia es que fetch es una herramienta implementada directamente dentro del navegador.
(Un detalle muy importante a la hora de trabajar con Fetch es que sus peticiones se ejecutan a través de promesas. Esto se da porque las peticiones HTTP no tienen un tiempo determinado, por lo que se consideran procesos asíncronos.)

Algunos desarrolladores prefieren crear proyectos de 0 dependencias. Esto significa ejecutar todo el código sin herramientas o librerías externas a los lenguajes de programación principales. En estos escenarios, Fetch es una herramienta más deseable, pues su estado nativo hace que no creemos ninguna dependencia externa.

Axios es mucho más completa que Fetch, pues es una librería entera y no un solo método. Esto quiere decir que nos brinda más posibilidades, es mejor usar Axios cuando vamos a ejecutar una diversidad de acciones recurrentes en un proyecto grande. Sin embargo, si vas a ejecutar algo muy puntual y concreto, podrás usar Fetch sin ningún problema, con lo que evitarás también generar una nueva dependencia en un proyecto sencillo.

## CSS QUERIES

---
---
# SQL
## QUE ES
SQL es un lenguaje de programación que se utiliza para trabajar con bases de datos relacionales. El acrónimo SQL significa Structured Query Language (Lenguaje de Consulta Estructurado).
Las aplicaciones modernas, en su inmensa mayoría, utilizan bases de datos para almacenar la información

### BASES DE DATOS RELACIONALES son aquellas que almacenan la información en tablas, y que relacionan unas tablas con otras mediante claves primarias y claves foráneas.
Todas estas tablas pueden tener referencias entre sí.
Las bases de datos relacionales se basan en el *modelo relacional*, una forma intuitiva y directa de representar datos en *tablas*.
En una base de datos relacional, cada fila en una tabla es un registro con una ID única, llamada *clave*.
Las columnas de la tabla contienen los *atributos* de los datos y cada registro suele tener un valor para cada atributo, lo que simplifica la creación de relaciones entre los puntos de datos.


## CRUD
CRUD es una función esencial para muchos sistemas de información, ya que permite a los usuarios realizar tareas básicas de mantenimiento y gestión de datos.

El acrónimo CRUD es muy utilizado en el mundo de la programación a la hora de trabajar con bases de datos. Este acrónimo significa:

- Create: crear datos.
- Read: leer datos.
- Update: actualizar datos.
- Delete: eliminar datos.

La idea es que cualquier sistema de información que interactúe con datos debe proporcionar funcionalidades para crearlos, leerlos, actualizarlos y eliminarlos.

son las operaciones básicas que se pueden realizar sobre una base de datos. 
---
## implementaciones de SQL
el lenguaje SQL es el mismo para todas ellas. La diferencia entre unas y otras es mínima y aprender a usar una implementación hará que sea muy sencillo aprender a usar las demás.
Las más utilizadas son:
- MySQL: una se las más utilizadas. Es open source y está siempre en constante desarrollo. (La que utilizaremos en este curso)
- PostgreSQL: otra de las más utilizadas. Es muy popular en el mundo de la programación ruby on rails.
- SQL Oracle : es una de las más antiguas, no es open source y es de pago. Es muy utilizada en el mundo empresarial.
- MS SQL : muy utilizada en el mundo .NET. versión de SQL de Microsoft. También tiene un excelente soporte, pero no es gratis.
 -MariaDB: aplicaciones como Facebook utilizan esta implementación. Es open source, pero no está tan extendida como otras.

## WORKBENCH
> es una herramienta visual de diseño de bases de datos que integra desarrollo de software, administración de bases de datos, diseño de bases de datos, gestión y mantenimiento para el sistema de base de datos MySQL

## SQUEMA

Un esquema es un marco o plano para que los programadores construyan y codifiquen una base de datos. Puede ayudar al usuario de una base de datos a entender y conocer la información almacenada.

se basan en un conjunto de códigos y líneas que conforman la sintaxis del mismo. La sintaxis es un conjunto de reglas que estipula la manera en que se deben combinar de manera adecuada los elementos de un idioma.

sirve para agilizar el procesamiento de la información y facilitar el trabajo de los analistas de datos. al permitir que los datos agrupados y no agrupados de la base de datos se organicen en grupos, es decir, un esquema es un contenedor que permite agrupar los objetos y clasificarlos por nombre.

> Un esquema es una herramienta que podemos usar para incluir todas las tablas de nuestra base de datos. Un esquema es un espacio de trabajo para nuestra base de datos que nos permite agrupar todos nuestros datos. Una base de datos estará formada por todo tipo de tablas que se encuentran en diferentes lugares. Podemos almacenar datos relacionados con otras tablas en nuestro esquema. Es una forma en la que podemos definir dónde existen nuestras tablas y cómo se relacionan entre sí.


---
## DATATYPES

- CHARACTER CHAR(10) de longitud fija. van entre comillas
- VARCHAR VARCHAR(10) se indica el máximo. entre comillas
- BOOLEAN True or False values.
- SMALLINT como integer, desde -32768 hasta 32767. Sin decimales
- INTEGER INT  from -2147483647 to 2147483647 Decimals are truncated
- DECIMAL DECIMAL(4, 3) (DEFINIMOS ENTEROS Y DECIMALES) limite 38 digitos
- FLOAT tipos de datos que permiten guardar números muy grandes, de hasta 179 dígitos seguidos de 306 ceros.
- DATETIME objetos de fecha. 1968-10-23 1:45:37.123
- CLOB character large object. Up to 2GB
- BLOB objeto binario grande. cuando se desea almacenar una imagen real en la base de datos

--- 
## CLAVES FORANEAS Y PRIMARIAS
Las tablas se relacionan con otras tablas mediante una relación de clave primaria o de clave foránea. 
Las relaciones de claves primarias y foráneas se utilizan en las bases de datos relacionales para definir relaciones de muchos a uno entre tablas.

- Una clave primaria 
es una columna o un conjunto de columnas en una tabla cuyos valores identifican de forma exclusiva una fila de la tabla. Una base de datos relacional está diseñada para imponer la exclusividad de las claves primarias permitiendo que haya sólo una fila con un valor de clave primaria específico en una tabla.

- Claves foráneas
Una clave foránea es una columna o un conjunto de columnas en una tabla cuyos valores corresponden a los valores de la clave primaria de otra tabla. Para poder añadir una fila con un valor de clave foránea específico, debe existir una fila en la tabla relacionada con el mismo valor de clave primaria.
