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

'''
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
## ¿Cuáles son algunas cosas que puede hacer para prepararse para las entrevistas de trabajo?

