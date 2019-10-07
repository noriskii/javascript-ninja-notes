# Aula 11

## Estruturas de Repetição III (LOOP)

### Do/While:
Semelhante ao While, porém, ele sempre entra na primeira execução de um laço
```js
var counter = 10;

do {
    conxole.log(counter);
} while (counter < 10);
```

### For in:
```js
var car = {
    brand: 'audi',
    model: 'a330',
    year: 2017
};

for(var prop in car) {
    console.log(prop + ' = ' + car[prop]);
}

//in pode ser usado para testar também
console.log('O carro tem marca?','brand' in car);
> 'O carro tem marca?' true
```

## Saltos
Palavras chave capazes de pular partes de código
```js
// return - Retorna um resultado e ignora o resto do código;
// break - 'quebra' o escopo atual (for, if), pulando para o próximo código;
// continue - Ele funciona de forma parecida com o break, porém, não quebra o código, apenas continua para o próximo laço válido.
```