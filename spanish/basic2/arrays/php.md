# Aprenda sobre arrays en php

# Indice

[Definición](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#definici%C3%B3n)

[Sintaxis](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#sintaxis)

[Recuento del número de elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#recuento-del-n%C3%BAmero-de-elementos)

[Modificación de elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#modificaci%C3%B3n-de-elementos)

[Agregar elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#agregar-elementos)

[Eliminar elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#eliminar-elementos)

[Invertir el orden de los elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#invertir-el-orden-de-los-elementos)

[Ordenar un array](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#ordenar-un-array)

[Sub-Arrays](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#sub-arrays)

[Arrays Multidimensionales](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#arrays-multidimensionales)

[Creación de arrays en blanco](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#creaci%C3%B3n-de-arrays-en-blanco)

[Recopilación](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#recopilaci%C3%B3n-de-todo-lo-dado)

# Definición

En primer lugar, debemos definir lo que es un `array`.

Un `array` es un tipo de dato estructurado con una colección de elementos con valores o variables ( o incluso otros arrays ).

# Sintaxis

Iniciamos una variable a la que le asignamos un valor de colección. La colección estará contenida entre corchetes `[]` y cada elemento separado por comas `,`

Para imprimir un array en `php` usaremos `print_r`

```php

$array = ['Elemento1', 'Elemento2', 'Elemento3', 'Elemento4'];

print_r ($array); #Con print_r imprimiremos la estructura del array

```

Para seleccionar un elemento, debemos saber su posición. La posicion es distinta al elemento, es decir, el `Elemento1` está en la posición 0. 
el `Elemento2` está en la posicion 1.

```php

$array = ['Hola', 'soy', 'acruma', '.'];
echo($array[0]); #Mostrará el valor del primer elemento. (`Hola`)

echo($array[2]); #Mostrará el valor del tercer elemento. (`acruma`)

```

Tabla de posiciones de los elementos

 Elemento 1 | Elemento 2 | Elemento 3 | Elemento 4 | Elemento 5 | Elemento 6 
---|---|---|---|---|---
 Posicion 0 | Posicion 1 | Posicion 2 | Posicion 3 | Posicion -2| Posicion -1 

# Recuento del número de elementos

Para saber cuantos elementos tiene una array usaremos `count`

```php

$array = ['Elemento1', 'Elemento2', 'Elemento3', 'Elemento4'];
$numero_array = count($array);
echo $numero_array; #Mostrará `4` que es el número de elementos.

```

# Modificacion de elementos

Le asignaremos un nuevo valor a la posición deseada.

```php

$numeros = [10, 12, 15, 20, 25];
$numeros[2] = 55;   #La posicion 2 (15) pasará a valer (55) Resultado; [10, 12, 55, 20, 25]
$numeros[0] = 2;    #Cambiaremos el primer elemento (10) pasará a valer (2) Resultado; [2, 12, 55, 20, 25]
$numeros[count($numeros) -1]= 0;    #Cambiaremos el ultimo elemento (25) pasará a valer (0) Resultado; [2, 12, 55, 20, 0]

print_r($numeros);

```

# Agregar elementos

Para añadir un elemento al principio de un array usaremos `array_unshift($array, Valor)`. 

Para añadir un elemento al final de un array usaremos `array_push($array, Valor)`. 

Para añadir un elemento en una posicion deseada usaremos `array_splice($array, POSICION, 0, Valor)` 

Importante, si el valor `0` se cambia por otro valor, se eliminará una porcion del array (siguientes X elementos). Vease en el siguiente apartado [Eliminar elementos](https://github.com/acruma/learn/blob/master/spanish/basic2/arrays/php.md#eliminar-elementos). 

```php

$colores = ['Rojo', 'Verde', 'Azul'];

array_splice($colores, 2, 0, 'Gris');   #Se agregará 'Gris' en la posicion (2)          Resultado; ['Rojo', 'Verde','Gris, 'Azul']
array_unshift($colores, 'Blanco'); #Se agregará 'Blanco' al principio de la array. Resultado; ['Blanco', 'Rojo', 'Verde','Gris, 'Azul']
array_push($colores, 'Negro');     #Se agregará 'Negro' al final de la array.      Resultado; ['Blanco', 'Rojo', 'Verde','Gris, 'Azul', 'Negro']

print_r($colores); # Se mostrará ['Blanco', 'Rojo', 'Verde','Gris, 'Azul', 'Negro']

```

# Eliminar elementos

Para eliminar una cantidad X de elementos usaremos `array_splice($array, POSICION Inicial, Cantidad)` Donde cantidad empieza en el elemento "Posicion Inicial".

Para eliminar el primer elemento `array_shift()`

Para eliminar el ultimo elemento `array_pop()`


```php

$lenguajes = ['php', 'Bash', 'PowerShell', 'Java'];

array_splice($lenguajes, 2, 1);		#Se eliminará el elemento en la posicion (2) es decir 'PowerShell' Resultado; ['php', 'Bash', 'Java']
array_shift($lenguajes);			#Se eliminará el primer elemento es decir 'php' Resultado; ['Bash', 'Java']
array_pop($lenguajes);				#Se eliminará el ultimo elemento es decir 'Java'   Resultado; ['Bash']

print_r($lenguajes);	# Se mostrará ['Bash']

```

# Invertir el orden de los elementos

Para invertir el orden de los elementos, guardaremos en una variable el array invertido con `array_reverse()` .

```php

$numeros = [10, 40, 20, 35];	
$letras = ['g', 'a', 'z', 'd'];

$numeros_invertidos = array_reverse($numeros);		#Resultado [35, 20, 40, 10]
$letras_invertidas = array_reverse($letras);		#Resultado ['d', 'z', 'a', 'g']

print_r($numeros_invertidos);

print_r($letras_invertidas);

```

# Ordenar un array

Para ordenar una array de menor a mayor (numeros) o en orden alfabetico (a > z) usaremos `sort()`


```php

$numeros = [10, 40, 20, 35];
$letras = ['g', 'a', 'z', 'd'];

sort($numeros);	
print_r($numeros); #Resultado [10, 20, 35, 40]

#O guardandolo en una nueva variable

$letras_ordenadas = $letras;
sort($letras_ordenadas);
print_r($letras_ordenadas);	#Resultado ['a', 'd', 'g', 'z']


```

Si combinamos en orden los pasos de "Ordenar una array" e "Invertir el orden" conseguiremos ordenar una array de mayor a menor (numeros)
o en orden alfabetico (z > a).

# Sub-Arrays

Podemos crear sub-arrays apartir de un array. Para ello usaremos `array_slice(array, punto_inicio, cantidad)` Donde INICIO, es el primer elemento a seleccionar y cantidad el numero de elementos a seleccionar.

```php

$abecedario = ['a', 'b', 'c', 'd', 'e'];

$sub_abecedario1 = array_slice($abecedario, 0);		# Resultado ['a', 'b', 'c', 'd', 'e']
$sub_abecedario2 = array_slice($abecedario, 2);	# Resultado ['c', 'd', 'e']
$sub_abecedario3 = array_slice($abecedario, 2, 2);	# Resultado ['c', 'd'] Empezamos en elemento 2 y cogemos 2 (el 2 inclusive)
$sub_abecedario4 = array_slice($abecedario, -3, -2);	# Resultado ['c'] 

```


# Arrays multidimensionales

(Es un concepto abstracto a veces dificil de comprender)

A continuacion se mostrará como crear una array con mas de una dimension, es decir, `2D`, `3D`, `4D` etc..


```php

$array2d = [  [0,1,2], [1,1,2], [2,1,2], [3,1,2]  ];

print_r($array2d[3][0]);		# Mostrariamos el elemento [3] de la primera dimension ( [3,1,2] ) 
				# Y luego el elemento[0] de la segunda dimension que seria el "3"
						
$array3d = [   [[0,1,2], [1,1,2]]   ,   [[2,1,2], [3,1,2]]   ] ;

print_r($array3d[0][1][2]); # Mostrariamos el elemento [0] de la primera dimension [[0,1,2], [1,1,2]]
			# Luego mostrariamos el elemento [1] de la segunda dimension [1,1,2]
			# Y por ultimo el elemento [2] de la tercera dimension "2"

```

Se puede operar con lo aprendido hasta ahora, con cualquier tabla multidimensional.

# Creacion de arrays en blanco

Podemos crear una array en blanco. ( Por ejemplo, para rellenar mas tarde )

```php

$array_vacia_1d = [];                      # Crea una array vacia de 1 dimension
$array_vacia_2d = [ [] ];                  # Crea una array vacia de 2 dimensiones
$array_vacia_3d = [ [ [] ] ];              # Crea una array vacia de 3 dimensiones

#Etcétera...

```

# Recopilación de todo lo dado.

```php

<?php

$array_2d_vacia = [[],[]]; # array 2 dimensiones

echo count($array_2d_vacia) . PHP_EOL; # Mostrará que tiene 2 elementos

array_push($array_2d_vacia[0], 4.1, 2); # Agregamos al elemento 0-0 > 4.1 // Agregamos al elemento 0-1 > 2

array_push($array_2d_vacia[1], 'Acruma'); # Agregamos a la ultima posicion del elemnto 1 > 'Acruma'
array_push($array_2d_vacia[1], 'Soy');   # Agregamos a la ultima posicion del elemnto 1 > 'Soy'

$array_2d = $array_2d_vacia;   # Volcar valor a nueva variable

print_r($array_2d); 	# Mostrará [  [4.1, 2]  ,  ['Acruma', 'Soy']  ]

$array_2d[0][1] = 10; # Modificamos 0-1 que tenia de valor "2" a valor "10"

array_pop($array_2d[1]);  # Eliminamos  1-1 que tenia de valor 'Soy'

array_push($array_2d[1], 'te'); # Agregamos a la ultima posicion del elemnto 1 > 'te'
array_push($array_2d[1], 'enseña'); # Agregamos a la ultima posicion del elemnto 1 > 'enseña'
array_push($array_2d[1], 'PHP'); # Agregamos a la ultima posicion del elemnto 1 > 'PHP'

print_r($array_2d);     # [[4.1, 10], ['Acruma', 'te', 'enseña', 'PHP']]

$array_2d_r = array_reverse($array_2d[0]); # Le damos la vuelta al elemento 0 y lo guardamos en otra variable
$array_2d[0] = $array_2d_r;	#Guardamos la variable en el elemento [0] del array original
sort($array_2d[1]); # Ordenamos alfabeticamente el elemento 1

print_r($array_2d); # Mostrará [[10, 4.1], ['Acruma', 'PHP', 'enseña', 'te']] -- ( Mayúsculas primero )

$sub_array_2d = array_slice($array_2d[1], 1, 2);  # Elegimos del elemento 1. Los elementos desde el 1 seleccionamos 2

print_r($sub_array_2d);  # Mostrará ['PHP', 'enseña']

?>

```

By [@acruma](https://github.com/acruma)
