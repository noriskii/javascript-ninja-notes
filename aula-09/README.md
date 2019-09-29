# Aula 9

## Funções IV

### Escopo:
```js
// funções criam escopo entre si
function myFunction() {
    var n1 = 1;
    var n2 = 2;
    // Papel de Clojure (acessa variavel externa)
    function sum() {
        // aqui dentro temos outro escopo
        return n1 + n2;
    }
    return sum();
}

function myFunction() {
    // Cria a funcao, mas não executa
    function sum() {
        return n1 + n2;
    }
    var n1 = 1;
    var n2 = 2;
    return sum(); //funciona
}
```

### Hoisting:
Ou elevação, ele sobe funções literais para cima do código, onde toda função literal estará disponível para todo o escopo do código
```js
function myFunction() {
    var n1 = 1;
    var n2 = 2;
    return sum(); //funciona
    function sum() {
        return n1 + n2;
    }
    // Na prática, ele sobe o sum para a primeira linha da função
}

function myFunction() {
    var n1 = 1;
    var n2 = 2;
    return sum(); //funciona
    var sum = function sum() {
        return n1 + n2;
    }
    // Quando ele sobe o sum, define ele como undefined e ignora a função
}

function myFunction() {
    console.log(number1); // undefined
    console.log(number2); // not declared
    var number1 = 10; // faz o hoisting
    console.log(number1); // 10
}
```

### IIFE (Immediately-invoked function expression):
Funções Autoexecutaveis, executadas somente quando forem uma expressão. Tem uma vantagem de criar escopo!
```js
(function () {
    console.log('Automagic');
})();
```