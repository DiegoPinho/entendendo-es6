# Exercícios

1 - Refatore o código a seguir para utilizar o operador Rest:

``` javascript
function produto(a, b, c, d, e) {
  var numeros = [a,b,c,d,e];

  return numeros.reduce(function(produto, numero) {
    return produto * numero;
  }, 1)
}
```

2 - Utilize o operador Rest para criar uma função que recebe um parâmetro referência, que é obrigatório, e mais n parâmetros numéricos. O objetivo é que esta função calcule se todos os valores numéricos passados são maiores que a referência e retorne verdadeiro ou falso.

Exemplo:
todosSaoMaioresQue(2,3,4,5,6,7); // resultado esperado: true

Outros exemplos de entradas:
todosSaoMaioresQue(5,4,3,2,1); // resultado esperado: false
todosSaoMaioresQue(1,2); // resultado esperado: true
