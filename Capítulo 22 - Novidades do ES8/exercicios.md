# Exercícios

Nestes exercícios vamos rever como funcionam as novidades trazidas pelo ES8 (ES2017).

## Exercício 1 - Tim tim por tim tim
Escreva uma função chamada `mapeiaObjeto` que recebe um objeto literal como parâmetro. A função deve retornar um mapa descrevendo todas as propriedades desta objeto, onde a chave é o nome da propriedade e o valor, o respectivo valor da propriedade.

Exemplo:

* mapeiaObjeto({nome: 'joão bobão'}) → mapa.get('nome'); // 'joão bobão'

## Exercício 2 - Quero os dados completos
Escreva uma função `detalhaObjeto` que recebe um objeto literal como parâmetro e então exibe, para cada propriedade, uma linha no console no formato: `propriedade: valor`. Não se esqueça de usar as funcionalidade do ES6, como o desestruturamento, loop for...of e template literais.

Exemplo:

* detalhaObjeto({rua: 'oscar freire'}) → rua: oscar freire

## Exerício 3 - Ih, não deu ._.
Qual o caso em que o `Object.entries` não funciona?

## Exercício 4 - Prove o seu valor
Crie uma função chamada `somenteValores` que recebe um objeto literal e mostra no console, para cada propriedade, uma linha no console mostrando o valor da propriedade correspondente. 

## Exercício 5 - Todos para a direita!
Crie uma função chamada `tudoParaADireita` que recebe dois parâmetros: o primeiro é um array de strings; o segundo é o tamanho máximo em que as palavras devem ser empurradas para a direita. Esse valor precisa ser maior ou igual ao ao tamanho da palavra mais cumprida do primeiro parâmetro. A função deve alinhar todos os textos para a direita.

Exemplo:

``` javascript
tudoParaADireita([
  'carro', 'avião', 'foguete', 'helicóptero'  
], 11);

/*
      carro
      avião
    foguete
helicóptero
```

## Exercício 6 - Eu disse direita? Quis dizer esquerda!
Faça um método semelhante ao do exercício anterior, mas chame-o de `tudoParaAEsquerda` e faça com o texto seja alinhado para a esquerda e preencha o espaço restante com hífen "-".

Exemplo:

``` javascript
function tudoParaAEsquerda(palavras, tamanho) {
  palavras.forEach(palavra => {
    console.log(palavra.padEnd(tamanho,'-'));
  })
}

tudoParaAEsquerda([
  'carro', 'avião', 'foguete', 'helicóptero'  
], 11);

/*
carro------
avião------
foguete----
helicóptero
*/
```

## Exercício 7 - Quais enumeráveis eu tenho na minha mão?
Crie uma função de nome `quantidadePropriedadesEnumeraveis` que recebe um objeto literal e retorna o número de propriedade enumeráveis deste objeto.

Exemplo:

* quantidadePropriedadesEnumeraveis({nome: 'jão'}); // 1