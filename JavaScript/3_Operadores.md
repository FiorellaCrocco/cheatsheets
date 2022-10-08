## OPERADORES

Los operadores nos permiten manipular el valor de las variables, realizar operaciones y comparar sus valores.

**OPERADOR DE ASIGNACIÓN**

El signo de igual (=); asigna un valor a la variable que tiene a la izquierda.

*EJEMPLO:*

let variable = valor;


**OPERADORES ARITMÉTRICOS**

Devuelven el resultado de operaciones matemáticas como ser: 

- Suma + 

- Resta - 

- Multiplicación *

- División / 

- Incremento ++ 

- Decremento --

- Módulo % (devuelve el resto de la división)

*EJEMPLO:* 

- 2 + 2 ;  // Resultado: 4

- 5 - 2 ;  // Resultado: 3

- 2 * 2 ;  // Resultado: 4

- 6 / 2 ;  // Resultado: 3

- 6++ ;  // Resultado: 7

- 6-- ;  // Resultado: 5

- 6 % 2 ;  // Resultado: 0


**OPERADORES DE CONCATENACIÓN**

Unen cadenas de texto, también permite unir texto con variables, números, etc.

*EJEMPLO:* 

let nombre = "Fiorella";

let apellido = "Crocco"

let nombreCompleto = nombre + " " + apellido // Resultado: Fiorella Crocco


**OPERADORES DE COMPARACIÓN SIMPLE**

Comparan dos valores y devuelve un valor booleano (true o false)

*EJEMPLO:* 

10 == 15 // Resultado: false

10 != 15 // Resultado: true


**OPERADORES DE COMPARACIÓN ESTRICTA**

Comparan dos valores y el tipo de dato de ambos, devuelve un valor booleano (true o false).

*EJEMPLO:* 

10 === '10' // Resultado: false; porque son estamos comparando un 'number' con un 'string'

10 === 10 // Resultado: true

15 > 15 // Resultado: false

10 < 15 // Resultado: true

15 >= 15 // Resultado: true

10 <= 15 // Resultado: true


**RESUMEN**

- Tanto los operadores logicos como los de comparacion (== === != !== > < ) devuelven un valor booleano como resultado.

- La comparacion estricta (===) compara el valor y el tipo de dato, mientras que la debil (==) solo el valor.

- Primero debemos indicar el simbolo de < o > y por ultimo el = (<= o >=) porque si JS lee primero el igual entiende que es una asignacion y luego no sabe como continuar.

- Si JS nos retorna un 0 es porque hay un error de sintaxis (ej. se puso | en vez de ||).

- El operador de comparacion es de mayor prioridad que el operador logico.

- Si por error utilizamos el operador de asignacion (=) en vez del de comparacion (==) recibiremos un error.

- Cuando se comparan strings el == compara velor y el <= compara por orden alfabetico.

- En el caso de comparar strings con el operador && al ser ser ambos strings verdaderos (porque tienen una cadena de caracteres), la respuesta sera el ultimo string de la sentencia (porque recorre toda la sentencia).

- En el caso de comparar strings con el operador || al tener que cumplirse solo una condicion y como ambas son true la respuesta es la primer sentencia encontrada (porque cuando encuentra una sentencia verdader corta la ejecucion y ese valor es el que devuelve).

- El operador && devuelve el primer valor o expresion analizado como false.