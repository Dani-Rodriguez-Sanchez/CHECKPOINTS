# checkpoint8

## Ejercicio

*

    <pre><code><strong>Cree un bucle for en JS que imprima cada nombre de esta lista.
    </strong>        myList = ["velma", "scout", "jane", "john", "harry"]
    </code></pre>

```
let myList= [
  		"velma", 
  		"scout", 
  		"jane", 
  		"john", 
  		"harry"
	];

	for (var key in myList) {
  		console.log(myList[key]);
	}
	/*con el bucle for, le decimos que para cada elemento en myList, ejecute
	el console.log de cada elemento de esta lista, iterando a través de la 	variable key, 
	que acabamos de crear*/
```

*

    ```
    Cree un bucle while que recorra la misma lista e imprima también los nombres. 
    ```

```
let myList= [
  		"velma", 
  		"scout", 
  		"jane", 
  		"john", 
  		"harry"
	];

	var i = 0;
	while (i < myList.length) {
  		console.log(myList[i]);
  		i++;
	}
	//queremos que se ejecute el console.log de cada elemento de la lista, y
	para ello creamos un índice(i) que definimos en 0, y le decimos que cada 
	vez que se ejecute el código se le sume 1, a través del i++. Entonces, 
	introduciendo el condicional “mientras i sea menor que la longitud de la 
	lista”, ejecuta el console.log de cada elemento.*/

```

*

    ```
    Cree una función de flecha que devuelva "Hello World".
    ```

```
const holaMundo = () => {console.log ("Hello World")};

	holaMundo();

	/* Creamos la función holaMundo, sin parámetros, y con arrow le decimos 	
	que ejecute console.log, y que imprima Hello World.*/

```

## ¿Qué tipo de bucles hay en JS?

Los bucles son útiles para repetir un mismo código varias veces, como por ejemplo iterar los elementos de una lista.

Los tipos de bucles que hay son FOR y WHILE.

**FOR.**

Crea un bucle con una duración definida por sus expresiones.

Sintaxis básica:

```
for (begin; condition; step) { 
  // ... elemento a ejecutar...
}
```

Admite la declaración de variable dentro del bucle, podemos definir un elemento, darle un valor iniciar, decirle que lo modifique con cada vuelta del bucle, y parar el bucle cuando haya llegado a tal valor.

Por ejemplo:

```
let i = 0;
for (i = 0; i < 3; i++) { 
console.log(i); 
// 0, 1, 2
```

**WHILE Y DO/WHILE**

Tiene un funcionamiento diferente, ya que recorre un código mientras que una condición sea verdadera (true). Do while hace lo mismo, pero el código se ejecuta al menos una vez antes de la condición.

Sintaxis básica:

```
while (condition) {
  // code block to be executed
}
```

Previo al bucle, definimos i como 0, y le decimos que mientras i sea menor que 3, imprima cada i, sumándole 1 en cada vuelta del bucle. Finalizaría al llegar el index de i a 3.

```
let i = 0; 
while (i < 3) { 
	console.log( i ); 
	i++; 
}
//0, 1, 2

```

{% embed url="https://es.javascript.info/while-for#el-bucle-forhttps://www.w3schools.com/js/js_loop_for.asp" %}

## ¿Cuáles son las diferencias entre const, let y var?

Las tres se usan para la declaración de variables, aunque tienen alguna diferencia.

VAR eras las más usadas antes de la llegada de ES6. Las variables creadas con var se pueden volver a declarar y modificar. Tiene ámbito global cuando se declara fuera de la función, y local cuando está situada dentro.

`var x = 10;`

`var x = 20;`   &#x20;

**LET** es la preferible para la declaración de variables. Su alcance es sólo dentro del bloque de la función, dentro de los {}, significa que no estará disponible fuera de él. A diferencia de VAR, puede modificarse pero no volver a declararse, es decir, no puedes declarar la misma variable varias veces.

```
let x = 10; 
{ 
let x = 20; 
console.log(x); // Esto mostrará 20 ya que está dentro de su ámbito
} 
console.log(x); // Esto mostrará 10 al estar fuera de los {}

```

**CONST** tiene similitudes con LET, pero no puede modificarse ni volver a declararse. Aunque no es inmutable, ya que si declaras un objeto o array con Cont, puedes modificar sus propiedades.

`const cars = ["Saab", "Volvo", "BMW"];`

Por lo tanto, deberá usarse CONST, para variables que queremos mantener constantes(Arrays y objetos), LET es flexible y limita el alcance de la variable, pero sin los problemas que puede ocasionar Var, y VAR mejor evitar, solo es útil para su uso con navegadores antiguos.

