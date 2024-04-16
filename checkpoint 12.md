## ¿Qué significa UML?
(Unified Modeling Lenguage), se mantiene casi sin cambios desde su creación en 1996. Estandariza el estilo y proceso de modelado. El modelo es una forma de mostrar visualmente el comportamiento y estructura del sistema. A través de diagramas, que describen:

-Estructura: clases, interfaces, paquetes, componentes, despliegues, etc.
-Comportamiento: actividades, secuencias, estados, etc.
	-Interacciones: colaboraciones, comunicaciones, etc

Es independiente del codigo del lenguaje
Es un lenguaje de modelado gráfico, para REPRESENTAR LA ESTRUCTURA DE UN SISTEMA Y SU COMPORTAMIENTO, e interacciones.

Parte de la idea de que un sistema se puede representar mediante un conjunto de objetos que interactúan entre si.

*Estos diagramas pueden ser estructurales y de comportamiento

## ¿Por qué utilizamos UML?
Por dos motivos:
Se crea para estandarizar el modelado, y HACERLO COMPRENSIBLE para todas las partes implicadas en la implementación de los proyectos, de esta manera, a través de un lenguaje visual común, se hace comprensible para desarrolladores y otro tipo de usuarios más relacionados con el negocio o el marketing.

Y además es recomendable realizar cuando se ha empezado a desarrollar (antes de escribir código), por ORGANIZACION, sobre todo en sistemas complejos (de estructura como de comportamiento)

## Nombra algunos diagramas estructurales.
Son los que modelan la forma en que se diseña un sistema, define clases, atributos y métodos 
(Class , deployment, y package)
-CLASS los más comunes. modela la estructura a través de clases, atributos, y métodos
-DEPLOYMENT(de implementacion), modela como se configura la arquitectura del sistema
para tener una vision general de como se conectan los componentes del sistema
-PACKAGE permite agrupar elementos, para visualizar dependencias y relaciones, para mejorar la eficiencia en el proceso.


## Nombra algunos diagramas de comportamiento.
Son diferentes de los estructurales, ya que representan como se comportan y relacionan los elementos del sistema
(activity, use case, state machine, y sequence)
*-ACTIVITY es el más simple, es como un boceto inicial. da un estado inicial, un final, estado de actividad(preguntas), flujo de accion(flechas) que indican el paso de un estado a otro, decisiones, y guards. Y swim lanes, con un quiz comun, es útil para saber los roles de cada actor del sistema.

-USER CASE muestra a lo q tiene acceso cada usuario, útil para diseñar el sistema de autorizaciones.

-STATE MACHINE muestra como se ven los datos y las acciones en cada estado del sistema, es antigua

*-SEQUENCE
el mas útil para los desarrolladores. Es el más complejo, muestra como se debe implementar y de como debe funcionar el código.
Su planteamiento es un sistema que envía mensajes interna o externamente. Poder visualizar cómo se ven esos mensajes es increíblemente importante.

##¿Qué es el enrutamiento RESTful
El ENRUTAMIENTO es el mecanismo por el cual las solicitudes se enrutan(dirigen) al código que las maneja. El enrutamiento RESTFUL es una CONVENCION  para definir rutas, a través de unos verbos.
Es una convención sobre como manejar las URL, Las rutas RESTful proporcionan un patrón de diseño que permite una fácil manipulación de datos.
Se basa en principios como la simplicidad y la interoperabilidad (capacidad de compartir de datos).
En la práctica, asocia unos verbos REST  a acciones HTTP. Estos son: post, get, put, patch y delete.
Se basa en el principio de economía, o navaja de Occam, que dice que cuando dos teorias en igualdad de condiciones tienen las mismas consecuencias, la mas simple es la más probable.
Ejemplo de verbos restful:
en una e-commerce, delete para eliminar registros o recursos, get para consultar un recurso, post para crearlo, patch actualiza,
