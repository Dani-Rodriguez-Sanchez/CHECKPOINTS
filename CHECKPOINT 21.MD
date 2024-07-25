

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

1- Cómo utilizar alias para columnas
Para asignar un alias a una columna en MySQL, simplemente se utiliza la palabra clave AS seguida del nombre del alias después del nombre de la columna. Aquí tienes un ejemplo básico:

> SELECT nombre AS primer_nombre FROM usuarios;
En este caso, la columna nombre se mostrará como primer_nombre en los resultados de la consulta. Es una forma efectiva de hacer que los resultados sean más intuitivos. Por ejemplo, si tienes una columna que se llama fecha_nacimiento, podrías renombrarla temporalmente como fecha_de_nacimiento para que sea más descriptivo.

2 - Utilizando alias para tablas
Asignar un alias a una tabla sigue una lógica similar. Esto se vuelve extremadamente útil cuando se trabaja con múltiples tablas en una consulta, especialmente si las tablas tienen nombres largos o si se requiere hacer múltiples referencias a la misma tabla. Aquí está la sintaxis básica:

> SELECT u.nombre FROM usuarios AS u;
En este ejemplo, la tabla usuarios se ha aliasado como u, lo que simplifica las referencias posteriores en la consulta. Este método no solo acorta el texto de la consulta, sino que también aclara las relaciones entre varias tablas.

---

## INNER JOINS VS OUTER JOINS
