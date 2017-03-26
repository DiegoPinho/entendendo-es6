# Gabarito

## Exercício 1 - Dando uma transformada nos objetos
``` javascript
class VideoGame {
  constructor(marca, nControles, tipoMidia) {
    this.marca = marca;
    this.nControles = nControles;
    this.tipoMidia = tipoMidia;
  }
}

let playstation = new VideoGame('sony', '2', 'dvd');
console.log(playstation);
// { marca: 'sony', nControles: '2', tipoMidia: 'dvd' }
```

## Exercício 2 - O meu videogame é muito melhor que o seu
``` javascript
class VideoGame {
  constructor(marca, nControles, tipoMidia) {
    this.marca = marca;
    this.nControles = nControles;
    this.tipoMidia = tipoMidia;
  }
}


class PlayStation extends VideoGame {
  constructor(marca, nControles, tipoMidia, nEntradasUSB, voltagem, adicionais) {
    super(marca, nControles, tipoMidia);
    this.nEntradasUSB = nEntradasUSB;
    this.voltagem = voltagem;
    this.adicionais = adicionais;
  }
}


let playstation = new PlayStation('sony', 2, 'dvd', 2, 2, ['Volante']);
console.log(playstation);
/*
{
  marca: 'sony',
  nControles: 2,
  tipoMidia: 'dvd',
  nEntradasUSB: 2,
  voltagem: 2,
  adicionais: [ 'Volante' ]
}
*/
```

## Exercício 3 - Tem alguém ai?
``` javascript
class Porta {
  static toctoc() {
    console.log('Quem é?');
  }
}

Porta.toctoc(); // Quem é?
```

## Exercício 4 - Qual é o jeito certo de fazer isso então?
**R:** No ES5, quando criamos objetos por meio de funções, temos o comportamento de _hoisting_. Isto é, dentro de um escopo, as funções que são declaradas são imediatamente disponíveis para uso — independente de onde as declarações acontecem. Porém, declarações de classes não possuem este comportamento. A classe só existe quando a execução do código chega ao ponto onde a classe é avaliada. Se tentarmos acessar antes, tomaremos um `ReferenceError`. Para que o código funcione, basta trocar a ordem das declarações:


``` javascript
class Comida {
  constructor(nome) {
    this.nome = nome;
  }
}

const comida = new Comida('Feijão');
```

## Exercício 5 - Declarações anônimas
``` javascript
const Computador = class {
  // conteúdo da classe
}
```
