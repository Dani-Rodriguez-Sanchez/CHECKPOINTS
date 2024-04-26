# CHECKPOINT 13

### ¿Cuáles son las partes de un diagrama de clases?

NOMBRE, ATRIBUTOS, METODOS ó operaciones

1 nombre de la clase
2 atributo, son las características de la clase. el tipo de atributo va después de dos puntos (string, o int...). Pueden ser +(publicos) -(privados) #(protegidos)
3 metodos. Son las operaciones o comportamientos que esta clase puede realizar. seguidos de ()

### ¿Los diagramas de implementación son estructurales o de comportamiento?

DEPLOYMENT. Son estructurales. Definen la estructura del sistema. 

### ¿Qué es un diagrama de actividades?

ACTIVITY DIAGRAM. De comportamiento. Son útiles como boceto inicial, para tener un concepto de cómo desarrollar el sistema. Son útiles para usuarios no-téncicos.  Para comunicarse con claridad y brevedad.
Hay un estado inicial y otro final, y unos flujos de estado con branches, condiciones, etc

 muestra el flujo de actividades o acciones en un proceso o procedimiento. Se utiliza para modelar el comportamiento de un sistema, mostrando las acciones que se realizan y cómo se relacionan entre sí.

### ¿De qué manera el diseño del sistema ayuda al proceso de desarrollo?

Al ser una representación visual de los elementos del sistema. Es como dibujar unos planos o un mapa, para planificar como el sistema va a funcionar. Y como las partes del sistema van a interactuar
Permite una base sólida para la construcción del sitema, ya que permite la comprensión de todos lo miembros del equipo, y la identificación de problemas o conflictos antes de la implementación.

### ¿Por qué usaríamos un diagrama de implementación?

DEPLOYMENT DIAGRAM ilustra cómo la arquitectura de software, diseñada a nivel conceptual, se traduce en la arquitectura del sistema físico donde el software se ejecutará como nodos .
“Es representar como se traduciría el sistema de software en el mundo real.”
Tenemos una visión de como se distribuyen los elementos del sistema en nodos y como interactúan entre ellos. Se visualizan en cajas.
Se relacionan a través de enlaces y dependencias. Son servicios web, apis, bases de datos...
ayuda a identificar los recursos necesarios, las dependencias entre los componentes y las posibles limitaciones o restricciones de hardware.
La vista de implementación muestra el empaquetado físico de las partes reutilizables del sistema en unidades sustituibles, llamadas componentes. Una vista de implementación muestra los elementos físicos del sistema mediante componentes, así como sus interfases y dependencias entre componentes. Los componentes son piezas reutilizables de alto nivel a partir de las cuales se pueden construir los sistemas.

----
## TIPOS DE INTERACCIONES:

1 Herencia:
 El proceso por el cual un hijo o una subclase asume la funcionalidad de un padre o una superclase, también conocido como generalización. Está simbolizado con una línea recta conectada con una punta de flecha cerrada que apunta hacia la superclase.
2 Asociación bidireccional:
 La relación predeterminada entre dos clases. Ambas clases son conscientes la una de la otra y de su relación con la otra. Esta asociación está representada por una línea recta entre dos clases.

3 Asociación unidireccional:
 Una relación un poco menos común entre dos clases. Una clase es consciente de la otra e interactúa con ella

Asociación: Representa una conexión estructural y puede ser unidireccional o bidireccional. Por ejemplo, en un diagrama de clases de un sistema de ventas, puede haber una asociación entre las clases "Cliente" y "Producto", indicando que un cliente puede comprar varios productos.
Multiplicidad: Es una propiedad de una asociación que indica cuántos objetos de una clase están relacionados con un objeto de la otra clase. Se representa mediante un número o un rango de números. Por ejemplo, en una asociación entre las clases "Cliente" y "Producto", la multiplicidad puede indicar que un cliente puede comprar de 0 a muchos productos.
Navegabilidad: Es una propiedad de una asociación que indica si un objeto de una clase puede acceder directamente a los objetos de la otra clase a través de la asociación. Se representa mediante una flecha en el diagrama de clases. Por ejemplo, en una asociación entre las clases "Cliente" y "Producto", si la navegabilidad está presente en el lado del cliente, significa que un cliente puede acceder directamente a los productos que ha comprado.

### CLASS DIAGRAM (structural)

Los más comunes, se utilizan para modelar la estructura del sistema. Están compuestos por clases, y cada una de ellas tiene 3 elementos: nombre, atributos y metodos
-nombre o tema
-atributos. son las características de la clase. el tipo de atributo va después de dos puntos (string, o int...). Pueden ser +(publicos) -(privados) #(protegidos)
-metodos. Son las operaciones o comportamientos que esta clase puede realizar. seguidos de ()
*INTERACCIONES son las relaciones entre las clases. Pueden ser de herencia, bidireccional, o unidireccional.

### DEPLOYMENT (structural) o IMPLEMENTACIÓN

