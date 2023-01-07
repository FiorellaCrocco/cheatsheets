## FUNCIONES

 La funcion es un bloque de codigo que nos permite resolver una necesidad especifica

 En este caso, al no haber recibido el argumento que necesitaba, JavaScript le asigna el tipo de dato undefined a los parámetros que no recibio. Para que esto no suceda podemos predefinir que mostrar en caso de que quede vacio.

*EJEMPLO:*

function saludar(nombre, apellido) {
	return 'Hola ' + nombre + ' ' + apellido;
}

saludar(); // retorna 'Hola undefined undefined'

function saludar(nombre = 'visitante', 
	apellido = 'anónimo') {
	return 'Hola ' + nombre + ' ' + apellido;
}

saludar(); // retornará 'Hola visitante anónimo'

En caso de querer guardar lo que retorna una función, será necesario almacenarlo en una variable.

**DISTINTOS TIPOS DE FUNCIONES Y SU ESTRUCTURA**

*1) DECLARADA* : alcance global, puede ser usada en lineas previas a ser definida.

        console.log(nombreFuncion("ejemplo")) // en consola veremos: www.ejemplo.com

        function nombreFuncion(nombreVariable){
            return "www." + nombreVariable + ".com" 
        }

*2) EXPRESADA*: tiene un alcance mas local, para ser usada ya debe haber sido definida - es una funcion anonima
EJ: Declaramos la funciones en la linea 10 y la podemos invocar a partir de la linea 11.

        let nombre = function(nombreVariable){
            return nombreVariable * 5;
        }

        console.log(nombre(5)); // en consola veremos: 25

*3) ARROW*: tiene un alcance local, solo podemos usarla en el scope en el que estamos

// Se puede definir la arrow tanto con LET como con CONST.

Hay 3 formas para escribirla:

- CON 0 PARAMETROS Y UNA SOLA LINEA DE CODIGO: Dejamos los parentesis vacios y luego del arrow no ponemos llaves, por eso tampoco return.

let ejemplo = () => "Hola mundo!"

console.log(ejemplo()); // en consola veremos: "Hola mundo!"

- CON 1 PARAMETRO Y UNA SOLA LINEA DE CODIGO: No usamos parentesis y luego del arrow tampoco ponemos llaves ni return.

let ejemplo1 = nombre => "www." + nombre + ".com"

console.log(ejemplo1("juan")); // en consola veremos: www.juan.com

- CON 2 PARAMETROS O MAS: Usamos parentesis para las variables, las mismas se separan por comas. Luego del arrow ponemos llaves y por ultimo el return.

let ejemplo2 = (nombre, apellido) => {
    let edad = 5;
    return nombre + " " + apellido + " tiene " + edad + " años ";
}    

console.log(ejemplo2("juan", "perez")); // en consola veremos: juan perez tiene 5 años

*CODIGO QUE MUESTRA LO VISTO*

let edad = (nombre, apellido) => {
    let edad= 5;
    return nombre + " " + apellido + " tiene " + edad + " años ";
}    

console.log(edad("Juan", "Perez"));


let admirar = frase => frase + "!!!";

console.log(admirar("HOLA"));


let edadPerro = numero => numero * 7;
console.log("La edad del perro es " + edadPerro(5));


Estructura de la arrow (aclaracion)
      let           edadPerro   =   numero  => numero * 7;
 definirVariable nombreVariable = parametro => loQueQuieroHagaLaFuncion
