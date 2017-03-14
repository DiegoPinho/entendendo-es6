# Exercícios

Nestes exercícios, iremos reforçar como fazer uso das melhorias em objetos literais.

## Exercício 1 - Dando um trato no busão
Refatore o seguinte código para usar as vantagens oferecidas pelo ES6 em relação a objetos literais.

``` javascript
var modelo = 'Mercedes-Benz Monobloco O-371 RSL';
var ano = 1993;
var capacidade = 50;

var acelerar = function() {
  console.log('vrum vrum');
}

var busao = {
  modelo: modelo,
  ano: ano,
  capacidade: capacidade,
  acelerar : acelerar
}

busao.acelerar(); // vrum vrum
```

## Exercício 2 - Corta isso fora
Refatore o código abaixo com o que foi aprendido até agora.
``` javascript
var dimensoes = function(comprimento, alturaInicial) {
  var altura = alturaInicial * 9 /16;
  return { comprimento : comprimento, altura : altura };
}

console.log(dimensoes(10,10)); // { comprimento: 10, altura: 5.625 }
```
