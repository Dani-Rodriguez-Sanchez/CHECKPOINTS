# SCSS
es un preprocesador CSS

### SCSS vs CSS
CSS lo puede interpretar cualquier navegador, y SCSS tiene que ser procesado para que pueda ser convertido a CSS y ser leído

### variable SCSS
contiene código CSS, creado al inicio del proyecto. Se usa para acortar el código
$/ .elementos { background-color: $main-color; 

### SCSS Mixin
bloques de código reutilizables, dentro de ellos pueden contener variables, u otros mixins.
``` @mixin texto-resaltado{   font-size: 25px;   font-weight: bold;   border: 1px solid blue; }```

`.elemento{   @include texto-resaltado; }`

### Unidad fraccionaria (fr) 
significa que cada unidad se dividirá proporcionalmente al valor del (fr). Y es una opción al uso de tantos por ciento o de pixeles. Por ejemplo: .elementos { display: grid; grid-template-columns: 1fr 1fr 2fr; }  Significa que dentro del grid de tres elementos, los dos primeros son iguales en tamaño, y el tercero es el doble de cada uno de los anteriores

