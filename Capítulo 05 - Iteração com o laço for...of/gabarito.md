# Gabarito

## Exercício 1 - Contando o faturamento
``` javascript
function somaFaturamento(valores) {
  var total = 0;
  for(var valor of valores) {
    total += valor;
  }

  return total;
}
```

## Exercício 2 - Por quê não funciona?
R: Neste capítulo vimos que a estrutura por debaixo dos panos acessa o iterador da estrutura a cada passo da iteração. É por isso que quando ele tentou iterar o objeto literal `Casa`, ele obteve um erro. Ao invés disso, os atributos estivessem dentro de um `Array`, teria funcionado sem problemas.

## Exercício 3 - Agora vai funcionar
``` javascript
var Casa = {
  metrosQuadrados: 4000,
  altura: 3000,
  nQuartos: 4,
  nBanheiros: 2

  //...
}

for(var atributo in Casa) {
  console.log(atributo + ' : ' + Casa[atributo]);
}
```

## Exercício 4 - Pare aqui senhor motorista
``` javascript
function percorreRuas(ruas, parada) {
  for(var rua of ruas) {
    console.log(rua);
    if(rua === parada) break;
  }
}
```

## Exercício 5 - Não vá por ali!
``` javascript
function percorreRuas(ruas, ruaPerigosa) {
  for(var rua of ruas) {
    if(rua === ruaPerigosa) continue;
    console.log(rua);
  }
}
```
