# Aprenda sobre arrays en PHP

# Indice

[Definición](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#definici%C3%B3n)

[Sintaxis](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#sintaxis)

[Recuento del número de elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#recuento-del-n%C3%BAmero-de-elementos)

[Modificación de elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#modificaci%C3%B3n-de-elementos)

[Agregar elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#agregar-elementos)

[Eliminar elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#eliminar-elementos)

[Invertir el orden de los elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#invertir-el-orden-de-los-elementos)

[Ordenar una lista](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#ordenar-una-lista)

[Sub-Listas](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#sub-listas)

[Listas Multidimensionales](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#listas-multidimensionales)

[Creación de listas en blanco](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#creaci%C3%B3n-de-listas-en-blanco)

[Recopilación](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/python.md#recopilaci%C3%B3n-de-todo-lo-dado)

# Definición

En primer lugar, debemos definir lo que es un `array`.

Una `Lista` es un tipo de dato estructurado con una colección de elementos con valores o variables ( o incluso otras listas ).

# Sintaxis

Iniciamos una variable a la que le asignamos un valor de colección. La colección estará contenida entre corchetes `[]` y cada elemento separado por comas `,`

```python

lista = ['Elemento1', 'Elemento2', 'Elemento3', 'Elemento4']

```

Para seleccionar un elemento, debemos saber su posición. La posicion es distinta al elemento, es decir, el `Elemento1` está en la posición 0. 
el `Elemento2` está en la posicion 1.

```python

lista = ['Hola', 'soy', 'acruma', '.']
print(lista[0]) #Mostrará el valor del primer elemento. (`Hola`)

print(lista[2]) #Mostrará el valor del tercer elemento. (`acruma`)

```

Tabla de posiciones de los elementos

 Elemento 1 | Elemento 2 | Elemento 3 | Elemento 4 | Elemento 5 | Elemento 6 
---|---|---|---|---|---
 Posicion 0 | Posicion 1 | Posicion 2 | Posicion 3 | Posicion -2| Posicion -1 

# Recuento del número de elementos

Para saber cuantos elementos tiene una lista usaremos `len`

```python

lista = ['Elemento1', 'Elemento2', 'Elemento3', 'Elemento4']
numero_lista = len(lista)
print(numero_lista) #Mostrará `4` que es el número de elementos.

```

# Modificacion de elementos

Le asignaremos un nuevo valor a la posición deseada.

```python

numeros = [10, 12, 15, 20, 25]
numeros[2] = 55   #La posicion 2 (15) pasará a valer (55) Resultado; [10, 12, 55, 20, 25]
numeros[0] = 2    #Cambiaremos el primer elemento (10) pasará a valer (2) Resultado; [2, 12, 55, 20, 25]
numeros[-1]= 0    #Cambiaremos el ultimo elemento (25) pasará a valer (0) Resultado; [2, 12, 55, 20, 0]

print(numeros)    #Se mostrará en pantalla [2, 12, 55, 20, 0]

```

# Agregar elementos

Para añadir usaremos `.insert`(  la posición y su valor ). Y para añadir al final de la lista usaremos `.append`( su valor )

```python

colores = ['Rojo', 'Verde', 'Azul']
colores.insert(2, 'Gris')   #Se agregará 'Gris' en la posicion (2)          Resultado; ['Rojo', 'Verde','Gris, 'Azul']
colores.insert(0, 'Blanco') #Se agregará 'Blanco' al principio de la lista. Resultado; ['Blanco', 'Rojo', 'Verde','Gris, 'Azul']
colores.append('Negro')     #Se agregará 'Negro' al final de la lista.      Resultado; ['Blanco', 'Rojo', 'Verde','Gris, 'Azul', 'Negro']

print(colores) # Se mostrará ['Blanco', 'Rojo', 'Verde','Gris, 'Azul', 'Negro']

```

# Eliminar elementos

Para eleminiar un elemento usaremos `.pop` y la posicion del elemento a eliminar

```python

lenguajes = ['Python', 'Bash', 'PowerShell', 'Java']
lenguajes.pop(2)			#Se eliminará el elemento en la posicion (2) es decir 'PowerShell' Resultado; ['Python', 'Bash', 'Java']
lenguajes.pop(0)			#Se eliminará el primer elemento es decir 'Python' Resultado; ['Bash', 'Java']
lenguajes.pop()				#Se eliminará el ultimo elemento es decir 'Java'   Resultado; ['Bash']

print(lenguajes)	# Se mostrará ['Bash']

```

# Invertir el orden de los elementos

Para invertir el orden de los elementos, usaremos `.reverse()`

```python

numeros = [10, 40, 20, 35]		
letras = ['g', 'a', 'z', 'd']	

numeros.reverse()		#Resultado [35, 20, 40, 10]
letras.reverse()		#Resultado ['d', 'z', 'a', 'g']

```

# Ordenar una lista

Para ordenar una lista de menor a mayor (numeros) o en orden alfabetico (a > z) usaremos `sorted()`


```python

numeros = [10, 40, 20, 35]
letras = ['g', 'a', 'z', 'd']

print(sorted(numeros))		#Resultado [10, 20, 35, 40]

#O guardandolo en una nueva variable

letras_ordenadas = sorted(letras)
print (letras_ordenadas)	#Resultado ['a', 'd', 'g', 'z']

```

Si combinamos en orden los pasos de "Ordenar una lista" e "Invertir el orden" conseguiremos ordenar una lista de mayor a menor (numeros)
o en orden alfabetico (z > a).

# Sub-Listas

Podemos crear sub-listas apartir de una lista. Para ello usaremos `nombre_lista[inicio:fin]` Donde INICIO, es el primer elemento a seleccionar y FIN (si esta relleno) el ultimo -1.

```python

abecedario = ['a', 'b', 'c', 'd', 'e']

sub_abecedario1 = abecedario[:]		# Resultado ['a', 'b', 'c', 'd', 'e']
sub_abecedario2 = abecedario[2:]	# Resultado ['c', 'd', 'e']
sub_abecedario3 = abecedario[2:4]	# Resultado ['c', 'd'] Notese, el elemento 4 no se incluye
sub_abecedario4 = abecedario[-3:-2]	# Resultado ['c'] Notese, el elemento -2 no se incluye

```

# Listas multidimensionales

(Es un concepto abstracto a veces dificil de comprender)

A continuacion se mostrará como crear una lista con mas de una dimension, es decir, `2D`, `3D`, `4D` etc..


```python

lista2d = [  [0,1,2], [1,1,2], [2,1,2], [3,1,2]  ]

print(lista2d[3][0])		# Mostrariamos el elemento [3] de la primera dimension ( [3,1,2] ) 
				# Y luego el elemento[0] de la segunda dimension que seria el "3"
						
						
lista3d = [   [[0,1,2], [1,1,2]]   ,   [[2,1,2], [3,1,2]]   ] 

print(lista3d[0][1][2]) # Mostrariamos el elemento [0] de la primera dimension [[0,1,2], [1,1,2]]
			# Luego mostrariamos el elemento [1] de la segunda dimension [1,1,2]
			# Y por ultimo el elemento [2] de la tercera dimension "2"

```

Se puede operar con lo aprendido hasta ahora, con cualquier tabla multidimensional.

# Creacion de listas en blanco

Podemos crear una lista en blanco. ( Por ejemplo, para rellenar mas tarde )

```python

lista_vacia_1d = []                      # Crea una lista vacia de 1 dimension
lista_vacia_2d = [ [] ]                  # Crea una lista vacia de 2 dimensiones
lista_vacia_3d = [ [ [] ] ]              # Crea una lista vacia de 3 dimensiones

#Etcétera...

```

# Recopilación de todo lo dado.

```python

lista_2d_vacia = [[],[]] # Lista 2 dimensiones

print(len(lista_2d_vacia)) # Mostrará que tiene 2 elementos

lista_2d_vacia[0].insert(0, 4.1) # Agregamos al elemento 0-0 > 4.1
lista_2d_vacia[0].insert(1, 2)   # Agregamos al elemento 0-1 > 2

lista_2d_vacia[1].append('Acruma') # Agregamos a la ultima posicion del elemnto 1 > 'Acruma'
lista_2d_vacia[1].append('Soy')   # Agregamos a la ultima posicion del elemnto 1 > 'Soy'

lista_2d = lista_2d_vacia   # Volcar valor a nueva variable

print(lista_2d) 	# Mostrará [  [4.1, 2]  ,  ['Acruma', 'Soy']  ]

lista_2d[0][1] = 10 # Modificamos 0-1 que tenia de valor "2" a valor "10"

lista_2d[1].pop(1)  # Eliminamos  1-1 que tenia de valor 'Soy'

lista_2d_vacia[1].append('te') # Agregamos a la ultima posicion del elemnto 1 > 'te'
lista_2d_vacia[1].append('enseña') # Agregamos a la ultima posicion del elemnto 1 > 'enseña'
lista_2d_vacia[1].append('Python') # Agregamos a la ultima posicion del elemnto 1 > 'Python'

print(lista_2d)     # [[4.1, 10], ['Acruma', 'te', 'enseña', 'Python']]

lista_2d[0].reverse() # Le damos la vuelta al elemento 0
lista_2d[1] = sorted(lista_2d[1]) # Ordenamos alfabeticamente el elemento 1

print(lista_2d) # Mostrará [[10, 4.1], ['Acruma', 'Python', 'enseña', 'te']] -- ( Mayúsculas primero )

sub_lista_2d = lista_2d[1][1:3]  # Elegimos del elemento 1. Los elementos 1 y 2 ( el 3 no se selecciona, recuerdalo )

print(sub_lista_2d)  # Mostrará ['Python', 'enseña']

```

By [@acruma](https://github.com/acruma)
