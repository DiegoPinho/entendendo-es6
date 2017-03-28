# Exercícios

Nos exercícios a seguir iremos rever os principais aspectos das funções geradoras.

## Exercício 1 - O que é isso?
Em termos simples, explique o que são funções geradoras e como podemos identificá-las.


## Exercício 2 - Sinal de parada
Considere o trecho de código a seguir:
``` javascript
function* testeDeGeradores() {
  console.log('passei aqui!');
  yield 'fim do método';
}
```

Ao executar o método, a frase "passei aqui!" não é exibida no console como esperado. Por quê? O que é necessário fazer para que a mensagem seja exibida?


## Exercício 3 - Corre Bolt! Corre!
Implemente uma função geradora chamada 'correBolt' que retorna para cada parada um checkpoint. Em cada checkpoint, deve ser impresso a mensagem: `Usain passou no Checkpoint X`, onde "X" indica o número do checkpoint. A função deve ter quatro paradas. Não se esqueça de invocar o método `next`.


## Exercício 4 - Temos que pegar!
Refatore o trecho de código a seguir utilizando todas as melhorias propostas pelo ES6 até então. Use obrigatoriamente funções geradoras.

``` javascript
var pokemons = ['Pikachu', 'Charmander', 'Caterpie'];
for(var index = 0; index < pokemons.length; index++) {
	var pokemon = pokemons[index];
	console.log('Capturou o ' + pokemon + '!');
}
```

## Exercício 5 - Símbolos dizem até demais
Considere o seguinte objeto `equipe` representada pelo código que segue:
``` javascript
const equipe = {
  gerente: 'Gilberto',
  estagiario: 'Fernanda',
  senior: 'Paulo',
  pleno: 'Camila',
  junior: 'Adão'
}
```

Faça com que o objeto `equipe` se torne iterável em um laço de repetição do tipo `for...of`.

Exemplo:
``` javascript
for(let integrante of equipe) {
  console.log(integrante);
}

/*
Gilberto
Fernanda
Paulo
Camila
Adão
*/
```
