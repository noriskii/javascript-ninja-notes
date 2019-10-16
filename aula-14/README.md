# Aula 14

## Arrays IV:
```js
var arr = [1, 2, 3, 4, 5, 6];

// reduce(function(acumulado, atual, index, array) {}, 0) retorna um valor, reduzindo todos os valores do array, o segundo parametro além da function é o que define o acumulado. Caso o segundo parametro n seja enviado, o valor de acumulado será o indice [0] e o atual será o indice [1]
arr.reduce( function( acumulado, atual, index, array ) {
    return acumulado + atual; // 21
}, 0); 

// reduceRight(function(acumulado, atual, index, array) {}, 0) funciona da mesma forma que o reduce, porém, começa do final do array para o começo. Caso o segundo parametro n seja enviado, o valor de acumulado será o indice [last] e o atual será o indice [last - 1]
arr.reduceRight( function( acumulado, atual, index, array ) {
    return acumulado + atual; // 21
}, 0); 

arr = [1, 2, 3, 4, 5, 3];
// indexOf(item, index) retorna o indice da primeira ocorrencia enviada como parametro. retorna -1 caso não encontre o item procurado. pode receber o index que deve começar a procurar
arr.indexOf(3); // 2

// lastIndexOf(item, index) funciona da mesma forma que o indexOf, porém, inicia do final do array. o index do parametro define qual é o primeiro index a se olhar, mesmo q de traz pra frente
arr.lastIndexOf(3); // 5

// Array.isArray(item) verifica se o item enviado pelo parametro é um array
Array.isArray(arr); // true
```