# Exercícios

## Exercício 1 - Gastando até o que não tem
Refatore o código a seguir para utilizar o operador Rest:

``` javascript
function calculaPrecoTotal(a, b, c, d, e) {
  let precos = [a,b,c,d,e];
  return precos.reduce(function(total, preco) {
    return total + preco;
  }, 0)
}

calculaPrecoTotal(1,2,3,4,5); // 15
```

## Exercício 2 - Eu sou maior do que você, lero lero!
Utilize o operador Rest para criar uma função que recebe um parâmetro referência, que é obrigatório, e mais n parâmetros numéricos. O objetivo é que esta função calcule se todos os valores numéricos passados são maiores que a referência e retorne verdadeiro ou falso.

Exemplo:
todosSaoMaioresQue(2,3,4,5,6,7); // resultado esperado: true

Outros exemplos de entradas:
todosSaoMaioresQue(5,4,3,2,1); // resultado esperado: false
todosSaoMaioresQue(1,2); // resultado esperado: true

## Exercício 3 - Bingo!
Refatore o código abaixo para utilizar o operador Rest ao invés do `arguments`

``` javascript
function anunciaBolasSorteadas() {
  var nBolas = arguments.length;
  for(var i = 0; i < nBolas; i++) {
    console.log('A bola escolhida foi: ' + arguments[i]);
  }
}

anunciaBolasSorteadas(1,2,3);
// saída
// A bola escolhida foi: 1
// A bola escolhida foi: 2
// A bola escolhida foi: 3
```

## Exercício 4 - Mas o professor que ensinou assim!
Um aluno de computação tentou utilizar o operador Rest para tratar números e letras, de quantidade indefinida, dentro do seu código, mas não conseguiu. Este foi o código que ele escreveu:

``` javascript
function numerosELetras(...numeros, ...letras){
  // corpo da função
}

Explique o porque este código não funciona.
```

## Exercício 5 - Este sim saber argumentar
O que é o objeto `arguments`?
