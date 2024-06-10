## METODO HANDLER

## REFS Y DOM
sobre la manera en que REACT se relaciona con el DOM: react trabaja con un Dom virutal, pero hay veces que necesitamos interactuar directamente con el DOM y eso es lo que hacen los REFS
lo hemos utilizado para poder borrar los archivos tan pronto como se hayan cargado exitosamente. es útil para trabajar con bibliotecas de terceros.

## DROPZONE
el dropzone component es una libreria de javascript, q se instala como componente. 
Es una ZONA DE ARRASTAR Y SOLTAR.


## Qué significa CRUD?

CRUD (Create, Read, Update, and Delete)
para muchas aplicaciones, es el conjunto completo de funcionalidad, significa crear, leer, actualizar y eliminar.
En REACT se puede aplicar para el manejo de datos en la API o localmente.

los métodos HTTP (POST, GET, PUT y DELETE) se corresponden a las operaciones CRUD
CONJUNTO DE OPERACIONES DE CRUD que son las siguientes:
- Crear: crear una publicación o agregar la fila de la tabla, agregar datos a la página web o crear contenido.  CREATEUSER POR EJEMPLO. EN HTTP POST
- Leer: leer o recuperar datos de una página web. EN HTTP GET
- Actualización: actualizar o editar contenido existente en la página web EN HTTP PUT
- Eliminar: eliminar y eliminar la entrada o contenido/publicación de la página web EN HTTP DELETE

## ¿Qué es un operador ternario?
en javascript es un operador con TRES OPERANDOS 
se usa para condensar una expresión de if/else mucho más larga en menos código y más compacta.
condición ? valor verdadero : valor falso;

Si la condición es true, el operador retorna el valor de la valorverdadero; de lo contrario, devuelve el valor de valorfalso

En el módulo lo hemos utilizado en ...

## ¿Qué tipo de solicitud API hacemos cuando queremos eliminar datos?
DELETE

## ¿Qué tipo de solicitud de API hacemos cuando queremos actualizar datos?
PUT Reemplaza todo el recurso con la versión actualizada completamente.
PATCH cuando necesita actualizar sólo una parte de un recurso en lugar de todo el recurso. Este método le permite enviar un conjunto de instrucciones al servidor, indicando los cambios que se deben realizar en el recurso.

## ¿Qué es el código dinámico?
Es un código que responde a las intereacciones con el usuario.
 dos flujos de trabajo por ejemplo a partir de una condicion


## ¿cuál es un caso de uso común para poder pasar un componente secundario a un componente principal? 
(modificar el contenido de una dropzone por ejemplo)
