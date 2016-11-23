# Exercícios

1 - Utilizando Templates Literais Marcadas, crie uma tag que transforma uma String que representa uma lista de compras (divididas por vírgula) em um elemento de lista HTML (&lt;ul&gt; com &lt;li&gt;).

Por exemplo:
``` javascript
const compras = ‘leite,feijão,arroz,mandioca’;
var elemento = tag`${compras}`;

console.log(elemento)
// <ul><li>leite<li><li>feijão<li><li>arroz<li><li>mandioca<li></ul>
```
