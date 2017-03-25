# Exercícios

Nestes exercícios vamos revisar como o desestruturamento de objetos funciona.

## Exercício 1 - Desestruturando a definição
De forma resumida, defina o que é o desestruturamento.

## Exercício 2 - Pegando a propriedade na lata
Refatore o trecho de código a seguir para utilizar a técnica de desestruturamento.

``` javascript
const email = usuario.email;
const nome = usuario.nome;
const idade = usuario.idade
```

## Exercício 3 - Não gostei desse nome não
Considere o objeto literal `usuario` e extraia as propriedades `nome` e `email` em variáveis com o nome `nick` e `login`, respectivamente.

``` javascript
const usuario = {
  nome: 'Toreto',
  email: 'velozesefuriososparasempre@gmail.com'
}
```

## Exercício 4 - Minha mãe mandou eu escolher esse daqui...
Considere a lista de contatos a seguir:
``` javascript
const contatos = [
  {
    nome: 'Mario Antonio',
    numero: '1234-5678'
  },
  {
    nome: 'Reinalda Silva',
    numero: '1234-6789'
  },
  {
    nome: 'Bárbara Lopes',
    numero: '1234-5567'
  }
];
```

Utilizando a técnica de desestruturamento de arrays, obtenha somente os dados do segundo contato.

## Exercício 5 - Cara-Crachá
Otimize o trecho de código a seguir utilizando o desestruturamento.
``` javascript
const profissional = {
  titulo: 'Engenheiro de Software',
  departamento: 'Engenharia'
};

function isEngenheiro(profissional) {
  const titulo = profissional.titulo;
  const departamento = profissional.departamento;

  return titulo.indexOf("Engenheiro") > -1 && departamento === 'Engenharia';
}

isEngenheiro(profissional); // true
profissional.titulo = 'Marketing';
isEngenheiro(profissional); // false
```

## Exercício 6 - Mas o que são estes dados!?
O seu sistema escolar contém uma série de informações armazenadas em arrays no seguinte formato:

``` javascript
const corpoDocente = [
  [ 'Gramática', '9:00', 'Sueli' ],
  [ 'Matemática', '10:15', 'Amilton'],
  [ 'Educação Física', '11:30', 'Bruno' ]
];
```

Para o usuário final, é necessário que a informação seja apresentada de uma forma mais adequada, identificando o que significa cada um dos itens. Implemente o método `mostraGradeProfessores()` quer recebe um array de arrays no formato do objeto `corpoDocente` e devolve, para cada item, a seguinte mensagem no console:

``` javascript
"Aula de <matéria> às <hora> com professor(a) <nome>"
```

## Exercício x - Converta do modelo 1 para o modelo 2 utilizando desestruturamento de objetos e arrays.
``` javascript
// modelo1
const pontos = [
  [1,2],
  [3,4],
  [5,6]
];

// modelo 2
const pontos = [
  {x:1, y:2},
  {x:3, y:4},
  {x:5, y:6},
]
```
