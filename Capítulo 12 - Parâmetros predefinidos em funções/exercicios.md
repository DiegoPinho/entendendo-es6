# Exercícios

1 - Refatore o código a seguir utilizando parâmetros padrão de função:

``` javascript
function soma(a,b) {
  if(a === undefined) {
    a = 0;
  }
  if(b === undefined) {
    b = 0;
  }

  return a + b;
}
```
