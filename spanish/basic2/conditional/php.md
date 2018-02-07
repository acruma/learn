# Aprenda sobre Condicionales en PHP

# Indice

[Operadores de Comparación](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#operadores-de-comparaci%C3%B3n)

[Operador AND](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#operador-and)

[Operador OR](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#operador-or)

[Operador NOT](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#operador-not)

[Combinaciones de operadores](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#combinaciones-de-operadores)

[Sentencia IF](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#sentencia-if)

[Sentencia IF + ELSE](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#sentencia-if--else)

[Sentencias IF anidadas](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#sentencias-if-anidadas)

[Recopilación](https://github.com/acruma/learn/blob/master/spanish/basic2/conditional/php.md#recopilaci%C3%B3n)

# Operadores de Comparación

Para comparar dos variables vamos a usar unos operadores, el resultado de estas comparaciones se devuelven en True o False

```php

$x = 5;
$y = 3;

$z = $x === $y;   // $x es igual y del mismo tipo de dato a $y  		Resultado: False
$z = $x !== $y;   // $x no es igual O no es del mismo tipo de dato a $y  	Resultado: True
$z = $x > $y;     // $x es MAYOR que $y			             		Resultado: True
$z = $x >= $y;    // $x es MAYOR o IGUAL que $y				 	Resultado: True
$z = $x < $y;     // $x es MENOR que $y		                		Resultado: False
$z = $x <= $y;    // $x es MENOR o IGUAL que $y				    	Resultado: False

```

# Operador `AND`

El operador `and` en php `&&`, sirve para comprobar dos o más comparaciones y que se cumplan todos.

```php

$f = false;
$t = true;

$z = $f && $f;         // Resultado: False         (false && false) --> false
$z = $f && $t;         // Resultado: False         (false && true)  --> false
$z = $t && $f;         // Resultado: False         (true  && false) --> false
$z = $t && $t;         // Resultado: True          (true  && true)  --> true

```

# Operador `OR`

El operador `or` en php `||`, sirve para comprobar dos o más comparaciones y que se cumpla al menos uno.

```php

$f = false;
$t = true;

$z = $f || $f;         // Resultado: False         (false || false) --> false
$z = $f || $t;         // Resultado: True          (false || true)  --> true
$z = $t || $f;         // Resultado: True          (true  || false) --> true
$z = $t || $t;         // Resultado: True          (true  || true)  --> true

```

# Operador `NOT`

El operador `not` invierte el valor de true a false y viceversa.

```php

$f = false;
$t = true;

$z = !$f;             // Resultado: True           !(false) --> true
$z = !$t;             // Resultado: False          !(true)  --> false

```

# Combinaciones de operadores

Con lo dado hasta ahora, podemos hacer cualquier combinacioón que queramos, aquí os dejo un ejemplo.

```php

$a = 5;
$b = 3;

$z = !($a === $b) || ($a >= $b && $a !== $b);             

		// True   ||  True  Resultado: True

```

# Sentencia `IF`

`IF` significa `SI (condicional)` en español. Su funcionamiento es simple. Se evalúa una condición, si es verdadera ejecuta un código, si es falsa, ejecuta otro código (o continúa con la ejecución del programa).

Ejemplo. Como, `$variable` es mayor a 3 se mostrará el siguiente mensaje.

```php

$variable = 5;

if ($variable > 3){
	echo $variable . " es mayor a 3";
}

```

Ejemplo. Como `$variable` es menor a 10, se continuará el programa sin imprimir nada.

```php

$variable = 5;

if ($variable > 10){
	echo $variable . " Es mayor a 10";
}

```

# Sentencia `IF + ELSE`

Como hemos visto hasta ahora si `if` era false, continuaba con el codigo, pero si añadimos la sentencia `else`, siempre que el resultado de `if` sea falso se ejecutará el interior de `else`.

Ejemplo. Como `$variable` es menor a 10, imprimirá el contenido de `else`.

```php

$variable = 5;

if ($variable > 10) {
    echo $variable . " Es mayor a 10";
} else {
    echo $variable . " Es menor a 10";
}

```

# Sentencias `IF` anidadas.

Una sentencia IF anidada sirve para comprobar todos los casos que tengamos previstos en una ejecucion. Y puede acabar con un `else` o no.

```php

$variable = 5;

if ($variable === 5) {
    echo $variable . " Es igual a 5";
} elseif ($variable < 5) {
    echo $variable . " Es menor a 5";
} elseif ($variable >= 6 && $variable <= 10) {
    echo $variable . " vale entre 6 y 10";
} // y un largo ETCÉTERA...

```

# Recopilación

```php

<?php

$x = 5;
$y = 3;

$z = $x === $y;   // $x es igual y del mismo tipo de dato a $y  		Resultado: False
$z = $x !== $y;   // $x no es igual O no es del mismo tipo de dato a $y  	Resultado: True
$z = $x > $y;     // $x es MAYOR que $y			             		Resultado: True
$z = $x >= $y;    // $x es MAYOR o IGUAL que $y				 	Resultado: True
$z = $x < $y;     // $x es MENOR que $y		                		Resultado: False
$z = $x <= $y;    // $x es MENOR o IGUAL que $y				    	Resultado: False

$f = false;
$t = true;

$z = $f && $f;         // Resultado: False         (false && false) --> false
$z = $f && $t;         // Resultado: False         (false && true)  --> false
$z = $t && $f;         // Resultado: False         (true  && false) --> false
$z = $t && $t;         // Resultado: True          (true  && true)  --> true

$z = $f || $f;         // Resultado: False         (false || false) --> false
$z = $f || $t;         // Resultado: True          (false || true)  --> true
$z = $t || $f;         // Resultado: True          (true  || false) --> true
$z = $t || $t;         // Resultado: True          (true  || true)  --> true

$z = !$f;             // Resultado: True           !(false) --> true
$z = !$t;             // Resultado: False          !(true)  --> false

$a = 5;
$b = 3;

$z = !($a === $b) || ($a >= $b && $a !== $b);             

		// True   ||  True  Resultado: True
		
$variable = 5;

if ($variable > 3){
	echo $variable . " es mayor a 3";
}

if ($variable > 10){
	echo $variable . " Es mayor a 10";
}

if ($variable > 10) {
    echo $variable . " Es mayor a 10";
} else {
    echo $variable . " Es menor a 10";
}

if ($variable === 5) {
    echo $variable . " Es igual a 5";
} elseif ($variable < 5) {
    echo $variable . " Es menor a 5";
} elseif ($variable >= 6 && $variable <= 10) {
    echo $variable . " vale entre 6 y 10";
} // y un largo ETCÉTERA...

?>

```
