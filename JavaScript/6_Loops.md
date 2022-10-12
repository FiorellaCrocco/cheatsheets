## LOOPS

**ESTRUCTURA FOR**

for (inicio; condicion; modificador){
    // Código a ejecutar en cada ejecucion
}

*EJEMPLO:*

```
for (let vuelta = 1; vuelta <= 5; vuelta++) {
  console.log('Dando la vuelta número ' + vuelta);
};
```

La consola mostrara:
Dando la vuelta número 1
Dando la vuelta número 2
Dando la vuelta número 3
Dando la vuelta número 4
Dando la vuelta número 5

** El modificador hace referencia a incrementar (vuelta++) o disminuir (vuelta--) para hacer que en algun momento se deje de cumplir la condicion y eso corte el loop del for.

**BUCLES WHILE Y DO WHILE**

*ESTRUCTURA WHILE:* Tiene una estructura similar a la de los condicionales if/else, palabra reservada + condición entre paréntesis. Sin embargo, el while Loop revalúa esa condición repetidas veces y ejecuta su bloque de código hasta que la condición deja de ser verdadera. En el caso que al inicio esa condicion ya sea falsa no ejecutara ninguna vez ese codigo.

* El WHILE lo utilas siempre que se esté cumpliendo una condición detallada al principio

Definimos variable:

```
while (condicion) {
    // Código que se ejecutará en cada repetición
    // Modificador.. Hace algo para que la condición eventualmente se deje de cumplir
}
```

*EJEMPLO:*

```
let vuelta = 1

while(vuelta <= 5) {
  console.log('Dando la vuelta número ' + vuelta);
  vuelta++ // Al final de cada vuelta sumara 1 a vuelta, asi no quedamos en un loop infinito.
};
```

*ESTRUCTURA DO WHILE:* La condición en este caso se verifica al finalizar el bloque de código. Por lo tanto, sin importar lo que se resuelva (si es TRUE o FALSE), las acciones se realizarán al menos una vez.

* En el DO WHILE vos pones el código que tiene que ejecutarse (sucede por primera vez) y luego llega a revisar si cumple la condición (en caso de que no la cumpla quedó con una sola ejecución).

Definimos variable:

```
do{
    // Código que se ejecutará en cada repetición
    // Hace algo para que la condición eventualmente se deje de cumplir
} while (condicion); 
```

* Si la condicion resulta FALSE no se repite el loop, pero ya se ejecuto una vez; de ser TRUE se repetira el loop.

*EJEMPLO:*

```

let vuelta = 5

do{
  console.log('Dando la vuelta número ' + vuelta);
  vuelta++ // Se suma 1 a vuelta por lo tanto vuelta = 6
} while(vuelta <= 5); // Al vuelta ser 6 la condición retorna false y se termina el bloque de código

```
