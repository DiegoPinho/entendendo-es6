# Exercícios

Nestes exercícios iremos exercitar como utilizar as estruturas de Set e WeakSet

## Exercício 1 - Retirando o excesso
Implemente o método 'removeDuplicatas' quer recebe o seguinte parâmetro:
- numeros: lista de números inteiros positivos

O método deve retornar a lista de número sem repetições. Utilize a estrutura de dados `Set` para resolver este problema.

* Exemplo: removeDuplicatas([1,1,2,2,3,3]) → [1,2,3]

## Exercício 2 - Um é forte e o outro é fraco, não é isso?
Qual é a principal diferença entre a estruturas de dados `Set` e `WeakSet`?

## Exercício 3 - Mas na minha máquina funciona!
Um aluno do curso de computação está tentando executar o código a seguir:
``` javascript
var musica1 = {
  titulo: 'O amor não tem rollback',
  autor: 'SQL'
}

var musica2 = {
  titulo: 'Nada se componentiza a você',
  autor: 'React'
}

var musicas = new WeakSet([musica1, musica2]);
for(var musica of musicas){
  console.log(musica);
}
```

Mas sempre que ele tenta executar este código, ele dá erro. Você sabe dizer qual é o problema?

## Exercício 4 - Isso é completamente inútil!
Cite um caso onde podemos utilizar a estrutura de `WeakMap`.
