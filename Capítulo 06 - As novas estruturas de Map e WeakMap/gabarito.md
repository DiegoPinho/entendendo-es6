# Gabarito

## Exercício 1 - Você tem esse produto?
``` javascript
function possuiProduto(produtos, produtoDesejado) {
  return produtos.has(produtoDesejado);
}
```

## Exercício 2 - Comprinhas online
``` javascript
var caixa = new Map();
caixa.set('Arroz', 7.10);
caixa.set('Feijão', 2.30);
caixa.set('Macarrão', 4.70);
caixa.set('Refrigerante', 3.00);

var fretes = new Map();
fretes.set('São Paulo', 10.10);
fretes.set('Rio de Janeiro', 12.30);
fretes.set('Brasília', 14.70);

function calculaValorTotalDaCompra(produtos, cidade, caixa, fretes) {
  var total = 0;
  for(var produto of produtos) {
    total += caixa.get(produto);
  }

  var frete = 13.00;
  if(fretes.has(cidade)) {
    frete = fretes.get(cidade);
  }

  return(total + frete);
}
```

## Exercício 3 - Não sei qual algoritmo usar hoje
R: Há algumas perguntas que podemos nos fazer que nos ajudam a decidir quando um `Map` ou um objeto literal:
* As chaves são desconhecidas até o tempo de execução,
você precisa procurá-las dinamicamente?
* Todos os valores sempre serão do mesmo tipo, e podem
ser usados de forma intercambiável?
* Você precisa de chaves que não são Strings?
* Os pares chave/valor são adicionados ou removidos
frequentemente?
* Você tem uma quantidade de pares chave/valor
arbitrária (de troca fácil)?
* A coleção é iterada?

Se as respostas para as perguntas forem positivas, são sinais de que você provavelmente queremos usar uma instância de Map.

## Exercício 4 - Professor, quando eu vou usar isso na minha vida?
R: É possível utilizar esta estrutura para criar dados privados dentro de uma classe JavaScript.

## Exercício 5 - Não vou mais com a sua cara.
``` javascript
var amigos = new Map();
amigos.set('João Silva', {idade:23, sexo:'masculino'});
amigos.set('Luisa Pimenta', {idade:18, sexo:'feminino'});
amigos.set('Julio Marinho', {idade:52, sexo:'masculino'});
amigos.set('Marcela Mel', {idade:27, sexo:'feminino'});

function deletaAmigos(amigos, exAmigos) {
  for(var exAmigo of exAmigos) {
    if(amigos.has(exAmigo)) {
      amigos.delete(exAmigo);
      console.log(exAmigo + ' foi deletado!');
    }
    else {
      console.log(exAmigo + ' não é seu amigo!');
    }
  }
}
```
