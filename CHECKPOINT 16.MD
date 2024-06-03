## ¿Por qué utilizamos Route Guards?

Se usa para restringir el acceso de usuarios no autenticados a ciertas partes de su aplicación, configurandolo para acceder solo a ciertas rutas.
Funciona como una barrera, que solo permite el acceso a los usuario autentificados.
Esto se configura a través del componente ROUTER

## ROUTER

Se usa porque REACT por si solo no permite el enrutamiento. Es un componente, y hay que agregarlo asi:
`npm i -D react-router-dom`
necesita una estructura de carpetas, y luego a través de una función:

- Primero envolvemos nuestro contenido con <BrowserRouter>.
- Luego definimos nuestro <Routes>  (se pueden anidar)

```
export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Layout />}>
          <Route index element={<Home />} />
          <Route path="blogs" element={<Blogs />} />
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NoPage />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}
```

## ¿Qué es una solicitud POST?

en REACT lo estamos usando como metodo HTTP.
Es lo opuesto a GET, este envia información, y no necesita THEN como Get
se usa para ENVIAR datos a la API.

Es asíncrona, lo que significa que hay dos momentos cruciales en la ejecución: el momento en el que inicias la llamada y el momento en que recibes una respuesta (o un tiempo de espera).

En el módulo lo hemos usado para crear nuevos items en el portfolio 

## ¿Cuáles son algunas cosas que puede hacer para prepararse para las entrevistas de trabajo?

## HIGH ORDER COMPONENT

un componente de orden superior es una función que toma un componente y devuelve un nuevo componente. 
permiten reutilizar la lógica de los componentes en varios componentes.
En React, un componente de orden superior es una función que toma un componente como argumento y devuelve un nuevo componente que envuelve el componente original.
pueden aceptar argumentos adicionales, lo que le permite personalizar el comportamiento del HOC. Esto los convierte en una forma flexible y reutilizable de agregar funcionalidad a sus componentes.

El componente empaquetado recibe todos los accesorios del contenedor, junto con un nuevo accesorio, dataque utiliza para representar su salida. Al HOC no le preocupa cómo o por qué se utilizan los datos, y al componente empaquetado no le preocupa de dónde provienen los datos.
Es una técnica avanzada en React para reutilizar la lógica de componentes. Los HOC no son parte de la API de React, per se. Son un patrón que surge de la naturaleza compositiva de React.

## SYNTHETIC EVENTS

En un sitio web HTML normal, tenemos lo que se llama DOM, es el Modelo de Objetos de Documento.

pero en React, tenemos lo que se llama DOM virtual, lo que significa que no estamos interactuando con el DOM como lo haría con un sitio web HTML normal, y eso es por razones de rendimiento.

no estamos trabajando con eventos reales, estamos trabajando con eventos sintéticos que están destinados a dar la misma sensación que trabajar con un evento normal, ese es el comportamiento natural de React, tiene muchas funciones agradables y de alto rendimiento por las que React es realmente conocido, es una de las razones clave por las que la gente usa React.

`SyntheticEvent` registra el nombre de un evento en diferentes navegadores para que usted no tenga que hacerlo. Como contenedor unificado entre navegadores en torno a los eventos nativos del navegador, React SyntheticEventproporciona una API unificada, 

## OBJETO FORM DATA
Para enviar datos a la API ya que al enviar los datos de la misma manera en la que se enviaron a la API cuando creamos el login-form. Sin embargo, en este caso no es posible porque querremos enviar datos que no son de tipo texto (como las imágenes).

ES un objeto propio de JavaScript que nos permitirá enviar datos de cualquier tipo: IMAGENES


```
buildForm() {
        let formData = new FormData();

        formData.append('portfolio_item[name]', this.state.name);
        formData.append('portfolio_item[description]', this.state.description);
        formData.append('portfolio_item[url]', this.state.url);
        formData.append('portfolio_item[category]', this.state.category);
        formData.append('portfolio_item[position]', this.state.position);

        return formData;
    }
```
