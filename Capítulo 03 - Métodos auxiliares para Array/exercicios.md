# Exercícios

Nestes exercícios iremos exercitar os métodos auxiliares para array:
* forEach
* map
* filter
* find
* every
* some
* reduce

## Exercício 1 - Par ou ímpar?
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

* Exemplo: validaParenteses(')((()()())))'); →  false
* Exemplo: "()()()" → true
* Exemplo: ")(" → false

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
Crie uma função `buscar` que recebe três parâmetros:
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

## Exercício 8 - Calculadora humana
Crie uma função `calculaAreaTotal` que recebe um parâmetro:
- dimensoes: objeto que possui as propriedades `altura` e `comprimento` que são números inteiros

A função deve retornar a soma de todas as áreas.
Tome como base a entrada a seguir:

``` javascript
var dimensoes = [
  { altura: 10, comprimento: 20},
  { altura: 2, comprimento: 4},
  { altura: 1, comprimento: 1},
  { altura: 50, comprimento: 50}
]
```

* Exemplo: calculaAreaTotal(dimensoes) → 2709

## Exercício 9 - Raízes quadradas
Crie uma função chamada `calculaRaizesQuadradas` que recebe um array de números inteiros positivos e devolve um outro array com as raízes quadradas correspondentes de cada um dos itens.

* para este exercício, assuma que a entrada terá somente números com raiz exata.
* utilize a função Math.sqrt para calcular a raiz quadrada

## Exercício 10 - E tem alguma diferença?
Diga, em poucas palavras, qual a diferença entre os métodos auxiliares `forEach` e `map`.

## Exercício 11 - A pequena ovelha Dolly
Utilizando o método auxiliar `forEach`, crie uma função `clonaObjeto` que recebe como parâmetro um objeto e cria uma cópia exata dela.

* utilize o método `Object.getOwnPropertyNames` para obter as propriedades do objeto

## Exercício 12 - Limpando o estoque
Crie um método chamado `existeProdutosDatados` que recebe um parâmetro chamado `produtos` que é um array de `produtos` e identifica se há algum produto que está acima da data de validade. Caso existe, deve voltar `true`, caso contrário, `false`. Cada produto tem as seguintes características:
- nome: String que representa o nome do produto
- preco: Número que representa o preço do produto
- dataValidade: Data de validade do produto

O método também deve aceitar um segundo parâmetro `dataReferencia`. Se passado, o método deve fazer a comparação de validade em relação a ele, caso contrário, utiliza a data da execução como parâmetro.

Tome como exemplo os produtos a seguir:
``` javascript
var produtos = [
  { nome:'Cereal', preco:'10', dataValidade:'21/02/2017' },
  { nome:'Suco de Abacaxi', preco:'12', dataValidade:'01/01/2017' },
  { nome:'Torta de frango', preco:'25', dataValidade:'07/07/2017' }
]
```

* Exemplo: existeProdutosDatados(produtos, '2017-03-01') → true
* existeProdutosDatados(produtos,'2016-01-01') → false
