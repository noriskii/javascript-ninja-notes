# Aula 10

## Wrapper Objects
```js
// Valores primitivos não são objetos
// OBJETOS tem propriedades e métodos.

var name = 'lucas';
> name.length; //5
// Então por que ele tem propriedades?

// Por debaixo dos panos o javascript um construtor
```

### Construtores I:
```js
// Utiliza-se o new para criar um novo 'objeto'
var name = new String('lucas');
var age = new Number(3);
var ninja = new Boolean(true);  

// Sem o new, ele apenas converte valor
var age = Number('3');
``` 

## Operador Unário (typeof)
```js
typeof 10
> 'number'
typeof NaN
> 'number'
typeof 'JS Ninja'
> 'string'
typeof {}
> 'object'
typeof []
> 'object'
typeof null // Erro de implementação do JS
> 'object'
typeof function() {}
> 'function'
typeof 'undefined'
> 'object'
// Garantido apenas para valores primitivos
```