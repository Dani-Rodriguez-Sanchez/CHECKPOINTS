## Exercise 1: Create a list, tuple, float, integer, decimal, and dictionary.

LIST: lista=1, 2, 3, 4, 5

TUPLE: tupla=('uno', 'dos' , 'tres', 'cuatro', 'cinco')

FLOAT: f=1.12345

INTEGER: i=12

DECIMAL: mi_decimal=3.3000000000000003

DICTIONARY: diccionario={ 'nombre': 'Dani', 'edad': 49, 'ciudad': 'Donostia' }

## Exercise 2: Round your float up.
  f=1.12345 f+=0.01 print(round(f,2)) #1.13

## Exercise 3: Get the square root of your float. 
  import math f=1.12345 print (math.sqrt(f)) #1.059929242921432

## Exercise 4: Select the first element from your dictionary. 
  mi_lista_diccionario = list(diccionario.values()) print(mi_lista_diccionario0) #Dani

## Exercise 5: Select the second element from your tuple. 
print(tupla1) #dos

## Exercise 6: Add an element to the end of your list. 
lista.append(6) print(lista) #1, 2, 3, 4, 5, 6

## Exercise 7: Replace the first element in your list. 
  lista=1, 2, 3, 4, 5 lista0=6 print(lista) #6, 2, 3, 4, 5

## Exercise 8: Sort your list alphabetically. 
  lista.sort() print(lista) #2, 3, 4, 5, 6

## Exercise 9: Use reassignment to add an element to your tuple.
  tupla=('uno', 'dos' , 'tres', 'cuatro', 'cinco') tupla += ('seis',)

print(tupla) #('uno', 'dos' , 'tres', 'cuatro', 'cinco', 'seis')
---
las preguntas teóricas:

## ¿Cuál es la diferencia entre una lista y una tupla en Python? 
Aunque ambas son contenedores de datos en una variable, y su estructura es parecida, se diferencian en que las tuplas son inmutables, mientras que las listas si se pueden modificar. Además mientras que las listas se declaran con el símbolo corchete [], las tuplas se declaran con paréntesis ().

## ¿Cuál es el orden de las operaciones? 
  Paréntesis, exponenetes, multiplicación, división, adición y sustracción. Se puede utilizar el acrónimo PEMDAS, para recordar el orden. Aunque multiplicación/división, y adición/sustracción pueden intercambiar orden entre ellos sin afectar al resultado.

## ¿Qué es un diccionario Python? 
  Es un método para almacenar en una variable datos clave-valor. A diferencia de las listas que sólo almacenan elementos, aquí podemos crear una clave, a la cual le corresponde un valor. De esta manera, a la hora de consultar un elemento, no necesitamos utilizar el índice como en las listas, y pasaremos la clave para acceder al valor.

## ¿Cuál es la diferencia entre el método ordenado y la función de ordenación? 
Las listas de Python tienen un método ordenado: list.sort() que modifica en la lista el orden de los elementos. Y también se puede utilizar una función de ordenación: sorted() que crea una nueva lista ya ordenada. Por ejemplo:

## Funcion de ordenación:
numeros=5, 2, 3, 1, 4 ordenados=sorted(numeros) ordenados #1, 2, 3, 4, 5

## método ordenado:
  numeros= 5, 2, 3, 1, 4 numeros.sort numeros #1, 2, 3, 4, 5

## ¿Qué es un operador de asignación? Se utilizan para asignar valores a variables, puede ser desde el signo igual =, que es el más básico, y operadores aritméticos, , / , % , +, - . Existe una manera de reducir el tamaño de las operaciones aritméticas, y es mediantes los operadores abreviados, que son capaces de realizar la operación y asignar el valor en un solo paso. Su expresión y equivalencia son las siguientes: = #x=y-->x=x*y /= #x/=y-->x=x/y %= #x%=y-->x=x%y += #x+=y-->x=x+y -= #x-=y-->x=x-y

