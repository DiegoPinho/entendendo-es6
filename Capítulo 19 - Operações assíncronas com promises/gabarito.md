# Gabarito

## Exercício 1 - Promessa verdadeira
**R:** Promises são objetos que nos auxiliam a trabalhar com operações assíncronas. Este tipo de objeto aguarda a operação ser completada e oferece uma resposta positiva (resolvida) para quando realizada com sucesso, ou negativa caso algo tenha ocorrido algum erro no processo (rejeitada).

## Exercício 2 - E que tudo mais vá para o inferno
**R:** Este nome foi dado para a situação na qual temos várias chamadas assíncronas que dependem uma da outra. Como as operações assíncronas ocorrem simultaneamente e respondem em tempos diferentes, torna-se uma tarefa extremamente árdua para o desenvolver entender o que acontece na execução deste código. As Promises foram criadas para que o desenvolvedor possa lidar melhor com as inúmeras chamadas assíncronas no código.

## Exercício 3 - Você cumpre as suas promessas?
``` javascript
function simulaPromise(sucesso = true) {
    let promise = new Promise((resolve, reject) => {
      if(sucesso) {
        resolve("ok");
      } else {
        reject("not ok");
      }
    });

    promise.then(data => console.log(`${data}`));
    promise.catch(data => console.log(`${data}`));
}

simulaPromise(); // ok
simulaPromise(true); // ok
simulaPromise(false); // not ok
```

## Exercício 4 - Você cumpre as suas promessas em tempo?
``` javascript
function simulaPromise(sucesso = true, delay = 0) {
    let promise = new Promise((resolve, reject) => {
      setTimeout(() => {
          if(sucesso) {
            resolve("ok");
          } else {
            reject("not ok");
          }
      }, delay);
    });

    promise.then(data => console.log(`${data}`));
    promise.catch(data => console.log(`${data}`));
}

simulaPromise(true, 2000); // ok
simulaPromise(false, 1000); // not ok

// ordem que aparece no console
// not ok
// ok
```

## Exercício 5 - Passando promessa de pai para filho
**R:** O problema é que na execução do segundo `then`, o resultado da variável `data` será `undefined`. Isso acontece porque o valor da variável `data`, disponível na primeira chamada, não é passada adiante. Para resolver isso, basta fazer a seguinte alteração:

``` javascript
// ...
promise
  .then((data) => {
    console.log(`resultado positivo: ${data}`);
    return data;
  })
  .then((data) => console.log(`resultado positivo 2: ${data}`))
  .catch((data) => console.log(`resultado negativo: ${data}`));
```
