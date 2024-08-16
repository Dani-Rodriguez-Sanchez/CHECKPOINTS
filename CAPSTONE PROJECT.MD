# PLANIFICACION 

## OBJETIVOS GENERALES

- CLIENTE. Se trata de un pequeño negocio, un albergue en el camino De Santiago
- NECESIDADES. Necesita una web, de uso sencillo, a través de la cual pueda darse a conocer, y sus futuros clientes peregrinos puedan interactuar con el.

- ESPECIFICAMENTE. Se trataría de un espacio donde se daría información atractiva como los servicios del albergue:
  * Ubicación
  * Servicios
  * Galería de imágenes
  * Información útil del entorno
  * predicción meteorológica
  Además de elementos donde el usuario interacciona, como:
  * Formulario de registro/reserva
  * guest book donde pueden dejar sus reseñas/Intagram

-NECESIDADES
  * FRONT-END JAVASCRIPT, REACT, HTML, CSS
  * BACK-END JAVASCRIPT, MONGODB, REACT, JSON, AXIOS
---
## MARKETING 

### OBJETIVOS DE EXPERIENCIA DE USUARIO
Debido a la naturaleza de público al que va dirigido, que son peregrinos que buscan información sobre lugares donde alojarse en sus teléfonos móviles, es importante que la web sera totalmente responsible web design.
La pestaña de "booking" quedará flotando sobre todo el scroll de la página, y la opción de cambiar de idioma será bastante visible.
Por otra parte, se incorpora incrustado nuestra cuenta de instagram, donde podrán ver imágenes y comentarios del negocio.

### OBJETIVOS DE CONTENIDO
Se da importancia a la información útil para el cliente, y por lo tanto, se detallan los servicios que van a encontrar en el establecimiento, donde estamos, la previsión meteorológica, experiencias de otros usuarios en instagram, y lo más importante: como pueden reservar.

### OBJETIVOS DE CONVERSION
Se trata de convertir a los observadores de la web, en clientes. Así que es importante que la experiencia de usuario sea cómoda y atractiva, para que eligan el negocio como su lugar de descanso entre etapas.

### OBJETIVOS DE FIDELIZACION
El cliente potencial tiene una experiencia puntual, ya que la necesidad de alojarse es temporal, por eso, mediante las redes sociales, se invita a que nos incluya en sus contactos, y se nos etiquete en publicaciones, de cara a conseguir visibilidad, y que el propio cliente repita su visita en posteriores viajes.

---
## PLANIFICACION

### USER EXPERIENCE (UX)
Debido a la alta posibilidad de que los usuario utilicen el teléfono móvil, es primordial la facilidad de uso, por lo cual prescindimos de submenus, y toda la información útil está al alcance. 
La información de localización, servicios, y contacto se mostrará mediante pop-ups. El cambio de idioma con un simple botón, y el booking con un botón visible que trasladará al servicio de reservas.

### USER INTERFACE (UI)
Se diseña la web basada en un SCROLL, basado en dos mitades, en la `upper page` encontramos una `navbar` con información útil, el logo del negocio en tamaño adecuado, y a su izquierda, donde nos llevaría la vista, un elemento fijo con enlace a la página de reservas.
Con este elemento fijo, bajaríamos a la `lower page`, y ahí tendríamos un elemento con la predicción meteorológica, y de manera incrustada nuesro instagram. Finalmente, en la parte inferior, un pie de página con los mismos elementos que en el `navbar`


