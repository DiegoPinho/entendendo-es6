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

## Exercício 3 - Oi, eu sou o Goku!
``` javascript
const pessoa = {
  nome: 'Goku',
  equipe: 'Guerreiro Z',
  seApresentar() {
    console.log(`Oi, eu sou o ${this.nome}!`);
  }
}

pessoa.seApresentar(); // Oi, eu sou o Goku!
```

## Exercício 4 - Criando à minha maneira
``` javascript
const caracteristicas = new Map();
caracteristicas.set('nome', 'diego pinho');
caracteristicas.set('idade', 24);

function criaObjetoComCaracteristicas(caracteristicas) {
  const objetoNovo = {};
  for(let caracteristica of caracteristicas.keys()) {
    objetoNovo[caracteristica] = caracteristicas.get(caracteristica);
  }

  return objetoNovo;
}

console.log(criaObjetoComCaracteristicas(caracteristicas));
// {nome: 'diego pinho', idade: 24}
```

## Exercício 5 - Esse tal de JSON
R: O JavaScript Object Notation (JSON) é um formato leve, criado como subconjunto da notação de objetos literais do JavaScript, para troca de dados. Originalmente criado por Douglas Crockford, o formato que é reconhecido devido a sua simplicidade e flexibilidade, não é usado somente no JavaScript, mas na maior parte das linguagens de programação voltadas para web. Ele é muito semelhante a um objeto literal e devido a sua simplicidade, tem sido usado por muitas empresas para criar APIs REST.
