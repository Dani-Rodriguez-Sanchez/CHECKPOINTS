## ¿Cuáles son algunas de las cosas que hacen que SCSS sea diferente de CSS? (ponme ejemplos)

Por definición es preprocesador CSS. CSS lo puede interpretar cualquier navegador, y SCSS tiene que ser procesado para que pueda ser convertido a CSS y ser leído. 
La utilidad de la sintaxis SCSS es dar una funcionalidad extra dentro de CSS, que es útil para eliminar procesos repetitivos(como manera de limpiar y agilizar el código), 
y además de reutilizar el código, da la posibilidad de compartirlo entre varios proyectos.

/en CSS tendríamos que escribir las propiedades cada vez que queramos definir los elementos/
```
body{ width: 800px; color: #ffffff; } body content{ width:750px; background:#ffffff; }

/*y con SCSS podríamos reutilizar las propiedades $color: #ffffff; $width: 800px;

content{ width: $width; background:$color; }
```
## ¿Qué es una variable SCSS? (porque crees que debes utilizarla pon un ejemplo de una variable, escribe una variable y como se pondría para utilizarla)

Una variable contiene código CSS, creado al inicio del proyecto, y puede ser llamado desde cualquier parte de este. 
Se debe utilizar para acortar el código, siendo de esta manera más optimizado. Por ejemplo: `/se define con el carácter $/ $main-color: #ffffff;`

/se llama con el mismo carácter $/ .elementos { background-color: $main-color; } /*
de esta manera, main-color puede ser reutilizado todas las veces que queramos dentro del código, sin necesidad de escribir el color, 
además, cualquier modificación en la definición, se trasladaría a los llamados.

## ¿Qué es un SCSS Mixin? (porque crees que debes utilizarla pon un ejemplo de una variable, escribe una variable y como se pondría para utilizarla) 
Son bloques de código reutilizables, dentro de ellos pueden contener variables, u otros mixins. Dan la posibilidad de incluir argumentos o valores predeterminados 
(que se pueden adaptar cada vez que se utilice el mixin). Es la mayor manera de aprovechar la funcionalidad de SCSS, ya que optimiza el tamaño del código. 
La sintaxis es @mixin para crearlo, y @include para llamarlo. Por ejemplo:
```
@mixin texto-resaltado{   font-size: 25px;   font-weight: bold;   border: 1px solid blue; }

.elemento{   @include texto-resaltado; }
```
En mi opinión utilizar mixin con valores predeterminados es muy interesante, porque nos permite reducir código, con la versatilidad de poder apartarlos a nuestras necesidades concretas en ese punto.

## ¿Qué significa Unidad fraccionaria (fr) con CSS Grid? Se utiliza para la ordenación de los elementos en las filas y columnas dentro de los CSS Grid, 
significa que cada unidad se dividirá proporcionalmente al valor del (fr). Y es una opción al uso de tantos por ciento o de pixeles.
Por ejemplo: 
`.elementos { display: grid; grid-template-columns: 1fr 1fr 2fr; } `
Significa que dentro del grid de tres elementos, los dos primeros son iguales en tamaño, y el tercero es el doble de cada uno de los anteriores