## ¿Qué es una función de flecha?

Es una forma de definir una función, es bastante reciente, ya que fué introducida en el ES6, y surge como una manera de simplificar código, dando lugar a una sintaxis más sencilla y fácil de leer, que en el caso de funciones simples puede ser definida en una sola línea. De hecho se prescinde de return, incluso se puede no incluir las {}.

Como ejemplo, esta función de multiplicar, con dos parámetros como argumentos, que en el bloque de la función se multiplican, y se imprime el resultado:\


```
const multiplicar = (x, y) => { const resultado = x * y; console.log(resultado); } 

multiplicar(2, 3); // 6

```

Puede aceptar ningún argumento, uno, o varios. Además de la palabra THIS, con la peculiaridad de que en este caso, this, hereda las condiciones del ámbito principal, mientras que en una función normal variaría dependiendo donde se escriba la función.

```
const myObject = {
  fullname: 'John Doe',
  sayName: () => {
    return `My name is ${this.fullname}`
  },
}

const myMethod = myObject.sayName
console.log(myMethod())
```

{% embed url="https://www.w3schools.com/js/js_arrow_function.asphttps://desarrolloweb.com/articulos/arrow-functions-es6.html" %}

## ¿Qué es la deconstrucción variable?

La deconstrucción de variables es una técnica que permite extraer limpiamente valores de un array y asignarlos a nuevas variables. Consigue que el código sea menos repetitivo, y cumplir el principio de programación DRY (_don´t repeat yourself_)

Entonces podríamos hacer algo así, donde se asigna en orden los dos elementos del array perfil, accedemos a ellos, y los asignamos a nuevas variables con nombres independientes.

\


```
const perfil = ["Daniel", "Rodriguez"];

const [nombre, apellido] = perfil;

console.log(nombre); // "Daniel"
console.log(apellido); // "Rodriguez"
```

//en lugar de este código más largo:

```
const perfil = ["Daniel", "Rodriguez"];

const nombre = perfil[0];
const apellido = perfil[1];


console.log(nombre); // "Daniel"
console.log(apellido); // "Rodriguez"
```

También podemos aprovechar la deconstrucción para combinar objetos y funciones, y lograr que se reconecten:

```
const user = {
  name: 'Daniel',
  lastname: 'Rodriguez'
}

const renderUser = ({ name, lastname }) => {
  console.log(`${name}: ${lastname}`);
}
```

{% embed url="https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Destructuring_assignmenthttps:/www.freecodecamp.org/espanol/news/arreglos-vs-desestructuracion-de-objectos-en-javascript/" %}

## ¿Qué hace el operador de spread JS?

Es un operador nos permite copiar rápidamente todo o parte de una array u objeto existente en otra array u objeto. Su sintaxis será tres puntos seguidos de algún tipo de palabra (...word)

Su utilidad es poder distribuir los elementos de un _iterable_ (cadena de texto, array) dentro de uno nuevo.

En este ejemplo, se combinan los elementos de una array, dentro de otra nueva a través de la definición de la nueva incluyendo ...delante del nombre de la emisora.

```
let frutas = ['Manzana', 'Pera', 'Platano'];

let nuevasFrutas = ['Fresa', ...frutas];
console.log(nuevasFrutas);
// Resultado -> ["Fresa","Manzana","Pera","Platano"]

```

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax" %}

## ¿Qué es OOP?

_**Object Oriented Programming**_

Es un estilo o paradigma de programación basado en clases y objetos. Estos últimos agrupan datos (propiedades) y métodos (acciones) dentro de sí mismo. Por ser un paradigma, dependiendo del tipo de proyecto, tendremos que elegir entre utilizar una programación basada en funciones (recomendable para códigos pequeños), y otra orientada a objetos, con clases y métodos (en los proyectos que requieren una arquitectura más sólida y mantenible en el tiempo).

El ejemplo sacado de la vida real podría ser el siguiente: la clase es el concepto de coche, el objeto es un modelo concreto de coche, con las propiedades (cilindrada, nºplazas, color, etc.) y con los métodos (acelerar, frenar, cambiar de marcha, etc).

La clase es como una representación de un conjunto, la instancia de una clase es lo que realmente tiene el código propio. En este sentido, podemos tener varias instancias de una sola clase, como podemos tener copias únicas de una sola versión original.

