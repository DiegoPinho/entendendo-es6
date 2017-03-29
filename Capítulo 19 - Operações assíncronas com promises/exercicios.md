# Exercícios

Nos exercícios a seguir iremos rever as operações assícronas com promises.

## Exercício 1 - Promessa verdadeira
Em poucas palavras, diga o que são as Promises.

## Exercício 2 - E que tudo mais vá para o inferno
O que é `callback hell` e qual a sua relação com as Promises?

## Exercício 3 - Você cumpre as suas promessas?
Implemente o método simulaPromise() que recebe um parâmetro chamado `sucesso` que é um Boolean que indicará se a Promise foi realizada com sucesso ou não. O método deve receber esta parâmetro e imprimir a mensagem: `ok` em caso de sucesso e `not ok` no caso contrário.

Exemplo:
``` javascript
simulaPromise(false); // not ok
simulaPromise(true); // ok
```

Não se esqueça de utilizar o `resolve`, `reject`, `then` e `catch` para resolver o exercício.

## Exercício 4 - Você cumpre as suas promessas em tempo?
Para melhorar a simulação de Promise criada no exercício anterior, faça com o método receba mais um argumento chamado `delay` que é um inteiro que representa os milisegundos que a solicitação demora para responder. Ao executar o método, ele deve demorar o tempo do `delay` para exibir a mensagem no console.

Exemplo:
``` javascript
simulaPromise(true, 2000); // ok
simulaPromise(false, 1000); // not ok

// ordem que aparece no console
// not ok
// ok
```

## Exercício 5 - Passando promessa de pai para filho
Qual é o problema com o trecho de código a seguir? E como consertá-lo?
``` javascript
// ...
promise
  .then((data) => console.log(`resultado positivo: ${data}`))
  .then((data) => console.log(`resultado positivo 2: ${data}`))
  .catch((data) => console.log(`resultado negativo: ${data}`));
```
