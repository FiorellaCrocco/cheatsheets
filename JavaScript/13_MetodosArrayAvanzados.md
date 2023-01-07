##  MÉTODOS AVANZADOS DE ARRAY

Para poder utilizar estos métodos es necesario tener bien presente la definición de _callback_. 
Como ya sabemos, las funciones pueden recibir uno o más parámetros. En caso de recibirlos, estos pueden ser un número, un string, un booleano o también una función. 
*Cuando un método o función recibe a una función como parámetro, a esa función se la conoce como callback.*

La cantidad de métodos disponibles es muy grande y variada, por tanto nosotros nos enfocaremos en los que consideramos son los más importantes y utilizados en la actualidad. Estos son: map, filter, reduce, forEach.

**map**
Este método recibe una función como parámetro (callback).
Recorre el array y devuelve un nuevo array modificado.
Las modificaciones serán aquellas que programemos en nuestra función de callback.

```
array.map(function(elemento){
   // definimos las modificaciones que queremos
   // aplicar sobre cada elemento del array
});
```

*Ejemplo:*
```
const numeros = [2, 4, 6];
const numerosMultiplicados = numeros.map(function(num){
    // Multiplicamos por 2 cada número
    return num * 2;
});

console.log(numerosMultiplicados); // [4,8,12]
```


**filter**
Este método también recibe una función como parámetro. 
Recorre el array y filtra los elementos según una condición que exista en el callback. 
Devuelve un nuevo array que contiene únicamente los elementos que hayan cumplido con esa condición. Es decir, que nuestro nuevo array puede contener menos elementos que el original.
```
array.filter(function(elemento){
    // definimos la condición que queremos utilizar
    // como filtro para cada elemento del array
});
```

*Ejemplo:*
```
var edades = [22, 8, 17, 14, 30];
var mayores = edades.filter(function(edad){
   return edad > 18;
});

console.log(mayores); // [22, 30]
```


**reduce**
Este método recorre el array y devuelve un único valor. 
Recibe un callback que se va a ejecutar sobre cada elemento del array. Este, a su vez, recibe cuatro argumentos: un acumulador, elemento actual, índice actual y array que esté recorriendo.

```
array.reduce(function(acumulador, elemento, índice, array){
    // definimos el comportamiento que queremos
    // implementar sobre el acumulador y el elemento
	// podemos indicar el valor inicial que por defecto es 0
}, 0);
```

*Ejemplo:*
```
var nums = [5, 7, 16];
var suma = nums.reduce(function(acum, num){
    return acum + num;
});

console.log(suma); // 28
```


**forEach**
La finalidad de este método es iterar sobre un array.
Recibe un callback como parámetro y, a diferencia de los métodos anteriores, este no retorna nada.

```
array.forEach(function(elemento){
    // definimos el comportamiento que queremos
    // implementar sobre cada elemento
});
```

*Ejemplo:*
```
var paises = ['Argentina', 'Cuba', 'Perú'];

paises.forEach(function(pais){
   console.log(pais);
});
```