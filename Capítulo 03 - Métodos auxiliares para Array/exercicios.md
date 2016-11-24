# Exercícios

Nestes exercícios iremos exercitar os métodos auxiliares para array:
* forEach
* map
* filter
* find
* every
* some
* reduce

## Exercício 1 - Par ou Ímpar?
Altere o código a seguir para utilizar o método `forEach` de modo que a saída permaneça a mesma.

``` javascript
var numeros = [0,1,2,3,4,5];
for(var i = 0; i<= numeros.length; i++) {
    if(i % 2 === 0) {
        console.log(i + ' é par');
    } else {
        console.log(i + ' é ímpar');
    }
}

// saída:
// 0 é par
// 1 é ímpar
// 2 é par
// 3 é ímpar
// 4 é par
// 5 é ímpar
```

## Exercício 2 - Quero o dobro
Utilizando o método `map`, escreva o método `dobrar` que recebe um array de números inteiros e retorna um array com todos os valores do array original dobrados.

* Exemplo: dobrar([1,2,3]) → [2,4,6]

## Exercício 3 - NÃO ESTOU BRAVO
Escreva o método `caps` que recebe um array de strings e retorna um outro array com todas as strings do array original em CAIXA ALTA.

* Exemplo: caps(['oi', 'tudo', 'bem?']) → ['OI', 'TUDO', 'BEM?']

## Exercício 4 - Equilibrio de parênteses
Utilizando a função auxiliar `reduce`, escreva uma função chamada `validaParenteses` que avalia se os parênteses estão balanceados. Isso significa que, pra cada parênteses esquerdo “(“ é necessário ter um parênteses direito “)” correspondente. A função deve aceitar uma `string` e retornar um valor booleano (true ou false).

* Exemplo: validaParenteses(“)((()()())))”); →  false
* Exemplo: “()()()”, “(())” → true
* Exemplo: “)(”, “())” → true

## Exercício 5 - Sem duplicações
Faça uma função chamada `removeDuplicatas` que recebe um array de números inteiros e remove todas as suas duplicadas.

Utilize as funções auxiliares: `reduce` e `find`.

* Exemplo: removeDuplicatas([1,2,3,3,4,5]) → [1,2,3,4,5]

## Exercício 6 - Reprovado!
Dada uma lista de objetos que contém o nome de um aluno e sua média final, crie o método 'aprovados' que recebe esta lista e retorna somente os alunos que foram aprovados.

Para isto, utilize o método `filter`.

``` javascript
var alunos = [
  { nome: 'Diogo', media: 5.5 },
  { nome: 'Julia', media: 9.5 },
  { nome: 'Roberto', media: 1.5 },
  { nome: 'Tiago', media: 6.0 }
];
```

* Exemplo: aprovados(alunos, 6.5) → [ { nome: 'Julia', media: 9.5 } ]

## Exercício 7 - Dados precisos
Crie uma função `buscar` que recebe dois parâmetros:
- propriedade: Nome da propriedade no objeto
- valor: Valor da propriedade no objeto
- lista: Lista de objetos onde a busca deve ser executada

Dado estes parâmetros, a função deve buscar na lista e retornar o registro que possui a propriedade com o valor especificado.

Utilize o método `find`.

``` javascript
var lista = [
    { nome: 'Tânia', sobrenome: 'Cardoso', idade: 65 },
    { nome: 'Emilly', sobrenome: 'Barbosa', idade: 46 },
    { nome: 'Vitória', sobrenome: 'Costa', idade: 83 },
    { nome: 'Erick', sobrenome: 'Ferreira', idade: 16 }
]
```

* Exemplo: buscar('nome', 'Tânia', lista) → { nome: 'Tânia', sobrenome: 'Cardoso', idade: 65 }

## Exercício xx
Utilizando o método auxiliar `forEach`, crie uma função `copiarObjeto` que recebe como parâmetro um objeto e cria uma cópia exata dela.
https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach

## Exercício xx
Crie uma função chamada `calculaRaizesQuadradas` que recebe um `Array` de números inteiros positivos e devolve um outro `Array` com as raízes quadradas correspondentes de cada um dos itens.

## Exercício xx
Crie uma função com o nome de `encontreNaLista` que recebe dois parâmetros:
* array de objetos com atributos distintos
* objeto com atribuitos de busca

Faça com que o método retorne um array com todos os elementos que possui todos os critérios de busca.
