## METODO HANDLER
event handling: controladores de eventos. determinan qué acción ocurrirá cada vez que se active un evento. Esto podría ser un clic en un botón o un cambio en una entrada de texto. hacen posible que los usuarios interactúen con su aplicación React

## REFS Y DOM
sobre la manera en que REACT se relaciona con el DOM: react trabaja con un Dom virutal, pero hay veces que necesitamos interactuar directamente con el DOM y eso es lo que hacen los REFS
lo hemos utilizado para poder borrar los archivos tan pronto como se hayan cargado exitosamente. es útil para trabajar con bibliotecas de terceros.
para utilizar en casos que no podamos solucionar con props, state y funciones.
permite acceder a los elementos del DOM o a los elementos react creados en el método render.

## DROPZONE
el dropzone component es una libreria de javascript, q se instala como componente. 
permite la creación sencilla de funciones de ARRASTAR Y SOLTAR en una ZONA, dentro de una aplicación React.

Simplifica la experiencia de carga de archivos del usuario, permitiéndole arrastrar archivos desde su explorador de archivos y soltarlos en la aplicación para cargarlos inmediatamente.
Es ideal para cualquier aplicación que implique la carga de archivos

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
en javascript es un operador CONDICIONAL con TRES ELEMENTOS
se usa para condensar una expresión de if/else mucho más larga en menos código y más compacta.
condición ? valor verdadero : valor falso;

Si la condición es true, el operador retorna el valor de la valorverdadero; de lo contrario, devuelve el valor de valorfalso

En el módulo lo hemos utilizado en construir una función condicional.

## ¿Qué tipo de solicitud API hacemos cuando queremos eliminar datos?
DELETE
axios.delete(`https://api.devcamp.space/portfolio/portfolio_items/${portfolioItem.id}`,
    { withCredentials: true }
  )

## ¿Qué tipo de solicitud de API hacemos cuando queremos actualizar datos?
PUT Reemplaza todo el recurso con la versión actualizada completamente.
PATCH cuando necesita actualizar sólo una parte de un recurso en lugar de todo el recurso. Este método le permite enviar un conjunto de instrucciones al servidor, indicando los cambios que se deben realizar en el recurso.

## ¿Qué es el código dinámico?
Es un código que responde a las intereacciones con el usuario o de los datos api. mejora la experiencia del usuario y haciendo que las aplicaciones sean más intuitivas y fáciles de usar.

 dos flujos de trabajo por ejemplo a partir de una condicion. 
por ejemplo, en un formulario, si los datos introducidos son incorrectos, lanza un mensaje de error


## ¿cuál es un caso de uso común para poder pasar un componente secundario a un componente principal? 
(modificar el contenido de una dropzone por ejemplo)

## INPUT VS TEXTAREA:
Los input de tipo radio y textarea en React son dos tipos de datos que podemos permitirle al usuario insertar en un formulario. TEXTAREA permite formato multiliniea, mientas que INPUT no

## HOOKS
(ganchos)
permiten que los componentes de funciones tengan acceso al estado y otras características de React. Debido a esto, los componentes de clase generalmente ya no son necesarios.
por ejemplo USESTATE que nos da un estado inicial, para después con una funcion poder actualizarlo. durante el ciclo de vida de la funcion
