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

## Exercício 4 - Minha mãe mandou eu escolher esse daqui...
``` javascript
const [,reinalda] = contatos;
console.log(reinalda); // {nome: 'Reinalda Silva', numero: '1234-6789'}
```

## Exercício 5 - Cara-Crachá
``` javascript
function isEngenheiro({titulo, departamento}) {
  return titulo.indexOf("Engenheiro") > -1 && departamento === 'Engenharia';
}
```

## Exercício 6 - Mas o que são estes dados!?
``` javascript
const corpoDocente = [
  [ 'Gramática', '9:00', 'Sueli' ],
  [ 'Matemática', '10:15', 'Amilton'],
  [ 'Educação Física', '11:30', 'Bruno' ]
];

function mostraGradeProfessores(corpoDocente) {
  return corpoDocente.forEach( ([materia, hora, nome]) => {
    console.log(`Aula de ${materia} às ${hora} com professor(a) ${nome}`);
  });
}
```
