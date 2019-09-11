# Aula 2

## Operadores Lógicos
```js
&& // and
|| // or 
! // not (inverte o valor)
```

## Operadores Unários
```js
+ // Unário, que tenta converter o próximo valor depois dele em um number, quando tem uma string, tenta converter tudo pra string
> +'3'
3
> +'lucks'
NaN // Not a Number
> 'lu' + 'cks'
'lucks'
> '1' + 1
'11'
> 1 + '1'
'11'

- // Unário, que tenta converter o próximo valor depois dele em um number, não converte para string
> -'3'
-3
> -'lucks'
NaN // Not a Number
> 'lu' - 'cks'
NaN
> '1' - 1
0
> 1 - '1'
0
```

## Estrutura Léxica
### Case Sensitive:
```js
var nome = 'lucks'
> nome
'lucks'
> NOME
NOME is not defined
```

### Comentários:
```js
//One Line
//Another one line

/* 
This
is
a
Block
*/
```

### Literals:
```js
int: 1
float: 1.2
string: 'x', "y"
bolean: true
null: null
object: {a: 1}
array: [1,2]
```

### Identificadores:
Devem iniciar com:
-  _ ou $;
-  a - z;
-  A - Z.
  
Podem conter:
-  0 - 9;
-  Caracteres Unicode (Ω, Ψ, π).

### Palavras Reservadas (Keywords):
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords

## Condicionais
```js
if(condicao) { // se condição, faça
    ...code
} else if(outraCondicao) { // senão, se outraCondição, faça
    ...code
} else {
    ...code // senão, faça
}

> var x = 0;
> var y = 0;
> if(x === y) { // true
    x = 1;
    y = 1;
} else {
    x = 100;
    y = 100;
}
// Result: x = 1, y = 1

> var x = 0;
> var y = 0;
> if(x > y) { // false
    y = x + 1;
} else if (y < x) { // false
    x = y + 1;
} else { // so, do it
    x = 100;
    y = 100;
}
// Result: x = 100, y = 100
```