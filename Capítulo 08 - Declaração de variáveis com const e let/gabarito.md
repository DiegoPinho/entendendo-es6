# Gabarito

## Exercício 1 - Sei tudo sobre variáveis
a) 10 várias vezes

b) Alterando o `var` para `let`

## Exercício 2 - ISSO_EH_UMA_CONSTANTE
R: Agora é possível utilizar o `const` para declarar esses tipos de variáveis. Além de revelar logo de cara que o valor armazenada em uma variável deste tipo é constante, o próprio JavaScript te impede de atribuir um novo valor a ela, dando mais segurança a constante.

## Exercício 3 - Eu estou mandando atribuir!
R: Ele está tentando atribuir um novo valor a variável `nomeCompleto` logo depois de atribuir o valor da variável `primeiroNome`, mas como a variável foi declarada com a palavra `const`, não é possível fazer uma nova atribuição nesta variável. Para este caso, ele deveria ter usado o `let`.

## Exercício 4 - Pode ou não pode?
R: É necessário ter em mente que um `const` não se trata de uma variável constante, mas uma referência constante. Em termos práticos, isso significa que o valor não é imutável, é possível adicionar e remover propriedades desta variável. Por isso funcionou.

## Exercício 5 - Lá vem um temporal
R: No JavaScript, a declaração das nossas funções e variáveis possuem o comportamento de Hoisting. Este nome é dado ao comportamento de mover declarações para o topo de um escopo (global ou não). Em outras palavras, isso significa que é possível usar uma variável ou função antes mesmo de declará-las no código. No ES6, o “hoisting” do let e const são diferentes de variáveis e funções. Quando uma variável é declarada usando let ou const , ela possui o que é chamada de Temporal Dead Zone (TDZ), nome que descreve o comportamento de que, no seu escopo, ela é inacessível até que a execução alcance sua declaração

## Exercício 6 - Tudo fora de escopo
``` javascript
const status = [
  { codigo: 'OK', resposta: 'Sucesso' },
  { codigo: 'FAILED', resposta: 'Erro' },
  { codigo: 'PENDING', resposta: 'Pendente' }
];
let mensagem = '';
const codigoAtual = 'OK';

for (let i = 0; i < status.length; i++) {
  if (status[i].codigo === codigoAtual) {
    mensagem = status[i].resposta;
  }
}

console.log(mensagem);
```
