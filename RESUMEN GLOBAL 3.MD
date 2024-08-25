# CHECKPOINT 11

### ¿Por qué usamos ramas de git?
Las ramas le permiten trabajar en diferentes partes de un proyecto sin afectar la rama principal, 
es una bifurcación para crear un nuevo camino en la que probar una funcionalidad previamente a incluirla en el código principal.
Cuando se completa el trabajo, se puede fusionar una rama con el proyecto principal. 
Incluso puedes cambiar entre ramas y trabajar en diferentes proyectos sin que interfieran entre sí. 
permite crear nuevas ramas de un proyecto para probar ideas, aislar nuevas características, o experimentar sin impactar al proyecto principal.

Podemos ver las ramas con: 
git branch
Y creamos con:
git checkout -b (nombre)

### comando para crear un repositorio git?
git add
se creará un nuevo subdirectorio .git en tu directorio de trabajo actual. También se creará una nueva rama principal.
Lo más lógico sería crear un directorio donde crearlo, con cd..., y estando ahí dentro git init

### ¿Qué es un conflicto de fusión?
suceden cuando fusionas ramas que tienen confirmaciones de cambios contrapuestas, 
y Git necesita tu ayuda para decidir qué cambios incorporar en la fusión final.

### Git branch
muestra todas las ramas, y en que rama nos encontramos, con un asterisco al lado.
Puede servir para renombrar una rama

### Git push y git pull
git push sirve para empujar el commit, es decir, pasar de una rama local en el ordenador a un repositorio remoto. 
El comando es git add. Con git status vemos los 
Git pull es lo contrario: descargar las modificaciones en nuestro ordenador en local.

### Pull vs fetch. 
Git fetch copia los cambios al repositorio local, mientras que pull los copia directamente al directorio de trabajo. 
Es una unión de git merge y git fetch

### Git merge 
sirve para volver a unir una rama bifurcada

### git checkout
permite navegar entre ramas

### commit
realiza una foto de los cambios hasta ese momento, a través de los commit, que son confirmaciones , como hitos dentro del proyecto. Estos commit se realizan en local(no interactuan en remoto hasta que se lo digamos)
*Identifica los cambios hechos en un entorno de trabajo. Luego con git push, los podemos trasladar al repositorio global o remoto.
Git commit -m (añadimos un mensaje con info sobre que se ha cambiado y por que).


