# Aula 16

**HTML Para uso geral:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JS Ninja Aula 16</title>
</head>
<body>
    <script src="main.js"></script>
</body>
</html>
```
## 'use strict':
Diretiva que define um escopo restrito.
```js
(function (){
    'use strict';
    myName = 'Lucas Augusto'; // Acusa um ReferenceError não deixando vc causar problemas das antigas versões do JS.
    console.log(myName);
})();
```
### with:
```js
(function(){
    'use strict'; // Não permite o uso do with, pois ele pode se confundir com variaveis de fora do with
    var obj = {
        prop1: {
            prop2: {
                prop3: {
                    prop31: 'prop31',
                    prop32: 'prop32',
                    prop33: 'prop33'
                }
            }
        }
    }
    with(obj.prop1.prop2.prop3) {
        // O with reduz o escopo para usarmos alguma propriedade dentro de um determinado objeto
        console.log(prop31,prop32,prop33);
    }
})()
```
### this:
```js
(function(){
    'use strict'; // Define que o this é undefined 
    function Person( name, lastName, age) {
       this.name = name;
       this.lastName = lastName;
       this.age = age; 
    }
    console.log(Person('Lucas','Augusto',22)); // Retorna erro, pois não conseguimos definir as variaveis ao this global
})();
```
### delete:
```js
(function(){
    'use strict'; // lança um syntax error se o delete não puder ser usado
    var obj = {
        prop1: 'prop1',
        prop2: 'prop2',
        prop3: 'prop3'
    };
    console.log(delete obj.prop1, obj); // Deleta uma propriedade de um objeto;
    console.log(delete obj); // Retorna syntaxError pois ele não consegue deletar nada além de propriedades  
})();
```
### duplicates:
```js
(function(){
    'use strict'; // Não permite o uso de duplicates
    var obj = {
        prop1: 'prop1',
        prop1: 'prop2', // Error
        prop3: 'prop3'
    };

    function funcao(a, a, b) { // Error
        return a + b;
    }  
})();
```
## Objeto String:
```js
'string'.length; // Retorna quantos caracteres tem na string
> 6

'string'.charAt(index) && 'string'[index] // Retorna qual caractere tem no index definido
'string'[1]
> t

'string'.concat(' int', ' float') // Concatena na string, porém, não mexe no objeto principal, apenas cria outro valor
> 'string int float'

'string'.indexOf(string, start) // Retorna o index em que achou algum ou alguns caracteres buscados, sendo o start opcional, retorna -1 se não achr nada
'string'.indexOf('s');
> 0

'string'.lastIndexOf(string, start) // Funciona da msm forma que o indexOf, porém, começa do final
'strings'.lastIndexOf('s');
> 6

'string'.replace(string, newString) // Substitiu algo na string por outra string, faz o replace apenas no primeiro caractere encontrado, não modifica a string principal, cria outra.
'string'.replace('i','o');
> 'strong'

'string'.slice(start, end) // Corta a string, de um start até um end, sendo o end opcional, não altera a string principal
'string'.slice(2);
> 'ring'
'string'.slice(2,4);
> 'ri'

'string'.split(separator) // Cria um array, separando a string, funciona para fazer varias substituições, combando com o join do array
'string'.split();
> ['string']
'string'.split('i');
> ['str', 'ng']
'hahaha'.split('a').join('e');
> 'hehehe'

'string'.substring(start, end) // Funciona como um slice, a sua diferença é q se o start for maior que o end, ele inverte, pega do final ao começo
'string'.substring(0,3);
> 'str'
'string'.substring(3,0);
> 'str'

'StrIng'.toLowerCase(); // Transforma os caracteres em lowerCase, não modifica a string principal
> 'string'

'string'.toUpperCase(); // Transforma os caracteres em upperCase, não modifica a string principal
> 'STRING'
```
