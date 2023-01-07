##  PROPIEDADES Y MÉTODOS: ARRAYS / STRINGS

*Método:* es una función que pertenece a un objeto.


**METODOS DE ARRAY** 

**.push()**
Recibe uno o más elementos como parámetros.
Retorna la nueva longitud del array.

*Ejemplo:*
let colores = ['Rojo','Naranja','Azul'];
colores.push('Violeta'); // retorna 4
console.log(colores); // ['Rojo','Naranja','Azul','Violeta']


**.pop()**
Elimina el último elemento de un array.
No recibe parámetros.
Devuelve el elemento eliminado.

*Ejemplo:*
let series = ['Mad Men','Breaking Bad','The Sopranos'];
// creamos una variable para guardar lo que devuelve .pop()
let ultimaSerie = series.pop();
console.log(series); // ['Mad men', 'Breaking Bad']
console.log(ultimaSerie); // ['The Sopranos']


**.shift()**
Elimina el primer elemento de un array.
No recibe parámetros.
Devuelve el elemento eliminado.

*Ejemplo:*
let nombres = ['Frida','Diego','Sofía'];
// creamos una variable para guardar lo que devuelve .shift()
let primerNombre = nombres.shift();
console.log(nombres); // ['Diego', 'Sofía']
console.log(primerNombre); // ['Frida']


**.unshift()**
Agrega uno o varios elementos al principio de un array.
Recibe uno o más elementos como parámetros.
Retorna la nueva longitud del array.

*Ejemplo:*
let marcas = ['Audi'];
marcas.unshift('Ford');
console.log(marcas); // ['Ford', 'Audi']
marcas.unshift('Ferrari','BMW');
console.log(marcas); // ['Ferrari','BMW','Ford', 'Audi'];


**.join()**
Une los elementos de un array utilizando el separador que le especifiquemos. Si no lo especificamos, utiliza comas.
Recibe un separador (string), es opcional.
Retorna un string con los elementos unidos.

*Ejemplo:*
let dias = ['Lunes','Martes','Jueves'];
let separadosPorComa = dias.join();
console.log(separadosPorComa); // 'Lunes,Martes,Jueves'
let separadosPorGuion = dias.join(' - ');
console.log(separadosPorGuion); // 'Lunes - Martes - Jueves'


**.indexOf()**
Busca en el array el elemento que recibe como parámetro.
Recibe un elemento a buscar en el array.
Retorna el primer índice donde encontró lo que buscábamos. Si no lo encuentra, retorna un -1.

*Ejemplo:*
let frutas = ['Manzana','Pera','Frutilla'];
frutas.indexOf('Frutilla');
// Encontró lo que buscaba. Devuelve 2, el índice del elemento
frutas.indexOf('Banana');
// No encontró lo que buscaba. Devuelve -1


**.lastIndexOf()**
Similar a .indexOf(), con la salvedad de que empieza buscando el elemento por el final del array (de atrás hacia adelante).  
En caso de haber elementos repetidos, devuelve la posición del primero que encuentre (o sea el último si miramos desde el principio).

*Ejemplo:*
let clubes = ['Racing','Boca','Lanús','Boca'];
clubes.lastIndexOf('Boca');
// Encontró lo que buscaba. Devuelve 3
clubes.lastIndexOf('River');
// No encontró lo que buscaba. Devuelve -1


**.includes()**
También similar a .indexOf(), con la salvedad que retorna un booleano.
Recibe un elemento a buscar en el array.
Retorna true si encontró lo que buscábamos, false en caso contrario.

*Ejemplo:*
let frutas = ['Manzana','Pera','Frutilla'];
frutas.includes('Frutilla');
// Encontró lo que buscaba. Devuelve true
frutas.includes('Banana');
// No encontró lo que buscaba. Devuelve false



**METODOS DE STRINGS:** Los strings son como una colección de caracteres. Por esta razón disponemos de propiedades y métodos muy útiles a la hora de trabajar con la información que hay adentro. 

- Un string no es más que un array de caracteres. Al igual que en los arrays, la primera posición siempre será _0_.
- Para acceder a un carácter puntual de un string, nombramos al string y dentro de los corchetes escribimos el índice al cual queremos acceder.
- Las propiedad solo debemos llamarlas, sin necesidad de los paréntesis.

**.length**
Esta propiedad retorna la cantidad total de caracteres del string, incluidos los espacios.

*Ejemplo:*
let miSerie = 'Mad Men';
miSerie.length; // devuelve 7
let arrayNombres = ['Bart', 'Lisa', 'Moe'];
arrayNombres.length; // devuelve 3
arrayNombres[0].length; // Corresponde a 'Bart', devuelve 4


**.indexOf()**
Busca, en el string, el string que recibe como parámetro.
Recibe un elemento a buscar en el array.
Retorna el primer índice donde encontró lo que buscábamos. Si no lo encuentra, retorna un -1.

*Ejemplo:*
let saludo = '¡Hola! Estamos programando';
saludo.indexOf('Estamos'); // devuelve 7
saludo.indexOf('vamos'); // devuelve -1, no lo encontró
saludo.indexOf('o'); // encuentra la letra 'o' que está en la posición 2, devuelve 2 y corta la ejecución


**.slice()**
Corta el string y devuelve una parte del string donde se aplica.
Recibe 2 números como parámetros (pueden ser negativos):
El índice desde donde inicia el corte.
El índice hasta donde hacer el corte (es opcional).
Retorna la parte correspondiente al corte.

*Ejemplo:*
let frase = 'Breaking Bad Rules!';
frase.slice(9,12); // devuelve 'Bad'
frase.slice(13); // devuelve 'Rules!'
frase.slice(-10); // ¿Qué devuelve? ¡A investigar!


**.trim()**
Elimina los espacios que estén al principio y al final de un string.
No recibe parámetros.
No quita los espacios del medio.

*Ejemplo:*
let nombreCompleto = '   Homero Simpson   ';
nombreCompleto.trim(); // devuelve 'Homero Simpson'
let nombreCompleto = '   Homero	  J.    Simpson   ';
nombreCompleto.trim(); // devuelve 'Homero    J.    Simpson'


**.replace()**
Reemplaza una parte del string por otra.
Recibe dos strings como parámetros:
El string que queremos buscar.
El string que usaremos de reemplazo.
Retorna un nuevo string con el reemplazo.

*Ejemplo:*
let frase = 'Aguante Python!';
frase.replace('Python', 'JS'); // devuelve 'Aguante JS!'
frase.replace('Py', 'JS'); // devuelve 'Aguante JSthon!'


**.split()**
Divide un string en partes. 
Recibe un string que usará como separador de las partes.
Devuelve un array con las partes del string.

*Ejemplo:*
let cancion = 'And bingo was his name, oh!';
cancion.split(' ');
// devuelve ['And', 'bingo', 'was', 'his', 'name,' , 'oh!']
cancion.split(', ');
// devuelve ['And bingo was his name', 'oh!']