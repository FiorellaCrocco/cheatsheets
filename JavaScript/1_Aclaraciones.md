## ACLARACIONES

### 0) COMENTARIOS

En JavaScript podemos dejar comentarios le las siguientes maneras:

- Comentarios de línea: //texto comentado

- Comentario de bloque: /* bloque de texto comentado, varias líneas */



### 1) TIPOS DE DATOS:
Existen diferentes tipos de datos: los primitivos y los complejos.

**Primitivos**
- Number: 1
- String: "Hola"
- Booleanos: True / False
- Undefined (sin valor agregado)
- Null (vacío o desconocido)
- NaN (Not a Number)

**Complejos**
- Array: [dato, dato, dato]
- Objeto literal: {clave: valor}


### 2) EL SIGNO DE IGUAL

Es el operador de asignación, al poner un signo de igual (=) estamos asignando un valor a una variable.


### 3) SCOPE
El alcance o scope de las funciones y variables se define por { }

*EJEMPLO:*

```
scope 1

function{

    scope 2

    code{

        scope 3

    }
    
}
```


### 4) RETURN 
Una vez que escribimos la palabra reservada "return" se corta  la ejecución del codigo de TODA LA FUNCION, no lee nada que este por debajo. 


### 5) RETURN VS CONSOLE.LOG
Cuando se pide "RETORNAR" hay que utilizar return, esto lo que hace es *mostrar en pantalla*; por otro lado,cuando solicitan "MOSTRAR" se utiliza console.log, esto *muestra por consola*, es decir es una herramienta para el desorrallodor únicamente ya que el usuario no lo verá.

*DATO IMPORTANTE:* si dentro de una función utilizamos un "console.log" a la hora de _invocar_ la función solamente escribimos el nombre de la función (si volvemos a escribir console.log veremos en pantalla _undefined_).

