# Gabarito

## Exercício 1 - Desestruturando a definição
**R:** Resumidamente, podemos definir o desestruturamento como uma maneira de extrair valores armazenados em objetos e Arrays. A sua ideia é permitir que usemos a mesma sintaxe de construção de dados para extrair dados.

## Exercício 2 - Pegando a propriedade na lata
``` javascript
const {email, nome, idade} = usuario;
```

## Exercício 3 - Não gostei desse nome não
``` javascript
const usuario = {
  nome: 'Toreto',
  email: 'velozesefuriososparasempre@gmail.com'
}

const {nome:nick, email:login} = usuario;

console.log(nick); // Toreto
console.log(login); // velozesefuriososparasempre@gmail.com
```
