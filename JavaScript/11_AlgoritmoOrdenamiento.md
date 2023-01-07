## ALGORITMO DE ORDENACIÓN: BUBBLE SORT

En programación, el orden es importante: las computadoras están basadas en números y esto hace muy necesario mantener una estructura matemática —orden—. En muchas ocasiones vamos a necesitar tener nuestros datos ordenados, sobre todo cuando son muchos. Existen muchos métodos —algoritmos— ya creados para lograrlo. El método Bubble Sort, es uno de los más usados.

Lo podemos utilizar tanto para ordenar arrays como objetos literales.

**ARRAY DE NUMEROS**

- APLICADO PARA ORDENAR DE FORMA ASCENDENTE
```
let numeros = [12,1,3,15,7];

let bubbleSortAsc = array => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j] > array[j + 1]){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("************ ORDEN ASC NUMEROS ************");
bubbleSortAsc(numeros);
console.log(numeros);
```
- APLICADO PARA ORDENAR DE FORMA DESCENDENTE
```
let numeros1 = [12,1,3,15,7];

let bubbleSortDesc = array => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j] < array[j + 1]){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("************ ORDEN DESC NUMEROS ************");
bubbleSortDesc(numeros1);
console.log(numeros1);
```

**ARRAY DE LETRAS**

- APLICADO PARA ORDENAR DE FORMA ASCENDENTE
```
let letras = ["c","f","t","b","g"];

console.log("************ ORDEN ASC LETRRAS ************");
bubbleSortAsc(letras);
console.log(letras);
```
- APLICADO PARA ORDENAR DE FORMA DESCENDENTE
```
let letras1 = ["c","f","t","b","g"];

console.log("************ ORDEN DESC LETRAS ************");
bubbleSortDesc(letras1);
console.log(letras1);
```
**ARRAY DE OBJETOS LITERALES**
```
const arrayCuentas = [
    {
        titular: "Arlene Barr",
        estaHabilitada: false,
        saldo: 3253.40,
        edadTitular: 33,
        tipoCuenta: "sueldo"
    },
    {
        titular: "Roslyn Torres",
        estaHabilitada: false,
        saldo: 2229.45,
        edadTitular: 27,
        tipoCuenta: "sueldo"
    },
    {
        titular: "HardingMitchell",
        estaHabilitada: true,
        saldo: 1408.68,
        edadTitular: 25,
        tipoCuenta: "corriente"
    }
]

```
- APLICADO PARA ORDENAR UN ARRAY DE OBJETO LITERAL DE FORMA ASCENDENTE 

_SEGUN VALOR DE LA PROPIEDAD SALDO (NUMERICO)_
```
let bubbleSortObjAsc = (array) => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j].saldo > array[j + 1].saldo){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("************ ORDEN ASC ARRAY DE OBJETO LITERAL - SALDO ************");
bubbleSortObjAsc(arrayCuentas);
console.log(arrayCuentas);
```

- APLICADO PARA ORDENAR UN ARRAY DE OBJETO LITERAL DE FORMA DESCENDENTE 
_SEGUN VALOR DE LA PROPIEDAD TITULAR (STRING)_

```
let bubbleSortObjDesc = (array) => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j].titular < array[j + 1].titular){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("************ ORDEN DESC ARRAY DE OBJETO LITERAL - TITULAR ************");
bubbleSortObjDesc(arrayCuentas);
console.log(arrayCuentas);
```

- APLICADO PARA ORDENAR UN ARRAY DE OBJETO LITERAL DE FORMA ASCENDENTE E INDICANDO A QUE PROPIEDAD ACCEDER PARA ORDENAR (funcion generica de ordenamiento asc)

```
const arrayCuentasGen = [
    {
        titular: "Arlene Barr",
        estaHabilitada: false,
        saldo: 3253.40,
        edadTitular: 33,
        tipoCuenta: "sueldo"
    },
    {
        titular: "Roslyn Torres",
        estaHabilitada: false,
        saldo: 2229.45,
        edadTitular: 27,
        tipoCuenta: "sueldo"
    },
    {
        titular: "HardingMitchell",
        estaHabilitada: true,
        saldo: 1408.68,
        edadTitular: 25,
        tipoCuenta: "corriente"
    }
]
```

```
let bubbleSortObjAscGen = (array, prop) => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j][prop] > array[j + 1][prop]){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("*** ORDEN ASC ARRAY DE OBJETO LITERAL - PROP. INDICADA / EDAD ***");
bubbleSortObjAscGen(arrayCuentasGen, "edadTitular");
console.log(arrayCuentasGen);
```

- APLICADO PARA ORDENAR UN ARRAY DE OBJETO LITERAL DE FORMA DESCENDENTE E INDICANDO A QUE PROPIEDAD ACCEDER PARA ORDENAR (funcion generica de ordenamiento desc)

```
let bubbleSortObjDescGen = (array, prop) => {  
    let aux;
    for (let i = 0; i < array.length; i++) {     
        for (let j = 0; j < array.length - 1; j++) {       
            if ( array[j][prop] < array[j + 1][prop]){
                aux = array[j];
                array[j] = array[j + 1];
                array[j + 1] = aux;
            }
        }       
    }
}

console.log("*** ORDEN DESC ARRAY DE OBJETO LITERAL - PROP. INDICADA / EDAD ***");
bubbleSortObjDescGen(arrayCuentasGen1, "edadTitular");
console.log(arrayCuentasGen1);
```

- APLICADO PARA ORDENAR UN ARRAY DE OBJETO LITERAL DE FORMA ASCENDENTE O DESCENDENTE SEGUN EL USUARIO INDICA COMO ORDENAR (funcion generica de ordenamiento segun criterio asc o desc)

```
const person = 
[
    {
        nombre: "Arlene Barr",
        legajo: 3955,
    },
    {
        nombre: "Roslyn Torres",
        legajo: 3925,
    },
            {
        nombre: "Cleo Lopez",
        legajo: 1965,
    },
    {
        nombre: "Daniel Malone",
        legajo: 3525, //3925
            },
    {
        nombre: "Ethel Leon",
        legajo: 1915,
    },
    {
        nombre: "Harding Mitchell",
        legajo: 1905,
    }
]

```

```
const ordenar = (array, orden) => {
    let aux = [];
    if (orden === "Ascendente" || orden === "ascendente") {
        for(let i = 0; i < array.length; i++){
            for (let j = 0; j < array.length-1; j++) {
                if (array[j].legajo > array[j + 1].legajo) {
                    aux = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = aux;
                }   
            }
        }
    } else if (orden === "Descendente" || orden === "descendente"){
        for(let i = 0; i < array.length; i++){
            for (let j = 0; j < array.length-1; j++) {
                if (array[j].legajo < array[j + 1].legajo) {
                    aux = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = aux;
                }   
            }
        }
    } 
}

console.table(person); 
ordenar(person, "Ascendente")
console.table(person);
```
