## MATRICES

Es una estructura de datos que almacena datos de forma bidimensional. Es decir, es un array que guarda otros arrays.

**FORMAS DE RECORRERLAS**
Tenemos 4 posibles formas de hacerlo: Recorrer solo una fila, solo una columna, recorrerla por filas o recorrerla por columnas.

**ESTRUCTURA**
```
let matrix = [
*columna:  0   1   2   3   4   5   6   7*
          [14, 12, 17, 41, 55, 13, 40, 3], // *0  = 1er fila*
          [55, 16, 61, 23, 50, 12, 41, 2], // *1  = 2da fila*
          [13, 22, 13, 32, 51, 11, 42, 1], // *2  = 3er fila*
          [12, 61, 18, 23, 52, 10, 43, 5], // *3  = 4ta fila*
];
```
**ES IMPORTANTE RECORDAR:**
 Para acceder a una ubicacion en una matriz debemos indicar: **MATRIZ[fila][columna]**.
 Considerar que si piden la SEGUNDA FILA va ser el indice 1 -> Ej.: MATRIZ[1][columna].
 De pedir la PRIMER COLUMNA es indice 0 -> Ej.: MATRIZ[fila][0].
 Solo se puede pedir la diagonal _en una matriz cuadrada_ es decir misma cantidad de filas y columnas.

*UN SOLO CICLO FOR SE USA PARA:*
- RECORRER UNA FILA => LE PIDO LA LONGITUD A ESA FILA
- RECORRER UNA COLUMNA => LE PIDO LA LONGITUD A LA MATRIZ
- RECORRER DIAGONAL PRINCIPAL => LE PIDO LA LONGITUD A LA MATRIZ
- RECORRER DIAGONAL SECUNDARIA => LE PIDO LA LONGITUD A LA MATRIZ

*DOBLE FOR SE USA PARA:*
- RECORRER MATRIZ COMPLETA


**EJECUCIÓN**

**1 - RECORRER UNA FILA**

- En caso de que nos indiquen la fila a recorrer --> Ej.: Segunda fila -> [55, 16, 61, 23, 50, 12, 41, 2]
```
let valoresFila = (array) => {
    valores=[];
    for (let i = 0; i < array[1].length; i++) { // si no ponemos array[numFila] nos va devolver menos valores (los de la cantidad de filas que haya)
        valores.push(array[1][i])
    }
    return valores;
}

let segundaFila = valoresFila(matrix);
console.log(segundaFila);
```
- En caso de que el usuario sea quien ingrese el N° de fila
```
const recorrerFila = (matriz, fila) => {
    for (let i = 0; i < matriz.length; i++) {       
        matriz[fila][i];
    }
}

recorrerFila(matrix, columna);
```
**2 - RECORRER UNA COLUMNA**

- En caso de que nos indiquen la columna a recorrer --> Ej.: Tercera columna --> [17, 61, 13, 18]
```
let valoresColumna = (array) => {
    for (let i = 0; i < array.length; i++) {
        valores.push(array[i][2])
    }
    return valores;
}

let tercerColumna = valoresColumna(matrix);
console.log(tercerColumna);
```
- En caso de que el usuario sea quien ingrese el N° de columna
```
const recorrerColumna = (matriz, columna) => {
    for (let i = 0; i < matriz.length; i++) {       
        matriz[i][columna]
    }
}

recorrerColumna(matriz, columna);
```
**3 - RECORRER DIAGONAL PRINCIPAL**

Ejemplo para comprender que es la diagonal principal
```
let matrix2 = [
    [14, 12, 17, 41], // 0
    [55, 16, 61, 23], // 1
    [13, 22, 13, 32], // 2
    [12, 61, 18, 23], // 3
]

let DIAGONAL_PRINCIPAL = [14,     16,     13,     23]; 
//                      [0][0], [1][1], [2][2], [3][3]*/
// El patron sería [i][i].

const diagonalPrincipal = matriz => {
    for (let i = 0; i < matriz.length; i++) { 
        matriz[i][i];
    }
}

let diagPrincipal = diagonalPrincipal(matrix2);
console.log( diagPrincipal )
```

*** RECORRER DIAGONAL SECUNDARIA ***

- Ejemplo para comprender que es la diagonal secundaria
```
let matrix2 = [
    [14, 12, 17, 41], // 0
    [55, 16, 61, 23], // 1
    [13, 22, 13, 32], // 2
    [12, 61, 18, 23], // 3
]
```
```
let DIAGONAL_SECUNDARIA = [41,61,22,12];
//(fila)(columna)
//  i  j
// [0][3],   
// [1][2],
// [2][1],
// [3][0]

// i++
// j--

// El patrón sería: [i][array.lenght - i - 1] 
//                  [3]          4   - 3 - 1  = 0 (con esto accedimos a: matrix2[3][0])
*/

const diagonalSecundaria = matriz => {
    for (let i = 0; i < matriz.length; i++) {      
        matriz[i][matriz.length - i - 1]
    }
}

let diagSecundaria = recorrerDiagonalSecundaria(matrix2);
console.log( diagSecundaria )
```

**CREAR MATRIZ**
```
const generarMatriz = (filas, columna) => {
    let matriz = [];
    let cont = 1;
    for (let i = 0; i < filas; i++) {
        matriz.push([]);
     
        for (let j = 0; j < columna; j++) {
            matriz[i].push(cont++);
        }
    }
    return matriz;
}

let matGenerada = generarMatriz(4,8);
console.table(matGenerada);
```