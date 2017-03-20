# Gabarito

## Exercício 1 - Hora do ditado
``` javascript
const ditado = ['e','c','m','a','s','c','r','i','p','t'];
console.log(...ditado);
```

## Exercício 2 - Não são só umas reticências?
**R:** Apesar de ambos utilizarem a notação `…` (três pontos), o funcionamento deles é totalmente diferente:

* O operador Rest coleta os itens e coloca-os em um Array;
* O operador Spread torna um Array (e outros objetos iteráveis) em itens individuais.

## Exercício 3 - Contador de Vogais
``` javascript
function contaQuantidadeVogaisNaoAcentuadas(...palavras) {
  let ocorrencias = 0;
  for(let palavra of palavras) {
    let palavraLowerCase = palavra.toLowerCase();
    const letras = [...palavraLowerCase];
    for(let letra of letras) {
      if("aeiou".indexOf(letra) !== -1) {
        ocorrencias++;
      }
    }
  }

  return ocorrencias;
}
```

## Exercício 4 - Esse jeito é tão ultrapassado...
É possível através do método `apply`:

``` javascript
var argumentos = [1,2,3];
console.log.apply(console, argumentos);
// 1, 2, 3
```

## Exercício 5 - A união faz a força
``` javascript
const equipeMarketing = ['Joana', 'Marcela', 'Bruna'];
const equipeComercial = ['Talita', 'Luisa', 'Vitória'];

const timeCompleto = [...equipeComercial, ...equipeMarketing];

realizaBrainstorm(timeCompleto);
```
