# Exercícios

Nestes exercícios vamos reforçar o que foi ensinado sobre o operador `Spread`.

## Exercício 1 - Hora do ditado
Refatore o código a seguir para utilizar o operador `Spread` no método `log` do console.

``` javascript
console.log('e','c','m','a','s','c','r','i','p','t');
```

## Exercício 2 - Não são só umas reticências?
Qual a diferença básica entre os operadores `Rest` e `Spread`?


## Exercício 3 - Contador de Vogais
Implemente o método `contaQuantidadeVogaisNaoAcentuadas` que recebe um número indeterminado de palavras e retorna para o usuário o número total de vogais não acentuadas encontradas. Para este exercício, Considere somente palavras em minúsculo.


## Exercício 4 - Esse jeito é tão ultrapassado...
Como podemos refatorar o código a seguir sem utilizar os benefícios do ECMAScript 6?

``` javascript
var argumentos = [1,2,3];
console.log(argumentos[0], argumentos[1], argumentos[2]);
// 1, 2, 3
```

## Exercício 5 - A união faz a força
Refatore o código a seguir para utilizar o operador `Spread` ao invés do método `concat`.

``` javascript
const equipeMarketing = ['Joana', 'Marcela', 'Bruna'];
const equipeComercial = ['Talita', 'Luisa', 'Vitória'];

const timeCompleto = equipeMarketing.concat(equipeComercial);

realizaBrainstorm(timeCompleto);
```