Un objeto también se llama instancia de clase, ya que se crea mediante la instanciación, que consiste en crear un nuevo objeto a partir de una plantilla o molde predefinido. Esto se realiza por dos métodos, ESTÁTICO, y de INSTANCIA, se diferencian en cómo se accede a ellos y cómo se utilizan.

En el **método de INSTANCIA** primero se crea una instancia de clase, se convierte en objeto y a partir de ahí se le añaden atributos y métodos:

```
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre
    this.edad = edad
  }
 //así creamos la clase con el constructor que acepta dos parametros
  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`)
  }
//así creamos un método para la clase
}
const persona1 = new Persona("Daniel", 49)
persona1.saludar() // ¡Hola! Mi nombre es Daniel y tengo 49 años.
//y así creamos una instancia de clase. Podríamos crear mas, ya que la //estructura de objeto es reutilizable
```

A diferencia, el **método ESTATICO** no requiere un objeto para funcionar, se puede llamar a un método estático sin crear primero un objeto de la clase.

```
class Chat {
    static sendMessage() {
      return "Hola!";    }
}
console.log(Chat.sendMessage());
//"Hola!"
```

Hay varios conceptos básicos, como HERENCIA (para reutilizar código, ya que propiedades y métodos se heredan a las subclases), ENCAPSULAMIENTO (los propiedades y métodos pueden ser privados al interior de las funciones), y POLIMORFISMO (podemos ejecutar un mismo método en objetos distintos).

{% embed url="https://www.campusmvp.es/recursos/post/los-conceptos-fundamentales-sobre-programacion-orientada-objetos-explicados-de-manera-simple.aspxhttps://codigomovil.mx/blog/programacion-orientada-a-objetos-en-javascript" %}

## ¿Qué es una promesa JS?

Como concepto, es algo que, en principio pensamos que se cumplirá, pero queremos anticiparnos, y crear ciertos escenarios: se cumple, no se cumple, o queda en un estado pendiente.

Debido a la naturaleza asíncrona de JS, que en resumen significa que las instrucciones no son necesariamente ejecutadas una después de otra. Entonces, cuando nos comunicamos con una API externa, puede suceder que necesitemos que una tarea se ejecute antes que otra.

Por ejemplo, podemos necesitar que Twitter nos muestre unos elementos primero, y decidir que otros pueden tardar mas en caso que tarden más tiempo en cargar.

En JS, una promesa es un objeto que representa la finalización o falla de una tarea asíncrona y su valor resultante.

Esta es la sintaxis básica:

```
const myPromise = new Promise((resolve, reject) => { 
// Aquí se realiza la operación asíncrona 
	resolve(); // exito
  	reject();  // error
 }); 

myPromise 
	.then(resultado => { { console.log(value) })

	// el resultado está asociado a resolve, se cumple la promesa, ejecuta lo que esté entre {}
	.catch(error => {  console.log(err) });

	// resultado asociado a reject, no se cumple la promesa
```

Ejemplo, quiero comprobar que los valores x e y son estrictamente iguales. En caso positivo, lanzar un mensaje afirmativo, y en el contrario lanzar un error.

```
let myPromise = new Promise(function (resolve, reject) {
    const x = "manzana";
    const y = "manzana"
    if (x === y) {
        resolve();
    } else {
        reject();
    }
});
 
myPromise.
    then(function () {
        console.log('efectivamente, es una manzana');
    }).
    catch(function () {
        console.log('Some error has occurred');
    });
```



{% embed url="https://es.javascript.info/asynchttps://www.freecodecamp.org/news/guide-to-javascript-promises/" %}

## ¿Qué hacen async y await por nosotros?

Es una sintaxis especial para trabajar con promesas de una forma más confortable y fácil de escribir.

**ASYNC** hace que una función devuelva una Promesa, y **AWAIT** hace que la función suspenda la ejecución, y espere una promesa resuelta antes de continuar, sólo se puede usar dentro de la función async.

Por la naturaleza asíncrona de JS, necesitamos considerar el orden en el que se devuelven las funciones, ya que de no ser así lo que sucediese más rápido sería el que regresase primero, y esto puede no ser lo que necesitemos,y nos encontraríamos con un error. Entonces por ese motivo necesitamos la función async y await, para definir el orden en el que se llaman y devuelven las funciones.

Son una evolución de las funciones CALLBACK, las cuales se pasan como argumento a otra función y se ejecutan después de que se haya completado alguna operación. Pero su uso excesivo puede generar código complejo, y por ello ASYNC/AWAIT, es una alternativa más moderna para simplificar esta programación.

https://www.freecodecamp.org/espanol/news/tutorial-de-async-await-de-javascript/
