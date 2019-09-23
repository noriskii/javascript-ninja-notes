# Aula 7

## Operador Módulo
Resto de Divisão (inteiro)
```js
3 / 3 = 1;
3 % 3 = 0;
5 / 2 = 2.5;
5 % 2 = 1;

var num = 0;
while(num <= 20) {
    (num) % 2 === 0 ? console.log(num) : '';
    num++;
}
// Vai printar todos os números pares
```

## Arrays

### length:
A propriedade **length** retorna a quantidade de valores que temos em um array.
```js
var arr = ['a', 2, true, { teste: 'testa' }, function () {}];
// fato curioso, tudo no JS é objeto, portanto, conseguimos fazer arr[3].teste;

arr.length;
> 5

// imprime todos os valores do arr de forma inversa;
invertedIndex = arr.length; // 5
while(invertedIndex > 0) {
    console.log(arr[ --invertedIndex ]);
}
```

### push():
O método **push** insere (empurra) um valor para dentro do array.
```js
var arr = [1, 2, 3, 'lucas'];

arr.push('augusto');
> [1, 2, 3, 'lucas', 'augusto']

arr.push([1, 2, 3]);
> [1, 2, 3, 'lucas', 'augusto', [1, 2, 3]]
// fato curioso, podemos fazer arr[5][1..3] para mostrarmos o valor do array dentro do array

arr.push(function soma(x,y) { return x + y });
>´[1, 2, 3, 'lucas', 'augusto', [1, 2, 3], [Function soma]]
// fato curioso, podemos fazer arr[6](2,3) e teremos o retorno da soma
```

## Estruturas de Repetição II (LOOP)

### For:
```js
// for (init, condition, final-expression)
// para init, enquanto não satisfazer a condition, faça a final-expression
for (var num = 0; num <= 20; num++) {
    console.log(20);
} // Imprime todos os números de 0 a 20;
```