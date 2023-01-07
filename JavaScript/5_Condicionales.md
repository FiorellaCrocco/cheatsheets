## CONDICIONALES

Son mecanismos de control de flujo, éstos nos permiten evaluar condiciones y realizar diferentes acciones según el resultado de dicha evaluación.

**ESTRUCTURA DEL IF**

*Básica*
```
if (condicion){
    //codigo a ejecutar si se cumple la condicion
}
```
*Opcional*
```
if (condicion){
    //codigo a ejecutar si se cumple la condicion
} else {
    // codigo a ejecutar si la condicion del if anterior no se cumple, es decir si es FALSE.
}
```

*Opcional 2*: Para cuando necesitamos presentar diferentes situaciones segun distintas condiciones
```
if (condicion){
    //codigo a ejecutar si se cumple la condicion
} else if (otra condicion){
    // codigo a ejecutar si la condicion del if anterior no se cumple, es decir si es FALSE.
} else {
    codigo a ejecutar si no cumple ninguna de las condiciones evaluadas en los IF o ELSE IF (si no entro a niungun de ellos)
}
```

*IF TERNARIO*: A diferencia del IF visto anteriormente, en este si hay que poner si o si lo que hace en caso de ser FALSE la condicion, de no querer indicar nada utilizar " " (sting vacío).

```
condicion ? primer expresion : segunda expresion ;
```

primer expresion -> codigo a ejecutar si es TRUE la condicion
segunda expresion --> codigo a ejecutar en caso de ser FALSE la condicion.

**ESTRUCTURA DEL SWITCH**: Permite evaluar muchas posibilidades de un solo valor, para terminar cada escenario utilizamos la palabra reservada BREAK.
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

- Siendo TRUE una condicion:
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
- Siendo FALSE una condicion:
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