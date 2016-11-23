# Exercícios

## Exercício 1
Considere o trecho de código abaixo e responda as questões:

``` javascript
var arrayFuncoes = [];
for(var i = 0; i < 10; i++){
  arrayFuncoes.push(function(){
    console.log(i);
  });
}

arrayFuncoes.forEach(function(funcao){
  funcao();
});
```
a) Quais os valores são exibidos no console na execução desse código?
b) Como podemos ajustar o comportamento desta função utilizando ES6?
