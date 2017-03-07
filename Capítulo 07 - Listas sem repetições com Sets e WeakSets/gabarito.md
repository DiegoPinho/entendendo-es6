# Gabarito

## Exercício 1 - Retirando o excesso
``` javascript
function removeDuplicatas(numeros) {
  return new Set(numeros);
}
```

## Exercício 2 - Um é forte e o outro é fraco, não é isso?
R: No fundo o `WeakSet` é um `Set` que não previne os seus elementos de serem coletados pelo _Garbage Collector_. Uma vez que o elemento não existe mais e seja identificado pelo coletor para ser coletado, ele também é automaticamente removido do `WeakSet`.

## Exercício 3 - Mas na minha máquina funciona!
R: Ao contrário do `Set`, o `WeakMap` não é uma estrutura iterável. Isso significa que não é possível utilizar o laço de repetição `for...of` nela, por isso dá o erro sempre que executado: `TypeError: musicas[Symbol.iterator] is not a function`.

## Exercício 4 - Isso é completamente inútil!
R: Um dos casos de uso mais interessantes é o de garantir que certo método ou propriedade pertence a um objeto específico e não a todas as instâncias do mesmo tipo. Mas no uso geral, sempre que você tiver preocupação com vazamento de memória, o WeakSet estará a seu dispor.
