# Gabarito

## Exercício 1 - Lista de compras
``` javascript
function htmlify(strings, ...values){
  var itens = values[0].split(',');
  var shopItens = itens.map(function(value){
    return `<li>${value}<li>`;
  }).join(""); // remove as vírgulas

  return `<ul>${shopItens}</ul>`;
}
```

## Exercício 2 - Maçaroca de Strings
``` javascript
function criaMacaroca(textos) {
  let textoFinal = '';
  for(let texto of textos) {
    textoFinal = `${textoFinal}${texto}`;
  }

  return textoFinal;
}
```

## Exercício 3 - Quero o seu endereço completo
``` javascript
function montaEnderecoCompleto(rua, cidade, numero, cep) {
  return `${rua}, ${numero} - ${cidade}, ${cep}`;
}
```

## Exercício 4 - Seja muito bem-vindo!
``` javascript
let nome = 'usuario';
console.log(`Bem-vindo ${nome}!`);
```

## Exercício 5 - Cálculo interpolado
``` javascript
function soma(n1,n2) {
  let resultado = `${n1} + ${n2} = ${n1+n2}`;
  console.log(resultado);
}
```
