# Aula 1

## Variáveis
```js
var x;
> undefined

var x = 'Hello World'; // string
var x = true; // boolean
var x = false; // boolean
var x = 1; // number
var x = 1.2; // float

var x = []; // array
var x = {}; // object

var x = null; // uma variável com valor vazio
var x = undefined; // não existe valor
```

## Operadores

### Aritméticos
```js
> 1 + 1
2
> 3 - 1 
2
> 4 * 5
20
> 10 / 2
5

//Abreviados
++ // Incremento, pode ser pré e pós
-- // Decremento, pode ser pré e pós

soma = 1 + 1;
> soma = 2
soma = soma + 1;
> soma = 3 
soma++; // Pós Incremento
> soma = 3
soma
> soma = 4
++soma; // Pré Incremento
> soma = 5;

//mais alguns...
+= // var = var + something
-= // var = var - something
*= // var = var * something
\/= \// var = var / something

var x = 10;
x += 20;
> x = 30
```

### Igualdade/Relacionais
```js
== // igual a
!= // diferente de
=== // igual a, e do mesmo tipo
!== // diferente de, mas do mesmo tipo

1 == '1'
> true
1 === '1'
> false

> // maior
\< // menor
>= // maior ou igual
\<= // menor ou igual

1 > 1
> false
1 >= 1
> true
```

## Funções I
É um de código nomeado que é chamado utilizando o operador ().  
*Funções criam escopo.
```js
function funcao() {}
funcao()
> undefined
funcao
> [Function: funcao]

function soma(x, y) {
    return x + y;
}
soma(2,3);
> 5
```