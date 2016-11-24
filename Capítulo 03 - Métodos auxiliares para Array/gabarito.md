# Gabarito

## Exercício 1 - Par ou ímpar?
``` javascript
var numeros = [0,1,2,3,4,5];
numeros.forEach(function(numero){
    if(numero % 2 === 0) {
        console.log(numero + ' é par');
    } else {
        console.log(numero + ' é ímpar');
    }
});
```

## Exercício 2 - Quero o dobro
``` javascript
function dobrar(numeros) {
    return numeros.map(function(numero){
        return numero * 2;
    });
}
```

## Exercício 3 - NÃO ESTOU BRAVO
``` javascript
function caps(palavras) {
    return palavras.map(function(palavra){
        return palavra.toUpperCase();
    });
}
```

## Exercício 4 - Equilibrio de parênteses
``` javascript
function validaParenteses(parenteses) {
  var arrayParenteses = validaParenteses.split(""); // reduce só funciona com arrays
  /**
   * Vamos utilizar números para essa solução. Para cada parêntese esquerdo, vamos
   * somar 1 e para cada parêntese direito vamos subtrair um
   **/
  var balanceado =  !arrayParenteses.reduce(function(soma, parentese) {
    if(soma < 0) { return soma } // para o caso de começar com ")"
    if(parentese ==  "(") { return soma++ }
    if(parentese ==  ")") { return soma-- }
  }, 0);

  return balanceado;
}
```

## Exercício 5 - Sem duplicações
``` javascript
function unique(array) {
  return array.reduce(function(previous, value) {
     var foundDuplicate = previous.find(function(value2){
         return value === value2;
     });

     if(!foundDuplicate){
        previous.push(value);
     }

     return previous;
  }, []);
}
```

## Exercício 6 - Reprovado!
``` javascript
function aprovados(alunos, media) {
  return alunos.filter(function(aluno){
    return aluno.media >= media;
  });
}
```
