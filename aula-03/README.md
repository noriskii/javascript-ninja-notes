## Aula 3

### Tipos

#### Primitivos
```js
number // 1, 3.2, -1 e qualquer outro número
string // 'texto'. "teste", "1" e qualquer outro caractere seguido de aspas duplas+
boolean // true or false
null // Algo com o valor vazio
undefined /// Algo sem valor definido
```

#### Objeto
Conjunto de propriedades
```js
var objeto = { propriedade: 'valor' }
var funcao = function() { return 'x'; }

var objeto = {
    propriedade: 'valor',
    propriedade2: 10,
    propriedade3: true
};

> objeto.propriedade;
'valor'
> funcao();
'x'
```

### Objetos
```js
var pessoa = {
    nome: 'Lucas Augusto',
    spbrenome: 'Silva',
    idade: 22,
    altura: 1.65,
    peso: 62,
    sexo: 'masculino'
};
var pessoa = { x: 'y' } // sobreescreve objeto já existente
pessoa.cor = 'caucasiano'; // adiciona propriedade

pessoa.andar = function() { // Define um método
    return 'Pessoa Andando';
};

pessoa.aniversario = function() {
    pessoa.idade++;
};

pessoa.idade;
>22
pessoa.aniversario();
pessoa.idade;
>23

pessoa.nomeCompleto = function () {
    return pessoa.nome + ' ' + pessoa.sobrenome;
};

pessoa.nomeCompleto()
> 'Lucas Augusto Silva'
```