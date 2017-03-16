# Exercícios

Neste exercícios vamos exercitar como utilizar parâmetros padrões em funções.

## Exercício 1 - Quem é você?
O que acontece na execução do código a seguir?

``` javascript
function mostraNome(nome) {
    console.log(`Meu nome é: ${nome}`);
}

mostraNome(); // ??
```

## Exercício 2 - Me passa uns parâmetros ae
Refatore o código a seguir utilizando parâmetros padrão de função.

``` javascript
function soma(a,b) {
  if(a === undefined) {
    a = 0;
  }
  if(b === undefined) {
    b = 0;
  }

  return a + b;
}
```

## Exercício 3 - Tá aqui a minha identidade
Refatore o código a seguir de modo a remover as variáveis `sobrenomeTratado` e `nomeDoMeioTratado`.

``` javascript
function imprimeNomeCompleto(nomeTratado, sobrenome, nomeDoMeio) {
  let nomeTratado = nomeTratado || '';
  let sobrenomeTratado = sobrenome || '';
  let nomeDoMeioTratado = nomeDoMeio || '';

  console.log(`${nomeTratado} ${nomeDoMeioTratado} ${sobrenomeTratado}`);
}

imprimeNomeCompleto('João'); // João
```

## Exercício 4 - Adivinha em quem eu estou pensando?
Considere o código a seguir e responda: Qual o valor será mostrado? E por que?

``` javascript
const v = 'valor 1';
function funcao(x = v) {
  const v = 'valor 2';
  console.log(x);
}

funcao(); // qual valor será mostrado?
```

## Exercício 5 - Pare de me imitar!
Como podemos tornar o código abaixo menos repetitivo?

``` javascript
function subtrair(a = 0,b = 0) {
  return a + b;
}
```
