## ALGORITMO DE BÚSQUEDA: LINEAR SEARCH Y BINARY SEARCH 
Estos nos ayudan a encontrar elementos dentro de un array.

**LINEAR SEARCH**
Busca elemento por elemento, uno por vez y no para hasta encontrar el valor deseado.

```
function search(arr, n, x)
{
    let i;
    for (i = 0; i < n; i++)
        if (arr[i] == x)
            return i;
    return -1;
}
```

**BINARY SEARCH**
```
Lo primero que vamos a hacer para escribir este algoritmo, es crear una función que nos permita tomar dos parámetros: 
La lista sobre la que vamos a buscar y el elemento que vamos a buscar.

const binarySearch = (list, item) => {
  // punto mas bajo
  let low = 0;
  // punto mas alto
  let high = list.length - 1;
 
  // mientras que low sea menor o igual que high
  while (low <= high) {
    // encontramos la mitad entre low y high
    const mid = Math.floor((low + high) / 2);
 
    // adivinar si el valor es el de la mitad
    const guess = list[mid];

   // si es asi, retornar esa posicion
    if (guess === item) {
      return mid;
    }
    // si lo propuesto es mayor que lo que estamos buscando
    if (guess > item) {
      //
      high = mid - 1;
    } else {
      low = mid + 1;
    }
  }
 
  return null; // si no encontramos nada
 
};

let list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11];
let buscar = 1;
console.log(binarySearch(list, buscar));
```

*El código anterior nos indica que:*
Si el número de la mitad es el que estamos buscando, retornarlo.
Si no, vamos a hacer que la punta baja sea ese número y volveremos a buscar la mitad.
Repetimos el proceso anterior hasta encontrar el número.


