## FUNCIONES

La funcion es un bloque de codigo que nos permite resolver una necesidad especifica
Al momento de crear una función decidimos si tendrá uno, dos o más, o ningún parámetro. 

** Un parámetros es una variable que es utilizada para recibir valores de entrada; una vez que invocamos la función tenemos que parle los valores que verdaderamente utilizará, los mismos se llaman "argumentos".

*EJEMPLO:*

function saludar(nombre, apellido) {
	return 'Hola ' + nombre + ' ' + apellido;
}

saludar(); // Retorna 'Hola undefined undefined' porque no le pasamos como argumentos ningún nombre ni apellido.

En este caso, al no haber recibido el argumento que necesitaba, JavaScript le asigna el tipo de dato undefined a los parámetros que no recibio. Para que esto no suceda podemos predefinir que mostrar en caso de que quede vacio.

* Los parámetros son "nombre" y "apellido".

```

saludar("Fiorella", "Crocco");

```

Retorna 'Hola Fiorella Crocco'; porque pasamos "Fiorella", "Crocco" como argumentos.

```
function saludar(nombre = 'visitante', 
	apellido = 'anónimo') {
	return 'Hola ' + nombre + ' ' + apellido;
}

saludar(); // retornará 'Hola visitante anónimo'

```

En caso de querer guardar lo que retorna una función, será necesario almacenarlo en una variable.

## DISTINTOS TIPOS DE FUNCIONES Y SU ESTRUCTURA

**1) DECLARADA:** Tiene un alcance global, puede ser usada en lineas previas a ser definida.

```

    console.log(nombreFuncion("ejemplo")) // en consola veremos: www.ejemplo.com

    function nombreFuncion(nombreVariable){
        return "www." + nombreVariable + ".com" 
    }

```

**2) EXPRESADA:** Tiene un alcance mas local, para ser usada ya debe haber sido definida; es una funcion anónima.

EJ: Declaramos la funciones en la linea 10 y la podemos invocar a partir de la linea 11.

```

    let nombre = function(nombreVariable){
        return nombreVariable * 5;
    }

    console.log(nombre(5)); 

```

En consola veremos: 25.

**3) ARROW:** Tiene un alcance local, solo podemos usarla en el scope en el que estamos.

Estructura de la arrow (aclaracion)
      let           edadPerro   =   numero  => numero * 7;
 definirVariable nombreVariable = parametro => loQueQuieroHagaLaFuncion

La misma se puede definir tanto con LET como con CONST; hay 3 formas para escribir este tipo de función:

*A) CON 0 PARAMETROS Y UNA SOLA LINEA DE CODIGO:* Dejamos los paréntesis vacios y luego del arrow no ponemos llaves, por eso tampoco return.

```
let ejemplo = () => "Hola mundo!"

console.log(ejemplo()); 

// En consola veremos: "Hola mundo!"

```

*B) CON 1 PARAMETRO Y UNA SOLA LINEA DE CODIGO:* No usamos paréntesis y luego del arrow tampoco ponemos llaves ni return.

```
let ejemplo1 = nombre => "www." + nombre + ".com"

console.log(ejemplo1("juan")); 

// En consola veremos: www.juan.com

```

*C) CON 2 PARAMETROS O MAS:* Usamos paréntesis para las variables, las mismas se separan por comas. Luego del arrow ponemos llaves y por ultimo el return.

```

let ejemplo2 = (nombre, apellido) => {
    let edad = 5;
    return nombre + " " + apellido + " tiene " + edad + " años ";
}    

console.log(ejemplo2("juan", "perez")); 

// En consola veremos: juan perez tiene 5 años

```


```
let admirar = frase => frase + "!!!";

console.log(admirar("HOLA"));

```

```
let edadPerro = numero => numero * 7;

console.log("La edad del perro es " + edadPerro(5));

```
