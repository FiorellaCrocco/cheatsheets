## CONDICIONALES

Los mismos nos permiten evaluar condiciones y realizar diferentes acciones según el resultado de esas evaluaciones.

**ESTRUCTURA DEL IF**

*Estructura basica*

if (condicion){
    // Código a ejecutar si se cumple la condicion
}

*Estructura opcional*

if (condicion){
    // Código a ejecutar si se cumple la condicion
} else {
    // Código a ejecutar si la condicion del if anterior no se cumple, es decir si es FALSE.
}

*Otra opción de estructura, para cuando necesitamos presentar diferentes situaciones segun distintas condiciones*

if (condicion){
    //Código a ejecutar si se cumple la condicion
} else if (otra condicion){
    // Código a ejecutar si la condicion del if anterior no se cumple, es decir si es FALSE.
} else {
    // Código a ejecutar si no cumple ninguna de las condiciones evaluadas en los IF o ELSE IF (si no entro a niungun de ellos)
}

**ESTRUCTURA DEL IF TERNARIO** 

A diferencia del IF visto anteriormente, en éste si hay que poner _si o si_ lo que hace en caso de ser FALSE la condicion. De no querer indicar nada utilizar " " (sting vacio).

Primer expresion -> Código a ejecutar si es TRUE la condicion
Segunda expresion --> Código a ejecutar en caso de ser FALSE la condicion.

condicion ? primer expresion : segunda expresion ;

**SWITCH** 

Permite evaluar muchas posibilidades de un solo valor, para terminar cada escenario utilizamos la palabra reservada BREAK.
Las palabras reservadas son: switch, case, y break.

```
switch(expresion){
    case valorA:
        //codigo a ejecutar;
        break;
    case valorB:
        //codigo a ejecutar;
        break;
    case valorC:
        //codigo a ejecutar;
        break;
}
```

*EJEMPLOS:*

**A)** Siendo TRUE una condición.

```
let edad = 5;

switch (edad) {
	case 10: //En este caso, preguntamos si el valor de la variable edad es 10. Como este caso NO es verdadero, JavaScript ignora el código de este caso y pasa a evaluar el siguiente.
    	console.log('Tiene 10 años');
    	break; // La palabra reservada break corta la ejecución del switch. 
    case 5:
    	console.log('Tiene 5 años');
    	break;
}
```

**B)** Siendo FALSE una condición.

```
let fruta = 'wefwef';

switch (fruta) {
	case 'manzana':
    	console.log('Qué rica la manzana');
    	break;
case 'naranja':
    	console.log('¡Naranja, me encanta!');
    	break;
default: //en este caso no es necesario escribir el break.
    	console.log('¿Qué fruta es?');  // código a ejecutar si ningún caso es verdadero
}

```