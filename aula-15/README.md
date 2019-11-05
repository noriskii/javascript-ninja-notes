# Aula 15

## JS no Browser:
```html
<script></script>
<script src='folder/file.js'></script>

<!-- Utilizar IIFEs nos arquivos JS -->
```

### **this:**
index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JS Ninja Aula 15</title>
</head>
<body>
    <script src="main.js"></script>
</body>
</html>
```
main.js
```js
(function() {
    var myObject = {
        myProperty = 1,
        init: function init() {
            return this; // Faz referemcia ao objeto na qual ele esta inserido, ou seja o myObject
        }
    };
    console.log(myObject.init()); // Retorna o myObject

    function global() {
        return this;
    }
    console.log(global()); // Retorna o objeto window, que é o global no browser 

    function MyConstructor() {
        this.prop1 = 'prop1';
        this.prop2 = 'prop2';
    }
    var constructor = new MyConstructor(); // Croa escopo
    console.log(constructor); // Cria um objeto com o construtor de prop1 e prop2

    // Quando atribuimos uma variavel sem o var ou sem escopo, estamos pendurando ela no objeto global ou seja, window ou global
})();
```

### **arguments:**
index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JS Ninja Aula 15</title>
</head>
<body>
    <script src="main.js"></script>
</body>
</html>
```
main.js
```js
(function() {
    function myFunction() {
        return arguments; // É um array like que apresenta os argumentos passados na funcao
    }

    console.log(myFunction(1, 3, 5));
})();
```