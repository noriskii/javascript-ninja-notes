# Aula 6

## Operador Vírgula
```js
var a,
    b = 2,
    c;

function virgula() {
    return (b += 1, b); // returna b;
    // o mesmo que ++b    
} 
```

## Switch
```js
function mySwitch(x) {
    switch(x) {
        case 1:
            console.log('x é 1');
        break;
        case 2:
            console.log('x é 2');
        break;
        default:
            console.log('x não é 1 e nem 2');
    }
}
```

## Estruturas de Repetição I (LOOP)

### While:
```js
var counter = 0;
while(counter < 10) { // repete enquanto true
    console.log(counter);
    counter**;
}

var counter = 10;
while(counter--) { // repete enquanto true
    console.log(counter);
}
```