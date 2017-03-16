# Gabarito

## Exercício 1 - O dobro de nada
``` javascript
mostraNome(); // Meu nome é undefined
```
R: No JavaScript, quando declaramos e invocamos funções, elas possuem por definição seus parâmetros com o valor `undefined` como padrão. Como não passamos nenhum valor para a função, ele assumiu o `undefined`.


## Exercício 2 - Me passa uns parâmetros ae
``` javascript
function soma(a = 0, b = 0) {
  return a + b;
}
```

## Exercício 3 - Tá aqui a minha identidade
``` javascript
function imprimeNomeCompleto(nome = '', sobrenome='', nomeDoMeio='') {
  console.log(`${nome} ${nomeDoMeio} ${sobrenome}`);
}

imprimeNomeCompleto('João'); // João
```

## Exercício 4 - Adivinha em quem eu estou pensando?
``` javascript
Ao executar esta função, percebemos que o valor atribuído ao padrão é "valor 1" e não "valor 2". Isso aconteceu exatamente por causa do escopo de bloco que vimos no capítulo de const e let. Se removemos a primeira declaração da variável v, somos presenteados com um belo erro: `ReferenceError: v is not defined`
```

## Exercício 5 - Pare de me imitar!
``` javascript
function subtrair(a = 0,b = a) {
  return a + b;
}
```
