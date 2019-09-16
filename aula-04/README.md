# Aula 4

## Truthy and Falsy
São representações de valores que retornam um número booleano.

### Falsy:
- false
- undefined
- null
- NaN
- 0
- -0
- '' ou ""

### Truthy:
- Todos os valores que não são Falsy.

```js
!! // Testa a representação booleana de algum valor

!!true
> true
!!1
> true
!!false
> false
!!undefined
> false
```

## Condicional Ternário
```js
condicao ? true : false;

var valor = 1 == true ? 'yes' : 'no';
```

## Escopo de Variáveis
- GLOBAL: Pode ser acessado por qualquer parte do código
- LOCAL: Pode ser acessado apenas pelo bloco que definiu a variávels, exemplo, function cria escopo
```js
var x = 10;
function globalVar() {
    return x + 1;
}
globalVar();
> 11;

function localVar() {
    var y = 5;
    return y + 1;
}
localVar();
> 6
y;
> y is not defined

/*
Você pode criar uma variável sem a palavra chave var, let, const. Porém, ele cria ela global independente de onde seja criado.
*/

/*
Argumentos de função sempre são locais.
*/
```
