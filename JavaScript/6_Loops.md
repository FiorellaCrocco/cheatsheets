## LOOPS

Los ciclos (loops) son una serie de estados por los que pasa un acontecimiento o fenómeno, que se repiten siempre en el mismo orden. En programación, para hacer que nuestro código se siga ejecutando mientras una condición se cumpla, utilizamos los ciclos.

**FOR** 

for (inicio; condicion; modificador){
    //codigo a ejecutar en cada ejecucion
}

EJEMPLO:

for (let vuelta = 1; vuelta <= 5; vuelta++) {
  console.log('Dando la vuelta número ' + vuelta);
};

La consola mostrara:
Dando la vuelta número 1
Dando la vuelta número 2
Dando la vuelta número 3
Dando la vuelta número 4
Dando la vuelta número 5

*El modificador hace referencia a incrementar (vuelta++) o disminuir (vuelta--) para hacer que en algun momento se deje de cumplir la condicion y eso corte el loop del for.*

**BUCLES WHILE Y DO WHILE**

*ESTRUCTURA WHILE:*
Tiene una estructura similar a la de los condicionales if/else, palabra reservada más la condición entre paréntesis. Sin embargo, el while Loop revalúa esa condición repetidas veces y ejecuta su bloque de código hasta que la condición deja de ser verdadera. En el caso que al inicio esa condicion ya sea falsa no ejecutara ninguna vez ese codigo.
*El WHILE lo utilas siempre que se esté cumpliendo una condición detallada al principio*

// definimos variable
while (condicion) {
    //código que se ejecutará en cada repetición
    // Hace algo para que la condición eventualmente se deje de cumplir
}

*EJEMPLO:*

let vuelta = 1
while(vuelta <= 5) {
  console.log('Dando la vuelta número ' + vuelta);
  vuelta++ //al final de cada vuelta sumara 1 a vuelta, asi no quedamos en un loop infinito.
};

*ESTRUCTURA DO WHILE:* La condición en este caso se verifica al finalizar el bloque de código. Por lo tanto, sin importar lo que se resuelva (si es TRUE o FALSE), las acciones se realizarán al menos una vez.
*El DO WHILE vos pones el código que tiene que suceder (se ejecuta por primera vez) y luego llega a revisar si cumple la condición (en caso de que no la cumpla quedó con una ejecución)*

// definimos variable
do{
    //código que se ejecutará en cada repetición
    // Hace algo para que la condición eventualmente se deje de cumplir
} while (condicion); //si la condicion resulta FALSE no se repite el loop, pero ya se ejecuto una vez; de ser TRUE se repetira el loop.

*EJEMPLO:*

let vuelta = 5
do{
  console.log('Dando la vuelta número ' + vuelta);
  vuelta++ //Se suma 1 a vuelta por lo tanto vuelta = 6
} while(vuelta <= 5); //al vuelta ser 6 la condición retorna false y se termina el bloque de código
