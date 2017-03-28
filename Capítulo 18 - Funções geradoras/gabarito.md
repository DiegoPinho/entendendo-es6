# Gabarito

## Exercício 1 - O que é isso?
**R:** Funções geradoras são funções no JavaScript em que podemos interromper e retornar sua execução várias vezes. Em termos práticos, isso significa que a execução do método é realizada até um ponto e é interrompida até que invocada novamente. Quando invocada, continua sua execução a partir do ponto em que parou. Essas funções são identificadas pela presenta do `*` (asterisco) em sua declaração e da palavra reservada `yield` em sua implementação.

## Exercício 2 - Sinal de parada
**R:**  Quando chamamos uma função geradora, seu corpo não é executado imediatamente. Em vez disso, um objeto iterável é retornado. Esse objeto possui uma função muito útil chamada next. Ao utilizar este método next dele, o corpo da função geradora é executado até a primeira expressão yield, que define o valor que será devolvido no retorno da função.

Logo,
``` javascript
function* testeDeGeradores() {
  console.log('passei aqui!');
  yield 'fim do método';
}

testeDeGeradores().next(); // passei aqui!
```

## Exercício 3 - Corre Bolt!
``` javascript
function* correBolt() {
  console.log('Usain passou no Checkpoint 1');
  yield 'checkpoint 1';
  console.log('Usain passou no Checkpoint 2');
  yield 'checkpoint 2';
  console.log('Usain passou no Checkpoint 3');
  yield 'checkpoint 3';
  console.log('Usain passou no Checkpoint 4');
  yield 'checkpoint 4';
}

let bolt = correBolt();
bolt.next(); // Usain passou no Checkpoint 1
bolt.next(); // Usain passou no Checkpoint 2
bolt.next(); // Usain passou no Checkpoint 3
bolt.next(); // Usain passou no Checkpoint 4
```

## Exercício 4 - Temos que pegar!
``` javascript
function* capturaTodosOsPokemons() {
  yield 'Pikachu';
  yield 'Charmander';
  yield 'Caterpie';
}

for(let pokemon of capturaTodosOsPokemons()) {
	console.log(`Capturou o ${pokemon}!`);
}
```

## Exercício 5 - Símbolos dizem até demais
``` javascript
const equipe = {
  gerente: 'Gilberto',
  estagiario: 'Fernanda',
  senior: 'Paulo',
  pleno: 'Camila',
  junior: 'Adão',
  [Symbol.iterator]: function* () {
    yield this.gerente;
    yield this.estagiario;
    yield this.senior;
    yield this.pleno;
    yield this.junior;
  }
}

for(let integrante of equipe) {
  console.log(integrante);
}
```