![landing_page_draft](https://github.com/user-attachments/assets/6286c4f7-695f-4aea-b95a-1144e1263eb2)

## USE CASE DIAGRAM

![ACTIVITY DIAGRAM](https://github.com/user-attachments/assets/9a1f55ea-ee36-4099-bde9-aa78ea8b0ecf)

## DEPENDENCIAS

- MULTI IDIOMAS
https://www.npmjs.com/package/react-multi-lang

- BOOKING
https://www.npmjs.com/package/booking_calendar

- EL TIEMPO
https://www.npmjs.com/package/react-open-weather?activeTab=readme

- CONTACTO POR MAIL
https://www.npmjs.com/package/nodemailer

- GUESTBOOK (he pensado que sería más actual insertar una cuenta de intagram)
https://www.npmjs.com/package/react-insta-stories


---
## DESARROLLO EN TIEMPO

- 01/08 Desarrollo Idea del proyecto
- 05/08 Aprobación Idea
- 06/08 Esquema web/ estudiar páginas similares
- 07/08 Esquema carpetas/ router
- 09/08 Abandono router, y elijo diseño en scroll
- 10/08 scroll landing page/boton retorno/css para responsibe en navbar/subida a github
https://www.youtube.com/watch?v=oszUqCqTGHo&t=719s
- 12/08 modulo cambio idioma
https://react.i18next.com/legacy-v9/step-by-step-guide
 modulo boton whatsapp
https://www.npmjs.com/package/react-floating-whatsapp
- 13/08
seccion presentacion. problema bordes blancos css
https://stackoverflow.com/questions/75582308/weird-white-line-on-react-page
- 14/08 seccion localizacion
https://docs.maptiler.com/react/
alternativa a google maps, con api gratuita
- 16/08 seccion servicios- iconos con modals (multiples) reutilizables
https://www.youtube.com/watch?v=yYMRuqTIkmM
-17/08 contacto/mail
https://medium.com/swlh/create-an-enquiry-form-in-react-and-send-email-using-nodejs-1c0cd590dce1
---

- What is your project title?
Albergue Las Garzas / Las Garzas Hostel

- What is the problem you are trying to solve with your application? 
Me he puesto en el papel de un developer que recibe un encargo para solucionar una necesidad de un cliente: este necesita un webspace, donde peregrinos que están haciendo el camino de santiago por España, antes de pasar por el hostel, puedan ver lo que ofrece, y de una manera cómoda, puedan reservar una cama a través de whatssapp, o de un email. 
Entonces, el problema a solucionar, es realizar una web lo bastante cómoda como para usar en el móvil mientras se va caminando, y a la vez atractiva, para conseguir que el cliente potencial que entre a ella, reserve.

- Who is your intended end-user for your web application? 
El cliente de la aplicacion es el propietario del hostel, y el intended end-user, son los clientes potenciales, peregrinos que hayan visto el anuncio, entren a la web, y ahí puedan decidir para una noche en el establecimiento.

- What applications and languages do you expect to employ in your design?
La estructura de la aplicación la desarrollo con REACT, lenguaje JAVASCRIPT, para algunas funciones necesitaré módulos NPM.
Para el FRONTEND necesitaré además HTML y CSS.
Y para el BACKEND AXIOS, MONGODB, y JSON

- What is your predicted timeline and milestones to complete your build?
He previsto un tiempo de desarrollo máximo de un mes:

   1. los primeros días los he dedicado al desarrollo de la idea de proyecto, y a revisar webs similares para identificar las necesidades del cliente.
   2. después de la aprobación del proyecto, comienzo con la estructura, que me llevará unos días, y espero que antes de terminar la semana, comenzar en el     
      FRONTEND, que me llevará entre una semana y 10 días.
   3. sobre la mitad del mes, empiezo con el BACKEND, el cual me llevará una semana aproximadamente.
   4. Y al final, haré el deployment con HEROKU o RENDER
 
---

- What is your project title?
Albergue Las Garzas / Las Garzas Hostel

- What is the problem you are trying to solve with your application? 
I have put myself in the role of a developer who receives an assignment to solve a client's need: he needs a webspace, where pilgrims who are doing the Camino de Santiago through Spain, before stopping by the hostel, can see what it offers. , and in a comfortable way, you can reserve a bed through WhatsApp, or an email. 
So, the problem to solve is to make a website that is comfortable enough to use on a mobile phone while walking, and at the same time attractive, to get the potential client who enters it to book.

- Who is your intended end-user for your web application? 
The client of the application is the owner of the hostel, and the intended end-user are the potential clients, pilgrims who have seen the advertisement, go to the website, and there they can decide for a night in the establishment.

- What applications and languages do you expect to employ in your design?
The structure of the application was developed with REACT, JAVASCRIPT language, for some functions I will need NPM modules.
For the FRONTEND I will also need HTML and CSS.
And for the BACKEND AXIOS, MONGODB, and JSON

- What is your predicted timeline and milestones to complete your build?
I have planned a maximum development time of one month:

   1. I have dedicated the first days to developing the project idea, and reviewing similar websites to identify the client's needs.
   2. After the approval of the project, I start with the structure, which will take me a few days, and I hope that before the end of the week, I will start on 
     the FRONTEND, which will take me between a week and 10 days.
   3. About halfway through the month, I start with the BACKEND, which will take me approximately a week.
   4. And at the end, I will do the deployment with HEROKU or RENDER
