## CRA VS VITE

- Create React App. 
abreviado como CRA, es una herramienta desarrollada por Facebook para ayudar a los desarrolladores a configurar un proyecto de React 
desde cero de manera rápida y sencilla. CRA ofrece una configuración predefinida que es adecuada para la mayoría de los proyectos de React.
Esto significa que puedes comenzar a codificar de inmediato sin tener que preocuparte por las configuraciones iniciales.

- VITE. es una herramienta más reciente que ha ganado popularidad rápidamente en el mundo del desarrollo web con React. 
Desarrollada por Evan You, el creador de Vue.js, Vite promete una experiencia de desarrollo aún más rápida y eficiente que CRA.
Vite es conocido por su velocidad de desarrollo sobresaliente. Utiliza la compilación en tiempo real y el reemplazo de módulos (module replacement) 
para proporcionar una experiencia de desarrollo prácticamente instantánea.

DIFERENCIAS:
* Velocidad de desarrollo: con vite Gracias a su enfoque en el reemplazo de módulos y la compilación en tiempo real, los cambios se reflejan de inmediato en la aplicación. En cambio, Create React App, aunque ofrece una velocidad de desarrollo decente, no puede igualar la velocidad de Vite debido a su enfoque más tradicional.
* Configuración: Create React App brinda una configuración predeterminada que es fácil de usar para proyectos estándar de React. Sin embargo, si necesitas realizar configuraciones personalizadas específicas, puede requerir un poco más de esfuerzo y comprensión de las configuraciones de Webpack. Por otro lado, Vite destaca por su configuración mínima y su enfoque basado en estándares como ESM.
* Compatibilidad con proyectos existentes: si estás trabajando en un proyecto de React existente, Create React App puede ser una opción más cómoda, ya que está diseñado para ser compatible con proyectos ya en marcha. Puedes migrar tu proyecto a CRA sin demasiados problemas y continuar trabajando en él. En contraste, Vite está más orientado a proyectos nuevos. Si bien es posible migrar proyectos existentes a Vite, puede requerir un poco más de trabajo.
* Comunidad y ecosistema: Create React App ha existido durante más tiempo y tiene una comunidad establecida. Esto significa que puedes encontrar una gran cantidad de recursos, documentación y complementos desarrollados por la comunidad para ayudarte en tu proyecto. Vite, aunque más nuevo, también ha crecido rápidamente y tiene una comunidad en crecimiento.

ENTONCES: 
- Si buscas la máxima velocidad de desarrollo y estás dispuesto a aprender una nueva forma de trabajar, Vite es una excelente elección.

- Si estás trabajando en un proyecto existente de React o prefieres una configuración más tradicional, Create React App sigue siendo una opción sólida. Ten en cuenta que, si estás empezando con React y deseas una introducción suave al desarrollo web, Create React App

---
## REACT NATIVE
React Native, es un framework de código abierto creado por Meta Platforms, Inc.​ Se utiliza para desarrollar aplicaciones para Android, ​ Android TV, ​ iOS, macOS, ​ tvOS, Web, ​ Windows​ y UWP​ al permitir que los desarrolladores usen React con las características nativas de estas plataformas.

React Native usa el mismo paradigma fundamental de construcción de bloques de UI (componentes visuales con los que interacciona el usuario) que las aplicaciones nativas reales de Android e iOS, pero gestiona la interacción entre los mismos utilizando las capacidades de JavaScript y React.

https://www2.deloitte.com/es/es/pages/technology/articles/que-es-react-native.html
---
## REACT ANIMATE HEIGHT
https://www.npmjs.com/package/react-animate-height

> Componente React sin dependencias para animar la altura mediante transiciones CSS. Deslice un elemento hacia arriba y hacia abajo o anímelo a una altura específica. La opacidad del contenido también se puede animar de forma opcional (consulte animateOpacityla propiedad a continuación).
QUICK START:

Get it from npm

`$ npm install --save react-animate-height`

Import and use it in your React app.
```
import React, { useState } from 'react';
import AnimateHeight from 'react-animate-height';

const Example = () => {
  const [height, setHeight] = useState(0);

  return (
    <div>
      <button
        aria-expanded={height !== 0}
        aria-controls="example-panel"
        onClick={() => setHeight(height === 0 ? 'auto' : 0)}
      >
        {height === 0 ? 'Open' : 'Close'}
      </button>

      <AnimateHeight
        id="example-panel"
        duration={500}
        height={height} // see props documentation below
      >
        <h1>Your content goes here</h1>
        <p>Put as many React or HTML components here.</p>
      </AnimateHeight>
    </div>
  );
};
```
### GIT DIFF
sirve para Mostrar cambios entre el árbol de trabajo y el índice o un árbol, cambios entre el índice y un árbol, cambios entre dos árboles, cambios resultantes de una fusión, cambios entre dos objetos blob o cambios entre dos archivos en el disco.
En suma, da una vista más detallada de los cambios.

git diff es un comando multiusos de Git que, cuando se ejecuta, lleva a cabo una función para establecer las diferencias en los orígenes de datos de Git. Dichos orígenes de datos pueden ser confirmaciones, ramas y archivos, entre otras posibilidades. 

Gracias a este comando, no solo obtienes una visión general de tu repositorio, sino que además puedes identificar más rápidamente las fuentes de errores en el código en caso de problemas. La sintaxis de git diff es siempre la misma. El comando tiene el siguiente aspecto:
`git diff`

ejemplo:
https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/git-diff/

### INTERFACES

Básicamente, se trata de un lugar donde declaras todas tus variables antes de usarlas en el archivo real.
---
## JavaScript String substring()

https://www.w3schools.com/jsref/jsref_substring.asp
Muchos lenguajes han eliminado eso porque a veces es bastante innecesario, excepto para operaciones de gran escala que intentan desarrollar bibliotecas como esta.
