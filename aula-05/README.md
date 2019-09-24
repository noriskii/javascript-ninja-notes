# Aula 5

## Funções II

### Retorno:
```js
function myFunction() {
    return 1;
}
myFunction();
>1

function myFunction() {
    return 'string';
}
myFunction();
>'string'

function myFunction() {
    return true;
}
myFunction();
>true

function myFunction() {
    return [1, 2, 3];
}
myFunction();
>[ 1, 2, 3 ]
myFunction()[0];
>1

function myFunction() {
    return {
        prop1: 1,
        prop2: 'lucas',
        prop3: function() {
            return 'prop3';
        }
    };
}
myFunction().prop2;
>'lucas'
myFunction().prop3();
>'prop3'  
```

### Parâmetros:
```js
function myFunction() {
    return arg
}

myFunction([1, 2, 3]);
>[1, 2, 3]
myFunction([1, 2, 3])[2];
>3
myFunction({nome: 'lucas', ninja: true});
>{nome: 'lucas', ninja: true}
myFunction({nome: 'lucas', ninja: true}).ninja;
>true
```