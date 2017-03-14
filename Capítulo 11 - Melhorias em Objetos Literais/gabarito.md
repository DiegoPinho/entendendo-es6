# Gabarito

## Exercício 1 - Dando um trato no busão
``` javascript
const modelo = 'Mercedes-Benz Monobloco O-371 RSL';
const ano = 1993;
const capacidade = 50;

const acelerar = () => console.log('vrum vrum');

var busao = {
  modelo, ano, capacidade, acelerar
}

busao.acelerar(); // vrum vrum
```

## Exercício 2 - Corta isso fora
``` javascript
const dimensoes = (comprimento, alturaInicial) => {
  return {
    comprimento,
    altura: alturaInicial * 9 /16
  };
}

console.log(dimensoes(10,10)); // { comprimento: 10, altura: 5.625 }
```
