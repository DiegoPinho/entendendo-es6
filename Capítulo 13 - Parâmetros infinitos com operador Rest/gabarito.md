# Gabarito

## Exercício 1 - Gastando até o que não tem
``` javascript
function calculaPrecoTotal(...precos) {
  return precos.reduce(function(total, preco) {
    return total + preco;
  }, 0)
}

calculaPrecoTotal(1,2,3,4,5); // 15
```

## Exercício 2 - Eu sou maior do que você, lero lero!
``` javascript
function todosSaoMaioresQue(ref, ...valores) {
  for(let valor of valores) {
    if(valor < ref) {
      return false;
    }
  }

  return true;
}
```

## Exercício 3 - Bingo!
``` javascript
function anunciaBolasSorteadas(... bolas) {
  for(let bola of bolas) {
    console.log(`A bola escolhida foi: ${bola} `);
  }
}
```

## Exercício 4 - Mas o professor que ensinou assim!
**R:** O operador sempre interpreta as últimas variáveis passadas na função para compactá-las em um único `Array`. Apesar de a separação parecer fazer sentido para o aluno, não funcionará como esperado. O correto seria fazer algo do gênero:

``` javascript
function numerosELetras(...numerosELetras) {
  // corpo
}
```

## Exercício 5 - Este sim saber argumentar
**R:** Este objeto está disponível dentro de todas as funções construídas no JavaScript. Ele contém um registro para cada argumento passado para a função no contexto de sua execução, sendo que o primeiro índice de registro começa no índice 0.
