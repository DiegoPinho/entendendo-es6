# Gabarito

## Exercício 1
``` javascript
function htmlify(strings, ...values){
  var itens = values[0].split(',');
  var shopItens = itens.map(function(value){
    return `<li>${value}<li>`;
  }).join(""); // remove as vírgulas

  return `<ul>${shopItens}</ul>`;
}
```
