# Ejercicios básicos resueltos en BASH.

**1.-** Imprima en pantalla la cadena de caracteres "¡Hola, mundo!" .

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-1-)

**2.-** Inicializa una variable (crea una variable y dale un valor) de tipo número real e imprimela por pantalla.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-2-)

**3.-** Inicializa dos variables (de tipo número entero) con identificadores `edad` y `altura`, e imprímerlas junto en el mensaje: Tengo `edad` años y mido `altura` cm.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-3-)

**4.-** Inicializa cuatro variables, una de cada tipo de variable básico, e imprímelas todas en un mismo mensaje indicando cual es cual.
> Opcional - Cada una debe aparecer en una línea distinta (consejo usa \n).

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-4-)

**5.-** Inicializa 2 variables de tipo número entero y súmalos en una tercera variable. Imprime en pantalla esta última.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-5-)

**6.-** Inicializa una variable `radio` y calcula la circunferencia guardando el resultado en la variable `circunferencia`. 
**Fórmula: 2 · п · radio**. A posteriori imprime en pantalla `circunferencia`

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-6-)

**7.-** Inicializa una variable `radio` y calcula el área de un círculo guardando el resultado en la variable `area`. **Fórmula: п · radio · radio**. A posteriori imprime en pantalla `area`

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-7-)

**8.-** Convierte una variable con identificador `latitud` de tipo **cadena de caracteres** y con valor -234.62 a tipo número real. Réstale a la variable el valor 21.34 e imprime finalmente dicha variable.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-8-)

**9.-** Inicializa una variable `celsius`, calcula su equivalente a grados Fahrenheit guardando el resultado en la variable `fahrenheit` e ímprimelo por pantalla. **Fórmula: fahrenheit = (celsius * 1.8) + 32**.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-9-)

**10.-** Inicializa una variable `fahrenheit`, calcula su equivalente a grados Celsius guardando el resultado en la variable `celsius` e ímprimelo por pantalla. **Fórmula: celsius = (fahrenheit - 32) / 1.8**.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicio-10-)


> A continuación verás los ejercicios corregidos, son un ejemplo de como hacerlos, pues hay más de una forma.

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 1
---
---
---
# Ejercicio 1.-

Imprima en pantalla la cadena de caracteres "¡Hola, mundo!" .

```bash

echo "¡Hola, mundo!"

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 2
---
---
---
# Ejercicio 2.-

Inicializa una variable (crea una variable y dale un valor) de tipo número real e imprimela por pantalla.

```bash

x=123.2
echo $x

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 3
---
---
---
# Ejercicio 3.-

Inicializa dos variables (de tipo número entero) con identificadores `edad` y `altura`, e imprímerlas junto en el mensaje: Tengo `edad` años y mido `altura` cm.

```bash

edad=18
altura=185
echo "Tengo $edad años y mido $altura cm."

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 4
---
---
---
# Ejercicio 4.-

Inicializa cuatro variables, una de cada tipo de variable básico, e imprímelas todas en un mismo mensaje indicando cual es cual.
> Opcional - Cada una debe aparecer en una línea distinta (consejo usa \n).

```bash

integer=1
double=-10.1
string="Holaaa"
boolean=true
echo -e "$integer \n$double \n$string \n$boolean"
#Recordemos que tecnicamente TODO son "string"

```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 5
---
---
---
# Ejercicio 5.-

Inicializa 2 variables de tipo número entero y súmalos en una tercera variable. Imprime en pantalla esta última.

```bash

x=1
y=10
let z=$x+$y
echo $z

```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 6
---
---
---
# Ejercicio 6.-

Inicializa una variable `radio` y calcula la circunferencia guardando el resultado en la variable `circunferencia`. 
**Fórmula: 2 · п · radio**. A posteriori imprime en pantalla `circunferencia`

```bash

radio=11
circunferencia=$(bc -l <<< " 2 * 3.14 * $radio")
echo $circunferencia

```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 7
---
---
---
# Ejercicio 7.-

Inicializa una variable `radio` y calcula el área de un círculo guardando el resultado en la variable `area`. **Fórmula: п · radio · radio**. A posteriori imprime en pantalla `area`

```bash

radio=10
area=$(bc -l <<< " 3.14 * $radio * $radio")
echo $area

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 8
---
---
---
# Ejercicio 8.-

Convierte una variable con identificador `latitud` de tipo **cadena de caracteres** y con valor -234.62 a tipo número real. Réstale a la variable el valor 21.34 e imprime finalmente dicha variable.

```bash

#No podemos convertir, ya que BASH, solo reconoce strings (todos los datos los guarda como cadena de caracteres)

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 9
---
---
---
# Ejercicio 9.-

Inicializa una variable `celsius`, calcula su equivalente a grados Fahrenheit guardando el resultado en la variable `fahrenheit` e ímprimelo por pantalla. **Fórmula: fahrenheit = (celsius * 1.8) + 32**.

```bash

celsius=23
fahrenheit=$(bc -l <<< "($celsius * 1.8) + 32")
echo $fahrenheit

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 10
---
---
---
# Ejercicio 10.-

Inicializa una variable `fahrenheit`, calcula su equivalente a grados Celsius guardando el resultado en la variable `celsius` e ímprimelo por pantalla. **Fórmula: celsius = (fahrenheit - 32) / 1.8**.

```bash

fahrenheit=73.4
celsius=$(bc -l <<< "($fahrenheit - 32) / 1.8")
echo $celsius

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/bash.md#ejercicios-b%C3%A1sicos-resueltos-en-bash)
