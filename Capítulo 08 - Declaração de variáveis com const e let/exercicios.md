# Exercícios

Nestes exercícios iremos exercitar como utilizar a declaração de variáveis utilizando o `const` e o `let`

## Exercício 1 - Sei tudo sobre variáveis
Considere o trecho de código abaixo e responda as questões:

``` javascript
var arrayFuncoes = [];
for(var i = 0; i < 10; i++){
  arrayFuncoes.push(function(){
    console.log(i);
  });
}

arrayFuncoes.forEach(function(funcao){
  funcao();
});
```
a) Quais os valores são exibidos no console na execução desse código?
b) Como podemos ajustar o comportamento desta função utilizando ES6?

## Exercício 2 - ISSO_EH_UMA_CONSTANTE
Uma prática comum dos desenvolvedores é deixar o nome das variáveis que representam constantes em caixa alta. Como por exemplo, uma variável que armazena uma chave de API de um webservice. Com o ES6, temos uma maneira melhor de representar isso. Que maneira é essa?

## Exercício 3 - Eu estou mandando atribuir!
Um programador júnior de uma empresa de software está tentando executar o seguinte código:

``` javascript
function nomeCompleto(primeiroNome, segundoNome){
  const nomeCompleto = primeiroNome;
  nomeCompleto += ' ' + segundoNome;

  return nomeCompleto;
}
```

Ele não consegue entender o que está fazendo de errado. No que ele está errando?

## Exercício 4 - Não estou entendendo mais nada
Uma jovem programadora pensou que havia entendido como funcionava a declaração de variáveis com `let` e `const` até ver o seguinte trecho de código:
``` javascript
const jogador = {};
jogador.nome = 'Rodrigo';
jogador.idade = 33;

console.log(jogador.nome  + '_' +  jogador.idade); // saída: Rodrigo_33
```

Ela achou que este código não funcionaria, pois havia entendido que não era possível colocar novos valores em variáveis declaradas com `const`. Por que este código funciona sem problemas?

## Exercício 5 - Lá vem um temporal
O que significa o _Temporal Dead Zone_? Qual sua relação com o _Hoisting_?

## Exercício 6 - Tudo fora de escopo
Refatore o código a seguir utilizando o `const` e `let`.
``` javascript
var status = [
  { codigo: 'OK', resposta: 'Sucesso' },
  { codigo: 'FAILED', resposta: 'Erro' },
  { codigo: 'PENDING', resposta: 'Pendente' }
];
var mensagem = '';
var codigoAtual = 'OK';

for (var i = 0; i < status.length; i++) {
  if (status[i].codigo === codigoAtual) {
    mensagem = status[i].resposta;
  }
}

console.log(mensagem);
```
