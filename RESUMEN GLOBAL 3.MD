# CHECKPOINT 12 UML

### Qué significa UML?
(Unified Modeling Lenguage) Estandariza el estilo y proceso de modelado. El modelo es una forma de mostrar visualmente el comportamiento y estructura del sistema. A través de diagramas, que describen:

- Estructura: clases, interfaces, paquetes, componentes, despliegues, etc. 
- Comportamiento: actividades, secuencias, estados, etc. 
- Interacciones: colaboraciones, comunicaciones, etc

Es independiente del codigo del lenguaje Es un lenguaje de modelado gráfico, para REPRESENTAR LA ESTRUCTURA DE UN SISTEMA Y SU COMPORTAMIENTO, e interacciones.

Parte de la idea de que un sistema se puede representar mediante un conjunto de objetos que interactúan entre si.

*Estos diagramas pueden ser estructurales y de comportamiento

### Por qué utilizamos UML?

Por dos motivos: Se crea para estandarizar el modelado, y HACERLO COMPRENSIBLE para todas las partes implicadas en la implementación de los proyectos, de esta manera, a través de un lenguaje visual común, se hace comprensible para desarrolladores y otro tipo de usuarios más relacionados con el negocio o el marketing.

Y además es recomendable realizar cuando se ha empezado a desarrollar (antes de escribir código), por ORGANIZACION, sobre todo en sistemas complejos (de estructura como de comportamiento)

### Nombra algunos diagramas ESTRUCTURALES.
Son los que modelan la forma en que se diseña un sistema, define clases, atributos y métodos (Class , deployment, y package) 

- CLASS los más comunes. modela la estructura a través de clases, atributos, y métodos. 
Los más comunes, se utilizan para modelar la estructura del sistema. Están compuestos por clases, y cada una de ellas tiene 3 elementos: nombre, atributos y metodos -nombre o tema -atributos.

- DEPLOYMENT(de implementacion), modela como se configura la arquitectura del sistema para tener una vision general de como se conectan los componentes del sistema. 
diseñada a nivel conceptual, se traduce en la arquitectura del sistema físico donde el software se ejecutará como nodos . “Es representar como se traduciría el sistema de software en el mundo real.”
Se visualizan en cajas. Se relacionan a través de ENLACES Y DEPENDENCIAS. Son servicios web, apis, bases de datos...

- PACKAGE permite agrupar elementos, para visualizar dependencias y relaciones, para mejorar la eficiencia en el proceso. 
Es una representación a muy alto nivel. Se puede utilizar para simplificar diagramas de clases complejos y puede agrupar clases en paquetes.

### Nombra algunos diagramas de COMPORTAMIENTO.
Son diferentes de los estructurales, ya que representan como se comportan y relacionan los elementos del sistema (activity, use case, state machine, y sequence) 

- ACTIVITY es el más simple, es como un boceto inicial. da un estado inicial, un final, estado de actividad(preguntas).
Son útiles para usuarios no-téncicos. Para comunicarse con claridad y brevedad. 
flujo de accion(flechas) que indican el paso de un estado a otro, decisiones, y guards. Y swim lanes, con un quiz comun, es útil para saber los roles de cada actor del sistema.

- USER CASE muestra a lo q tiene acceso cada usuario, útil para diseñar el sistema de autorizaciones.
permite mostrar todo aquello a lo que un usuario tiene acceso. Por ello, son muy útiles en aquellos casos en los que se quiera diseñar el sistema de autorización.

- STATE MACHINE muestra como se ven los datos y las acciones en cada estado del sistema. para mostrar cómo se ven los datos y las acciones de los mismos en diferentes estados a lo largo del ciclo de vida del sistema. Es una forma antigua de representar información. Mientras que un diagrama de actividad muestra el comportamiento que puede tener un usuario, la state machine diagram muestra las acciones que pueden cambiar el estado del usuario

- SEQUENCE el mas útil para los desarrolladores. Es el más complejo, muestra como se debe implementar y de como debe funcionar el código. Su planteamiento es un sistema que envía mensajes interna o externamente. Poder visualizar cómo se ven esos mensajes es increíblemente importante.

### ¿Qué es el enrutamiento RESTful
El ENRUTAMIENTO es el mecanismo por el cual las solicitudes se enrutan(dirigen) al código que las maneja. El enrutamiento RESTFUL es una CONVENCION para definir rutas, a través de unos verbos. Es una convención sobre como manejar las URL, Las rutas RESTful proporcionan un patrón de diseño que permite una fácil manipulación de datos. Se basa en principios como la simplicidad y la interoperabilidad (capacidad de compartir de datos). En la práctica, asocia unos verbos REST a acciones HTTP. Estos son: post, get, put, patch y delete. Se basa en el principio de economía, o navaja de Occam, que dice que cuando dos teorias en igualdad de condiciones tienen las mismas consecuencias, la mas simple es la más probable. Ejemplo de verbos restful: en una e-commerce, delete para eliminar registros o recursos, get para consultar un recurso, post para crearlo, patch actualiza,

---
# CHECKPOINT 13

### partes de un diagrama de clases?
NOMBRE, ATRIBUTOS, METODOS ó operaciones

- nombre de la clase
- atributo, son las características de la clase. el tipo de atributo va después de dos puntos (string, o int...). Pueden ser +(publicos) -(privados) #(protegidos)
- metodos. Son las operaciones o comportamientos que esta clase puede realizar. seguidos de ()

las INTERACCIONES las relacionan entre si. Herencia y asoc bidireccional y unidireccional

### De qué manera el diseño del sistema ayuda al proceso de desarrollo?
Al ser una representación visual de los elementos del sistema. Es como dibujar unos planos o un mapa, para planificar como el sistema va a funcionar. Y como las partes del sistema van a interactuar Permite una BASE SOLIDA para la construcción del sitema, ya que permite la COMPRENSION de todos lo miembros del equipo, y la identificación de PROBLEMAS o conflictos antes de la implementación.

### TIPOS DE INTERACCIONES:
- Herencia:  El proceso por el cual un hijo o una subclase asume la funcionalidad de un padre o una superclase, también conocido como generalización. Está simbolizado con una línea recta conectada con una punta de flecha cerrada que apunta hacia la superclase. 

- Asociación bidireccional:  La relación predeterminada entre dos clases. Ambas clases son conscientes la una de la otra y de su relación con la otra. Esta asociación está representada por una línea recta entre dos clases.

3 Asociación unidireccional:  Una relación un poco menos común entre dos clases. Una clase es consciente de la otra e interactúa con ella

### LOAD BALANCER (EQUILIBRADOR DE CARGA) 
Los sitios web modernos de alto tráfico deben atender cientos de miles, si no millones, de solicitudes simultáneas de usuarios o clientes y devolver el texto, las imágenes, el vídeo o los datos de la aplicación correctos, Un equilibrador de carga actúa como el "policía de tráfico" sentado frente a sus servidores y enruta las solicitudes de los clientes a través de todos los servidores capaces de satisfacer esas solicitudes de una manera que maximiza la velocidad y la utilización de la capacidad
