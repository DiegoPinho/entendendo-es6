# Gabarito

## Exercício 1
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

## Exercício 2
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
