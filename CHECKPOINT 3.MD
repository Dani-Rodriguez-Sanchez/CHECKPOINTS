## EJERCICIO: Exercise 1: Create a string, number, list, and boolean, each stored in their own variable. #string cadena='mi cadena'
```
#number(integer)
entero=2

#number(float)
decimal=2.5

#list
lista=["manzana","fresa","naranja"]

#boolean
acabado=True
```
## Exercise 2: Use an index to grab the first 3 letters in your string, store that in a variable. 
`cadena='mi cadena' nueva_cadena=cadena:3 print(nueva_cadena)`

## Exercise 3: Use an index to grab the first element from your list. 
`lista="manzana","fresa","naranja" elemento=lista0 print(elemento)`

## Exercise 4: Create a new number variable that adds 10 to your original number. 
`entero=2 nuevo_entero=entero+10 print(nuevo_entero)`

## Exercise 5: Use an index to get the last element in your list. lista="manzana","fresa","naranja" nueva_lista=lista-1 print(nueva_lista)

## Exercise 6: Use split to transform the following string into a list. names = 'harry,alex,susie,jared,gail,conner' names = names.split(',') print(names)

## Exercise 7: Get the first word from your string using indexes. Use the upper function to transform the letters into uppercase. 
Create a new string that takes the uppercase word and the rest of the original string. cadena='mi cadena' primera_palabra=cadena.split()0 print(primera_palabra)
```
cadena_mayusculas=cadena.upper()
print(cadena_mayusculas)

cadena_mayuscula_primera=cadena.capitalize()
print(cadena_mayuscula_primera)

#no tenia claro si se refería a que hiciese mayúscula sola la primera palabra o todas, así 	que he investigado y he encontrado esta manera de imprimir en 
    mayúsculas todas la 	palabras del string. 

import string
cadena='mi cadena'
cadena=string.capwords(cadena)
print(cadena)
```
## Exercise 8: Use string interpolation to print out a sentence that contains your number variable. 
`entero=2 sentencia=f"hola, el numero elegido es {entero}" print(sentencia)`

## Exercise 9: Print “hello world”.

`print("hello world")`
---
PREGUNTAS TEORICAS

## ¿Cuáles son los 4 tipos de datos en Python?
Los tipos básicos son: String, Number(int y float), List, y Boolean

## ¿Qué tipo de convención de nomenclatura debemos usar para las variables en Python? 
Hay 3 reglas: 1-solo puede contener letras(mayúsculas y minúsculas), numeros, y guiones bajos(_) 
2-solo puede comenzar con letra o guión bajo, núnca con números 
3-Hay que evitar el uso de palabras reservadas, como True, False, def, else... *además son “case-sensitive”, con lo que por ejemplo diferencia entre Cadena y cadena

## ¿Qué es un heredoc de Python? Son cadenas de varias líneas, se organizan mediante 3 “””. 
Por ejemplo: cadena=””” linea1 linea2 linea3 “”” 

## ¿Qué es la interpolación de cadenas? Es la posibilidad de introducir una variable dentro de una cadena, 
su utilidad es dar dinamismo a la programación, ya que se pueden cambiar dinámicamente. Y se realiza mediante los corchetes {}. Uno de los métodos es el f-string. 
Por ejemplo:
```
usuario =  "Maria" 
edad =  "20" 
print (f "Hola {usuario}. Tu edad es {edad}" )
```
## ¿Cuándo debemos usar comentarios en Python? Lo ideal es que el mismo código se explique a si mismo, mediante los nombres adecuados. 
No son útiles para explicar la funcionalidad, ya que esta puede cambiar, aunque si lo son para ayudar a comprender el diseño del código a otros programadores o nosotros mismos en el futuro. 
Además deben ser frases concisas, fáciles de entender, limitados en su número, y actualizados

## ¿Cuáles son las diferencias entre las aplicaciones monolíticas y de microservicios 
-Las aplicaciones monoliticas funcionan desde un único código base, mientras que las basadas en microservicios, cada uno de ellos funciona para lograr una única característica. 

-La implementación y el desarrollo de las monolíticas es más sencilla, aunque también es más complejo su mantenimiento. 
-En caso de surgir algún problema, las de microservicios limitarían el error al servicio concreto, mientras que el resto de la aplicación seguiría funcionando, 
siendo así también más rápido de Identificar. -Además las monolíticas son más rápidas, ya que los servicios no necesitan comunicarse 
*Por lo tanto, no hay una opción general más indicada que otra, si no que dependerá del tipo de proyecto elegir el sistema adecuado

---

En el Ejercicio 7, se te pide hacer lo siguiente:

Obtener la primera palabra de la cadena: Para esto, debes dividir la cadena completa en palabras individuales. 
En Python, puedes usar el método split() que separa una cadena en una lista de subcadenas basándose en un delimitador, que en este caso es un espacio en blanco (' '). 
Al aplicar split(' ') a la cadena string, obtienes una lista donde cada elemento es una palabra. 
Luego,seleccionas el primer elemento de esta lista, que corresponde a la primera palabra de la cadena original. 
Transformar la primera palabra a mayúsculas: Una vez que tienes la primera palabra, puedes convertirla a mayúsculas usando la función incorporada upper(). 
Esta función toma una cadena y retorna una nueva cadena con todos los caracteres convertidos a mayúsculas. 
Crear una nueva cadena con la palabra en mayúsculas y el resto de la cadena original: Para lograr esto, 
necesitas eliminar la primera palabra de la cadena original y luego concatenarla con la versión en mayúsculas de la misma palabra.
Para eliminar la palabra, puedes usar el método replace() de la cadena original, indicando la palabra a reemplazar y una cadena vacía (''). 
Sin embargo, es importante tener en cuenta que replace() reemplaza todas las ocurrencias de la palabra, por lo que si la primera palabra aparece más de una vez en la cadena, 
todas las instancias serán eliminadas. Para evitar esto, puedes limitar el número de reemplazos a uno, pasando un tercer argumento a replace() con el valor 1. 
Aquí está el código corregido para el Ejercicio 7:
```
# Suponiendo que 'string' contiene la cadena 'hola mundo'
first_word = string.split(' ')[0]  # Obtiene la primera palabra 'hola'
first_word_upper = first_word.upper()  # Convierte a mayúsculas 'HOLA'
rest_of_string = string.replace(first_word, '',   1)  # Elimina la primera palabra
new_string = first_word_upper + rest_of_string  # Une la palabra en mayúsculas con ' mundo'
print(new_string)  # Imprime 'HOLA mundo'
```
Este código garantiza que solo la primera palabra sea reemplazada y convertida a mayúsculas, y luego se combina con el resto de la cadena original para formar una nueva cadena.


