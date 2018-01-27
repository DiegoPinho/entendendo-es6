# Gabarito

## Exercício 1 - Par ou ímpar?
``` javascript
var numeros = [0,1,2,3,4,5];
numeros.forEach(function(numero){
    if(numero % 2 === 0) {
        console.log(numero + ' é par');
    } else {
        console.log(numero + ' é ímpar');
    }
});
```

## Exercício 2 - Quero o dobro
``` javascript
function dobrar(numeros) {
    return numeros.map(function(numero){
        return numero * 2;
    });
}
```

## Exercício 3 - NÃO ESTOU BRAVO
``` javascript
function caps(palavras) {
    return palavras.map(function(palavra){
        return palavra.toUpperCase();
    });
}
```

## Exercício 4 - Equilibrio de parênteses
``` javascript
function validaParenteses(parenteses) {
  var arrayParenteses = parenteses.split(""); // reduce só funciona com arrays
  /**
   * Vamos utilizar números para essa solução. Para cada parêntese esquerdo, vamos
   * somar 1 e para cada parêntese direito vamos subtrair um
   **/
  var balanceado =  !arrayParenteses.reduce(function(soma, parentese) {
    if(soma < 0) { return soma } // para o caso de começar com ")"
    if(parentese ===  "(") { return ++soma }
    if(parentese ===  ")") { return --soma }
  }, 0);

  return balanceado;
}
```

## Exercício 5 - Sem duplicações
``` javascript
function removeDuplicatas(numeros) {
  return numeros.reduce(function(anterior, valor) {
     var achouDuplicata = anterior.find(function(valor2){
         return valor === valor2;
     });

     if(!achouDuplicata){
        anterior.push(valor);
     }

     return anterior;
  }, []);
}
```

## Exercício 6 - Reprovado!
``` javascript
function aprovados(alunos, media) {
  return alunos.filter(function(aluno){
    return aluno.media >= media;
  });
}
```

## Exercício 7 - Dados precisos
``` javascript
function buscar(propriedade, valor, lista) {
  return lista.find(function(item) {
    return item[propriedade] === valor;
  });
}
```

## Exercício 8 - Calculadora Humana
``` javascript
function calculaAreaTotal(dimensoes) {
  return dimensoes.reduce(function(anterior, valor) {
    return anterior + (valor.altura * valor.comprimento);    
  }, 0);
}
```

## Exercício 9 - Raízes Quadradas
``` javascript
function calculaRaizesQuadradas(numeros) {
  return numeros.map(function(numero) {
    return Math.sqrt(numero);
  });
}
```

## Exercício 10 - E tem alguma diferença?
Os dois métodos iteram toda a lista e tem a assinatura de método semelhante, no entanto, o `map` é capaz de nos devolver um array com valores que resultam da iteração de cada um dos valores do array original. Para cada item do array original, há um item no array resultante. O `forEach` não é capaz de fazer isso naturalmente. Logo, o `forEach` é útil quando o objetivo é somente iterar os itens de uma lista, como por exemplo, exibir todos os valores no console (`console.log`). Já o `map`, é mais apropriado para quando precisamos alterar os valores do array. Com ele, conseguimos alterar os valores sem danificar o array original.


## Exercício 11 - A pequena ovelha Dolly
``` javascript
function clonaObjeto(alvo) {
  var propriedades = Object.getOwnPropertyNames(alvo);
  var copia = {};
  propriedades.forEach(function(propriedade) {
    copia[propriedade] = alvo[propriedade];
  });

  return copia;
}
```

## Exercício 12 - Limpando o estoque
``` javascript
function existeProdutosDatados(produtos, data) {
  var dataReferencia = new Date();
  if(data) dataReferencia = new Date(data);
  return produtos.some(function(produto) {
    return new Date(produto.dataValidade) < dataReferencia;
  });
}
```
