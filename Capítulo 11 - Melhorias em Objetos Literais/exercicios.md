# Exercícios

1 - Refatore o seguinte código para usar as vantagens oferecidas pelo ES6 em relação a objetos literais.

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
