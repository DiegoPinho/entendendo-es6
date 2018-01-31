# Exercícios

Nestes exercícios vamos rever como funcionam as novidades trazidas pelo ES7 (ES2016).

## Exercício 1 - Você está ai?
Utilizando o `Array.prototype.includes`, refatore o código abaixo para indicar se uma dada String está contida dentro de um Array.

``` javascript
function possuiNumero(texto, termo) {
  let achou = false;
  const termos = texto.split(' ');
  for(let i = 0; i < termos.length; i++){
    if(termos[i] === termo) {
      achou = true; 
      break;
    }   
  }

  return achou;
}

possuiNumero('Era uma vez', 'vez'); // true
possuiNumero('Dois mais dois é quatro', 'mais'); // true
possuiNumero('Não há nada aqui', 'quadro'); // false
```

## Exercício 2 - ARÁ! Essa você não resolve
Qual o caso em que a função `indexOf` não consegue nos ajudar em identifica se existe um dado elemento dentro de um array?

## Exercício 3 - Hora de exponenciar
Refatore a função a seguir para utilizar o novo operador de exponenciação ao invés da função `Math.pow`.

``` javascript
function exponencial(base, expoente) {
  return Math.pow(base, expoente);
}

exponencial(2,2); // 4
exponencial(2,3); // 8
exponencial(3,2); // 9
```