# Gabarito

## Exercício 1 - Tim tim por tim tim
``` javascript
function mapeiaObjeto(objeto) {
  return new Map(Object.entries(objeto));
}

const mapa = detalhaObjeto(
  {
    nome: 'joão bobão',
    idade: 32,
    sexo: 'masculino'
  }
);

mapa.get('nome'); // 'joão bobão
mapa.get('idade'); // 32
mapa.get('sexo'); // masculino
```

## Exercício 2 - Queros dados completos
``` javascript
function detalhaObjeto(objeto) {
  for (let [chave, valor] of Object.entries(objeto)) {
    console.log(`${chave}: ${valor}`);
  }
}

detalhaObjeto(
  {
    nome: 'joão bobão',
    idade: 32,
    sexo: 'masculino'
  }
);

/*
nome: joão bobão
idade: 32
sexo: masculino
*/
```

## Exerício 3 - Ih, não deu ._.
**R:** Quando há um símbolo como chave. Como por exemplo: 
``` javascript
Object.entries({ [Symbol()]: 123});
// [ [ ] ]
```

## Exercício 4 - Prove o seu valor
``` javascript
function somenteValores(objeto) {
  for (let valor of Object.values(objeto)) {
    console.log(valor);
  }
}

somenteValores(
  {
    nome: 'joão bobão',
    idade: 32,
    sexo: 'masculino'
  }
);

/*
joão bobão
32
masculino
*/
```

## Exercício 5 - Tudo para a direita!
``` javascript
function tudoParaADireita(palavras, tamanho) {
  palavras.forEach(palavra => {
    console.log(palavra.padStart(tamanho));
  })
}

tudoParaADireita([
  'carro', 'avião', 'foguete', 'helicóptero'  
], 11);

/*
      carro
      avião
    foguete
helicóptero
*/
```

## Exercício 6 - Eu disse direita? Eu quis dizer esquerda!
``` javascript
function tudoParaAEsquerda(palavras, tamanho) {
  palavras.forEach(palavra => {
    console.log(palavra.padEnd(tamanho,'-'));
  })
}

tudoParaAEsquerda([
  'carro', 'avião', 'foguete', 'helicóptero'  
], 11);

/*
carro------
avião------
foguete----
helicóptero
*/
```

## Exercício 7 - Quantos enumeráveis eu tenho na minha mão?
``` javascript
function quantidadePropriedadesEnumeraveis(objeto) {
  let contador = 0;
  const propsDescriptors = Object.getOwnPropertyDescriptors(objeto);
  for(let [chave,] of Object.entries(objeto)) {
    if(propsDescriptors[chave].enumerable) contador++;
  }

  return contador;
}

quantidadePropriedadesEnumeraveis({nome: 'jão'}); // 1
```