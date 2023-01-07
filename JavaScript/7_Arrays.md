## ARRAY

Los arrays (también llamados "Listas" o "Arreglos") nos permiten generar una colección de datos ordenados, agrupados en una sola variable.

Utilizamos corchetes [] para indicar el inicio y el fin de un array. Y usamos comas , para separar sus elementos.
_Dentro de un array, podemos almacenar la cantidad de elementos que queramos, sin importar el tipo de dato de cada uno. Es decir, podemos tener en un mismo array datos de tipo string, number, boolean y todos los demás._

```
let nombreArray = ['Star Wars', true, 23];
```

- Cada dato de un array ocupa una posición numerada conocida como índice. La primera posición de un array es siempre _0_.
- Otra propiedad útil de los arrays es su longitud, o cantidad de elementos. Podemos saber el número de elementos usando la propiedad _length_.
- Para acceder a un elemento puntual de un array, nombramos al array y, dentro de los corchetes, escribimos el índice al cual queremos acceder.

```
let pelisFavoritas = ['Star Wars', 'Kill Bill', 'Alien'];
                        [ 0 ]         [ 1 ]       [ 2 ]


pelisFavoritas.length;
// Devuelve 3, el número de elementos del array

pelisFavoritas[1];
// Devuelve 'Kill Bill', el valor de la posición 1.
```