Ilustra como la arquitectura de software de un sistema se traduce en su forma en el mundo real del hardware. Tenemos una visión de como se distribuyen los elementos del sistema en nodos y como interactúan entre ellos. Se visualizan en cajas.
muestra los elementos físicos del sistema mediante componentes, así como sus interfases y dependencias entre componentes.
Son servicios web, apis, bases de datos...
ayuda a identificar los recursos necesarios, las dependencias entre los componentes y las posibles limitaciones o restricciones de hardware.

### PACKAGE DIAGRAM (structural)

Es una representación a muy alto nivel. Se puede utilizar para simplificar diagramas de clases complejos y puede agrupar clases en paquetes.
Permiten agrupar elementos de tal forma que se pueda visualizar de forma sencilla las dependencias entre los elementos y las relaciones que existen entre ellos.
Los paquetes aparecen como rectángulos con pequeñas pestañas en la parte superior. Unidos con flechas punteadas que son las dependencias.

### ACTIVITY DIAGRAM (behavioral)

Son útiles como boceto inicial, para tener un concepto de cómo desarrollar el sistema. Son útiles para usuarios no-téncicos.  Para comunicarse con claridad y brevedad.
Hay un estado inicial y otro final, y unos flujos de estado con branches, flujo de acción, condiciones, guardas, etc
Pueden tener swim lanes, que son carriles dentro de un quiz comun, para ver que rol tiene cada actor del sistema
 
### USE CASE DIAGRAM (behavioral)

permite mostrar todo aquello a lo que un usuario tiene acceso. Por ello, son muy útiles en aquellos casos en los que se quiera diseñar el sistema de autorización.
Las USE CASES son círculos que representan algun tipo de accion, como objetner información.
ACTORS, pueden ser humanos o tb un api, un blog, etc.
SUBSYSTEMS es un cuadrado rectangular, ayudan a organizar, ya que permite ver donde ocurren esas acciones.
RELATIONSHIPS son lineas intermitentes con flechas. Son la conexión entre los actores y los use cases.

### STATE MACHINE DIAGRAM (behavioral)

Sirven para mostrar cómo se ven los datos y las acciones de los mismos en diferentes estados a lo largo del ciclo de vida del sistema. Es una forma antigua de representar información.
Mientras que un diagrama de actividad muestra el comportamiento que puede tener un usuario, la state machine diagram muestra las acciones que pueden cambiar el estado del usuario

### SEQUENCE DIAGRAM (behavioral)

(el mas util para los desarrolladores)
es uno de los diagramas más complejos, muestra exactamente cómo debe implementarse el código. Importantes las lineas de vida y los mensajes

---
**TABLAS AUTOREFERENCIALES en este caso: un usuario que necesita poder seguir a otro usuario. ¿Pero cómo se hace un seguimiento de eso? Tener este tipo de mesa de unión es una excelente manera de hacerlo. Entonces, si tiene el Usuario A que quiere seguir al Usuario B, entonces lo que puede hacer es crear esta tabla de base de datos y poder decir, este siguiente usuario es donde almacenaremos la ID de quién está siendo seguido. Y luego tenemos seguidor. Entonces vamos a almacenar la identificación de usuario de la persona que realiza la siguiente acción. Y lo bueno de esto es que, debido a que tenemos esta referencia aquí mismo, y un usuario tiene muchos seguidores, y después tiene muchos usuarios, podemos ejecutar consultas limpias de la base de datos para realizar acciones, como poder representar una lista de todos los usuarios que un usuario está siguiendo.

**LOAD BALANCER 
(EQUILIBRADOR DE CARGA) Los sitios web modernos de alto tráfico deben atender cientos de miles, si no millones, de solicitudes simultáneas de usuarios o clientes y devolver el texto, las imágenes, el vídeo o los datos de la aplicación correctos,
Un equilibrador de carga actúa como el "policía de tráfico" sentado frente a sus servidores y enruta las solicitudes de los clientes a través de todos los servidores capaces de satisfacer esas solicitudes de una manera que maximiza la velocidad y la utilización de la capacidad y garantiza que ningún servidor esté sobrecargado, lo que podría degradar el rendimiento. . Si un solo servidor deja de funcionar, el equilibrador de carga redirige el tráfico a los servidores en línea restantes. Cuando se agrega un nuevo servidor al grupo de servidores, el equilibrador de carga comienza automáticamente a enviarle solicitudes.
De esta manera, un balanceador de carga realiza las siguientes funciones:
Distribuye las solicitudes de los clientes o la carga de la red de manera eficiente entre múltiples servidores. Garantiza alta disponibilidad y confiabilidad al enviar solicitudes solo a servidores que están en línea Proporciona la flexibilidad de agregar o quitar servidores según lo dicte la demanda.
Beneficios del equilibrio de carga Tiempo de inactividad reducido Escalable Redundancia Flexibilidad Eficiencia
