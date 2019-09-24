# Aula 8

## Funções III
```js
// Sempre prefira funções nomeadas
var func = function func() {
    return 'Hi';
}

// Funções tem proprerties e métodos inbound
func();
> 'Hi'

func.name;
> 'func'

```

## Functional Programming
Para uma linguagem ser funcional ela precisa suportar objetos de primeira classe para funções.

Ou seja, funções são tratadas como objetos.
```js
{} <3 function(){}
```

### Literais:
```js
// objeto literal (ou seja, como ele é ou vai ficar)
var obj = {
    a : 1
}
// função literal
function func(x, y) {
    return x + y;
}
```

### Atribuir a Variaveis:
```js
var obj = {};

var func = function func() {};
var func = function () {};
```

### Retorno:
```js
// Funções podem retornar objetos
function person() {
    var info = {
        name : 'Lucas Augusto',
        lastName : 'Silva'
    };
    return info;
}

// Você pode acessar propriedades do objeto a partir da função
person().name;
> 'Lucas Augusto'

// E podem retornar outras funções
function adder(x) {
    function addOther(y) {
        return x + y;
    }
    return addOther;
}

var add = adder(2); // Transforma o add em uma função com o X = 2
add(3); // 5  

adder(2)(3); // 5
```
### Parametros:
```js
// Do mesmo jeito q manipulamos objetos dentro de funções
var car = {
    color: 'yellow'
};

function getCarColor(myCar) {
    return myCar.color;
}

// Manipulamos funções dentro de funções
function showOtherFunction(func) {
    return func();
}

function returnedFunction() {
    return 'Returned Function';
}

showOtherFunction(returnedFunction);
> 'Returned Function';

showOtherFunction(function () {
    return 'Functional JS Ninja!';
});
> 'Functional JS Ninja!'
```