>Build out a Diner menu in JAVASCRIPT. Here are your instructions to build that Diner.
Bottega Diner
Have the Main Menu and a Sides Menu
You get one entree and two side choices at regular cost.
- show them the entire menu (print out)
- A user selects an entree.
- “Waitress” makes a comment based on their selection
- comment can either be a comparison of the two items, or random comment pulled from a comment vault.
- Tell them the price
- repeat the above options for side choices (comment and a price)
- total up the cost
BONUS
Have breakfast, lunch, and dinner menu. Breakfast has different items, lunch and dinner have the same items but are different prices.
BONUS: Allow for item customization (how items are prepared, decide additional cost implications)


![Añadir unsubtítulo](https://github.com/Dani-Rodriguez-Sanchez/CHECKPOINTS/assets/150516884/5c41ef12-7384-46ea-9450-e7480cd95b4c)


```
//menu desayuno
const breakfastCafes = [ 
    'café americano', 
    ' café cortado', 
    ' café con leche'
];

const breakfastComplementos = [
    'tostada con aguacate',
    ' tostada con tomate',
    ' croissant' 
];
//menu almuerzo
const lunchMain = [
    'filete de ternera',
    ' dorada al horno ',
    ' langostinos al ajillo'
];

const lunchComplementos = [
    'patatas fritas',
    ' patatas cocidas',
    ' ensalada de col'
];

//comentarios aleatorios
function comentariosAleatorios() {
    const arr = ["Hoy está buenisimo", "Buena elección", "Es nuestra especialidad"];
    return(arr[(Math.floor(Math.random() * arr.length))]);
}
//total menu
let total = 0
function suTotal() {
  total = (Precio)
    alert(`Su cuenta es: {total}€`)
}

//precios
const precioMenuDesayuno = 5;
const precioMenuAlmuerzo = 15;
const precioMenuCena = 20;
var precioAperitivo = 0;
var precioZumo = 0;

//define que tipo de menú mostramos en caso de almuerzo o cena, que comparten elementos, aunque no precio
function menuAlmuerzoCena(){
  alert(`Nuestros principales son: \n${lunchMain}`)
  const platoPrincipal = prompt("¿Cuál prefiere?")
  
  alert (comentariosAleatorios()+`\nNuestos acompañamientos son: \n${(lunchComplementos)}`);
  const complementos = prompt("¿Cuál prefiere?")
  
  if (platoPrincipal.toLowerCase() === "filete de ternera") {
    let coccion = prompt("¿Cómo desea el filete?: muy hecho, al punto, o poco hecho?");
      alert(`perfecto, el filete ${coccion}, lo avisaré en cocina`)
  }
  
  alert (`Su elección ha sido: \n${platoPrincipal} y ${complementos}`)
  
  const aperitivo = confirm("¿Quiere tomar un apertivo antes de su comida, por 3€ adicionales?")
    if (aperitivo == true){
      alert("Ahora mismo le traigo su apertivo");
      var precioApertivo = 3;
    }
    else {
      alert("Ahora le traigo su comida")
    }
  alert (precioApertivo);
}
//define el menu desayuno, tiene elementos distintos a comida y cena
function menuDesayuno(){
  alert(`Nuestros cafés son: \n${breakfastCafes}`)
  const cafe = prompt("¿Cuál prefiere?")
  
  alert (comentariosAleatorios()+`\nNuestos acompañamientos son: \n${(breakfastComplementos)}`);
  const complementos = prompt("¿Cuáles prefiere?")
  
  if (cafe.toLowerCase() === "café con leche" || cafe.toLowerCase()=== "café cortado") {
    let leche = prompt("Desea leche normal, de soja, o sin lactosa");
      alert(`perfecto, su café con leche de ${leche}`)
  }
  
  alert (`Su elección ha sido: \n${cafe} y ${complementos}`)
  
  const aperitivo = confirm("¿Quiere tomar zumo de naranja, por 2€ adicionales?")
    if (aperitivo == true){
      alert("Ahora mismo le traigo su zumo");
      var precioZumo = 2;
    }
    else {
      alert("Ahora le traigo su desayuno")
    }  
}
//elección de menu mediante un mensaje
const eleccionMenu = prompt("Bienvenido a Restaurante Bottega, ¿que tipo de menú desea?")
  if (eleccionMenu.toLowerCase() === "desayuno") {
    alert("Adelante, ahora le doy su menú, puede elegir café y un acompañamiento por 5€");
    menuDesayuno();
    let suTotal = (precioMenuDesayuno + precioZumo); {
      alert (`Su total, incluido el Zumo es: ${suTotal}€`);}
    //aqui hay un problema, el valor del var precioZumo no se actualiza
  }

  else if (eleccionMenu.toLowerCase() === "almuerzo") {
    alert("Adelante, ahora le doy su menú, puede elegir un plato principal y dos acompañamientos por 15€");
    menuAlmuerzoCena();
    let suTotal = (precioMenuAlmuerzo + precioAperitivo); {
      alert (`Su total, incluido el Aperitivo es: ${suTotal}€`);}
    //aqui hay un problema, el valor del var precioAperitivo no se actualiza
   
  }
  else if (eleccionMenu.toLowerCase() === "cena") {
    alert("Adelante, ahora le doy su menú, puede elegir un plato principal y dos acompañamientos por 20€");
    menuAlmuerzoCena();
    let suTotal = (precioMenuCena + precioAperitivo); {
      alert (`Su total, incluido el Aperitivo es: ${suTotal}€`);}
    //aqui hay un problema, el valor del var precioAperitivo no se actualiza

  }
  else{
    alert("disculpe, esto es un restaurante");}

```
