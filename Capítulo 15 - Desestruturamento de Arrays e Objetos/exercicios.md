# Exercícios

Nestes exercícios vamos revisar como o desestruturamento de objetos funciona.

## Exercício 1 - Desestruturando a definição
De forma resumida, defina o que é o desestruturamento.

## Exercício 2 - Pegando a propriedade na lata
Refatore o trecho de código a seguir para utilizar a técnica de desestruturamento.

``` javascript
const email = usuario.email;
const nome = usuario.nome;
const idade = usuario.idade
```

## Exercício 3 - Não gostei desse nome não
Considere o objeto literal `usuario` e extraia as propriedades `nome` e `email` em variáveis com o nome `nick` e `login`, respectivamente.

``` javascript
const usuario = {
  nome: 'Toreto',
  email: 'velozesefuriososparasempre@gmail.com'
}
```

## Exercício x -
Converta do modelo 1 para o modelo 2 utilizando desestruturamento de objetos e arrays.
``` javascript
// modelo1
const pontos = [
  [1,2],
  [3,4],
  [5,6]
];

// modelo 2
const pontos = [
  {x:1, y:2},
  {x:3, y:4},
  {x:5, y:6},
]
```
