# Gabarito

## Exercício 1 - Você está muito longe
``` javascript
function calculaDistancia(ruas) {
  var iteradorRuas = ruas[Symbol.iterator]();
  var distanciaTotal = 0;
  var rua = iteradorRuas.next();
  do {
    distanciaTotal += rua.value.tamanho;
    rua = iteradorRuas.next();
  }
  while (!rua.done);

  return distanciaTotal;
}
```

## Exercício 2 - Tem alguém ai?
``` javascript
function isListaVazia(lista) {
  return lista[Symbol.iterator]().next().done;
}
```

## Exercício 3 - S-o-l-e-t-r-a-n-d-o
``` javascript
function soletraPalavra(palavra) {
  var iteradorPalavra = palavra[Symbol.iterator]();
  var letra = iteradorPalavra.next();
  do {
    console.log(letra.value);
    letra = iteradorPalavra.next();
  } while (!letra.done);
}
```

## Exercício 4 - Eu prefiro o meu
``` javascript
function criaIterador(array) {
   var proximoIndice = 0;

    return {
       next: function() {
           if(proximoIndice < array.length) {
             return { value: array[proximoIndice++], done: false };
           } else {
             return { value: undefined, done: true };
           }
       }
    };

}
```
