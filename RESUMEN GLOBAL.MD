# SCSS
es un preprocesador CSS
### SCSS vs CSS
CSS lo puede interpretar cualquier navegador, y SCSS tiene que ser procesado para que pueda ser convertido a CSS y ser leído
### variable SCSS
contiene código CSS, creado al inicio del proyecto. Se usa para acortar el código
$/ .elementos { background-color: $main-color; 
### SCSS Mixin
bloques de código reutilizables, dentro de ellos pueden contener variables, u otros mixins.
' @mixin texto-resaltado{   font-size: 25px;   font-weight: bold;   border: 1px solid blue; }'

'.elemento{   @include texto-resaltado; }'
