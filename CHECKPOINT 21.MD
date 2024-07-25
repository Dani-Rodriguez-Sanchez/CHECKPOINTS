

## CRUD

## Foreign Key

## RANGOS

## Wildcard Search

## SUBCONSULTAS

## AGGREGATE FUNCTIONS

## CONTROL FLOW
---
#### ALIASES AS

¿Qué son los **alias** en MySQL?

Un alias es un nombre temporal que se asigna a una tabla o columna en una consulta SQL. Estos no afectan el nombre de la tabla o columna en la base de datos; su propósito es facilitar la escritura de la consulta y mejorar la legibilidad del resultado. Los alias son particularmente útiles en consultas complejas que involucran múltiples tablas y columnas con nombres largos o poco claros.

El uso de alias en MySQL es una habilidad esencial que todos los desarrolladores de bases de datos deberían dominar. Facilita tanto la escritura como la lectura de consultas SQL, haciendo que el manejo de datos sea más eficiente y menos propenso a errores.


1- Cómo utilizar alias para columnas
Para asignar un alias a una columna en MySQL, simplemente se utiliza la palabra clave AS seguida del nombre del alias después del nombre de la columna. Aquí tienes un ejemplo básico:

> SELECT nombre AS primer_nombre FROM usuarios;
En este caso, la columna nombre se mostrará como primer_nombre en los resultados de la consulta. Es una forma efectiva de hacer que los resultados sean más intuitivos. Por ejemplo, si tienes una columna que se llama fecha_nacimiento, podrías renombrarla temporalmente como fecha_de_nacimiento para que sea más descriptivo.

2 - Utilizando alias para tablas
Asignar un alias a una tabla sigue una lógica similar. Esto se vuelve extremadamente útil cuando se trabaja con múltiples tablas en una consulta, especialmente si las tablas tienen nombres largos o si se requiere hacer múltiples referencias a la misma tabla. Aquí está la sintaxis básica:

> SELECT u.nombre FROM usuarios AS u;
En este ejemplo, la tabla usuarios se ha aliasado como u, lo que simplifica las referencias posteriores en la consulta. Este método no solo acorta el texto de la consulta, sino que también aclara las relaciones entre varias tablas.
---
#### Beneficios de usar alias en MySQL

1- Mejora la legibilidad del código
El uso de alias hace que tus consultas SQL sean más legibles y fáciles de entender, especialmente para alguien que no esté familiarizado con la base de datos. Verdaderamente, una consulta bien escrita sirve como parte de la documentación del sistema.

2- Simplifica las consultas complejas
Cuando se trabaja con múltiples tablas o se realizan operaciones de unión, los alias son indispensables para mantener las consultas organizadas y comprensibles. Esto es esencial para evitar errores y para hacer el análisis de los datos más accesible.

3- Facilita el mantenimiento del código
Un código más claro significa un mantenimiento más fácil. Al usar alias, te aseguras de que cualquier persona que modifique la consulta en el futuro pueda entender rápidamente su propósito y estructura sin necesidad de buscar detalles de cada tabla o columna.

---
#### Ejemplos avanzados de uso de alias
Alias en consultas con JOIN
Supongamos que deseas unir dos tablas, usuarios y pedidos, para obtener una lista de usuarios y los pedidos que han realizado. Aquí está cómo los alias pueden limpiar esta consulta:
```
SELECT u.nombre_usuario, p.fecha_pedido
FROM usuarios AS u
JOIN pedidos AS p ON u.id_usuario = p.id_usuario;
```

#### Alias en funciones y agrupaciones
Los alias también son útiles cuando se utilizan funciones de agregación. Por ejemplo, si deseas contar el número de pedidos por usuario, podrías escribir algo como esto:
```
SELECT u.nombre_usuario, COUNT(p.id_pedido) AS total_pedidos
FROM usuarios AS u
JOIN pedidos AS p ON u.id_usuario = p.id_usuario
GROUP BY u.nombre_usuario;
```
Como ves, los alias u y p ayudan a simplificar la consulta, mientras que el alias total_pedidos hace que el resultado sea mucho más claro.

---

## INNER JOINS VS OUTER JOINS

---
## NORMALIZACION BASES DE DATOS

---
## diagramas EER en SQL
