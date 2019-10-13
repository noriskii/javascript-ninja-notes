# Aula 13

## Arrays III:
```js
var arr = [1, 2, 3];

// toString() transforma os itens do array em uma unica string separada por virgula
arr.toString();
> '1,2,3'

// concat() concatena arrays ou valores aos arrays, sem modificar o array principal (Quando o array for multidimensional, ele apenas adiciona ao array)
arr.concat(4);
> [1, 2, 3, 4]

// unshift() adiciona um item no começo do array;
arr.unshift(0);
> [0, 1, 2, 3]

// shift() remove o item no começo do array;
arr.shift();
> [1, 2, 3]

// slice(index,index_max) pega um valor a partir de um index até um index máximo, não altera o array principal. Se o index máximo não estiver definido, ele retorna até o final do array.
[0,1,2,3,4,5].slice(2);
> [2, 3, 4, 5]
[0,1,2,3,4,5].slice(3,4);
> [3]

// splice(index, quantity, add_sub...) modifica o array principal, removendo ou adicionando algo a algum indice especifico, pode remover a partir de um indice, ou adionar a partir do mesmo
arr = [1,2,3,4,5,6,7];
arr.splice(1,3); // retorna [2,3,4] que são os valores removidos pelo splice
console.log(arr); // retorna [1,5,6,7]
arr.splice(1,0, 'a'); // retorna [] pois não removeu nada
console.log(arr); // retorna [1,'a',5,6,7] 
arr.splice(1,1,2); // retorna [a] substituindo ele por 2
console.log(arr); // returna [1,2,5,6,7]
arr.splice(1,1,2,3,4); // retorna [2] substituindo ele por 2,3,4
console.log(arr); // returna [1,2,3,4,5,6,7]

// forEach(function(item, index, array) {}) itera sobre o array, e te disponibiliza (opcional) os seguintes valores, item, index e array. (mais rapido que o for normal)
arr = [1,2,3,4,5,6,7];
arr.forEach(function(item, index, array) {
    console.log(item, index, array)
});

// every(function(item) {}) retorna true ou false, te disponibiliza uma forma de FOR, para que sejam testadas condições para os itens do array, para o every, todos os itens precisam ser true para que ele retorne true
arr = [1,2,3,4,5,6,7];
arr.every(function(item) {
    return item < 5; // false
});

// some(function(item) {}) segue o mesmo método que o every, porém, ele verifica se pelo menos 1 item no array seja true para que ele retorne true.
arr = [1,2,3,4,5,6,7];
arr.every(function(item) {
    return item % 2 === 0; // true
});

// map(function() {}) percorre todo o array, fazendo alguma interação sobre os items do array, e retorna um novo array com as mudanças feitas (Não altera o array principal)
arr = [1,2,3,4,5,6,7];
arr.map(function(item, index, array){
    return item * 2; // [2,4,6,8,10,12,14]
});

// filter(function() {}) percorre o array, e filtra os valores, retornando um array, podemos por exemplo, criar um novo array, com os valores maiores que X, ou seja, retorne apenas os valores true
arr = [1,2,3,4,5,6,7];
arr.filter(function(item, index, array){
    return item > 2; // [3,4,5,6,7]
});
```