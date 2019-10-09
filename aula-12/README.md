# Aula 12

## Objetos:
- Mutaveis
- Manipulados por referência

### Formasde se Construir Objetos:
```js
// Criação Literal
var obj = {

};

// Com Construtor (new)
var obj = new Object();

// Com Object.create() 
// Todo objeto dentro do javascript herda de prototype (que mesmo vazio, tem seus métodos)
var obj = Object.create({});


var curiosity = {a: 1, b: 2};
var inheritance = Object.create(curiosity);

inheritance;
> {}
inheritance.a;
> 1
// Ele herda os valores de curiosity, porém, pode criar seus próprios valores para sobrepor a herança
curiosity.a = 2;
inheritance.a;
> 2
inheritance.a = 'asd';
curiosity.a;
> 2
```

### Propriedades
```js
var curiosity = {a: 1, b: 2};
var inheritance = Object.create(curiosity);

for(prop in curiosity) {
    console.log(prop);
}
> a, b;

for(prop in inheritance) {
    console.log(prop);
}
> a, b; // Mesmo que o objeto princiapl seja vaxio, ele tem essas propriedades herdadas

// Verifica se o objeto tem a própria propriedade, caso ela tenha sido herdada
inheritance.hasOwnProperty(prop)
```

### Métodos
```js
var obj = {a : 'asd',b : 2};

Object.keys(obj)
> ['a','b'];

Object.keys(obj).length
> 2;

// Verifica se um objeto é protótipo de outro objeto
Object.isPrototypeOf('Another Object');

// http://json.org
var str = JSON.stringify(obj);
> '{ "a" : "asd","b" : 2 }'
JSON.parse(str);
> {a : 'asd',b : 2}
```

## Arrays II:
```js
var arr = [];

arr[0] = 1;
arr[2] = 'asd';
arr;
> [1, , 'asd'];

arr.push('value');
> [1, , 'asd', 'value'];

arr.pop(); // Apaga a ultima ocorrencia do arr
> [1, , 'asd'];

// Transforma itens em string
arr.join();
> '1, asd'
arr.join('|');
> '1|asd'

// Inverte o array
arr.reverse(); // Modifica diretamente o array
> ['asd', 1]

// Ordena em ordem alfabética
arr.sort(); // Modifica diretamente o array
// ['b','a','c'];
> ['a','b','c']
```
