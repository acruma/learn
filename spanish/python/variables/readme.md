Antes de entrar en materia, debemos saber la definición de variable.

Variable ; En programación, las variables son espacios reservados en la memoria que, como su nombre indica, pueden cambiar de contenido a lo largo de la ejecución de un programa, incluso de un tipo de dato diferente al que tenía previamente.

Una variable sería como la unidad minima con la que se trabaja en programación. En este apartado le daremos a las variables los tipos de datos  más usuales. Más adelante conforme avance en el tutorial descubrirá otro tipos de datos mas complejos. Igualmente puede ir al apartado [Tipo de datos]() donde encontrará todos los tipos de datos que puede usar.

***

En programación es muy util comentar conforme se escribe nuestro programa, para ello, en Python podemos usar dos formas.

Comentarios de una sola línea usando el caracter reservado `#` o podemos hacerlo en varias lineas abriendo y cerrando con `'''`

 ```Python
 #Esto es un comentario

 '''
 Esto es un comentario
 en múltiples líneas 
 '''
 ```
 
 ***
 
 Y ahora... empecemos con las Variables mas básicas.

 ### Variables
 
 Como en cualquier lenguage hay que seguir una sintaxis especifica del mismo. La sintaxis en Python es la siguiente;
 
Debemos identificar con un nombre dicha variable. El nombre que le demos a la variable no puede verse cambiada a lo largo del programa, porque si se cambia, pasaria a ser literalmente una variable distinta.

Una vez nombrada la igualaremos con el simbolo `=` y a continuación le asignaremos un valor.
  
```Python
# identificador = valor       (EJ;)
     altura     =  100        #El valor "100" se le asigna a la variable "altura"	
```

Los cuatro tipos más básicos de variables son los que siguen. Aunque en Python no hay que señalar que tipo de dato le vas a asignar a una variable, no obstante es muy importante saber con que tipo de dato estamos trabajando para poder operar con ellos.

Integer  - [Número entero]()

Float    - [Número real]()

String   - [Cadena de caracteres]()

Boolean  - [Dato lógico]()

```Python
edad = 34 	#"Integer" (numeros enteros)
recorrido = 132.23   	#"Float"  (numeros reales)
nombre = "Acruma"    	#"String"  (cadena de caracteres)
comparativas = True 	#"Boolean" (valores "True" o "False")
```

***

### Estructura e impresiones en pantalla

Hay que saber estructurar correctamente un programa para que se ejecute en el orden que deseemos. Para ello, debemos saber como se recorre nuestro codigo cuando se esta ejecutando. Es bastante simple, el codigo se ejecuta de la misma manera en que nosotros leemos, es decir... De arriba a abajo, sabiendo que cada LINEA de codigo corresponde a una interacción.

Ejemplo;

```Python
edad = 34     # Esta es la primera linea que se va a ejecutar. En este caso, como en las demas lineas...
recorrido = 132.23   	# ... Tan solo estamos asignando valores a variables ...
nombre = "Acruma"    	
comparativas = True 	# ... Y esta será la ultima linea en ejecutarse.
```

Para poder ver en pantalla los valores que deseemos, usaremos la funcion `PRINT()` que funciona de la siguiente manera;

```Python
print( VALOR A MOSTRAR )
```
Ejemplos;

```Python
print("Esto es una frase") #Se mostrará en pantalla "Esto es una frase"
print(edad)		 #Se mostrará en pantalla la variable "edad"
```
Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con una coma ","

```Python
print(edad, " ", nombre)
#Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"
```

***

### Operaciones aritméticas con números
