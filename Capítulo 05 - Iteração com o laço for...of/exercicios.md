# Exercícios

Nestes exercícios iremos exercitar como fazer laços de repetição utilizando a estrutura `for...of`

## Exercício 1 - Contando o faturamento
Escreva uma função chamada `somaFaturamento` que recebe uma lista de números inteiros e devolve a soma destes valores.

* Exemplo: somaFaturamento([1,2,3,4]) → 10

## Exercício 2 - Por quê não funciona?
Um jovem programador tentou utilizar o laço de repetição `for...of` no objeto `Casa` na esperança de que o laço passasse por todas as propriedades deste objeto. No entanto, ele só recebeu o erro: `TypeError: Casa[Symbol.iterator] is not a function`. Por que não está funcionando?

Este foi o código que ele tentou executar:
``` javascript
var Casa = {
  metrosQuadrados: 4000,
  altura: 3000,
  nQuartos: 4,
  nBanheiros: 2

  //...
}


for(var atributo of Casa) {
  console.log(atributo);
}
```

## Exercício 3 - Agora vai funcionar
Resolva o problema do Exercício 2 utilizando a estrutura `for...in`.

## Exercício 4 - Pare aqui senhor motorista
Implemente o método `percorreRuas` que recebe uma lista de strings que representam nomes de ruas e um segundo parâmetro que também é um string, mas representa o nome da rua em que deve parar. Para cada rua percorrida, deve ser apresentada no console, como neste exemplo:

* Exemplo: percorreRuas(['Rua 1, Rua 2', 'Rua 3'], 'Rua 2') → 'Rua 1' , 'Rua 2'

Utilize o laço `for...of` e o `break` para não percorrer mais ruas que o necessário.

## Exercício 5 - Não vá por ali!
Implemente o método 'percorreRuas' que recebe dois parâmetros:
- ruas: Lista de strings que presentam as ruas que serão percorridas (ex: 'Rua 1')
- ruaPerigosa: String que represeta o nome da rua que deve ser evitada

Faça com que o método percorra cada uma das ruas exibindo no console, menos para a `ruaPerigosa`.
Utilize o `for...of` e o `continue` para fazer esta lógica.
