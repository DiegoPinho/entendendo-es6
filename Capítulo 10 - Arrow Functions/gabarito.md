# Gabarito

## Exercício 1 - Hora de usar as setas
``` javascript
let imprimeProduto = (nome,preco) => {
  console.log(`Produto: ${nome} | Preço: ${preco}`);
};
```

## Exercício 2 - Hora de usar as setas novamente
``` javascript
let itens = ['abacaxi', 'banana', 'maçã', 'laranja', 'limão'];
itens.forEach(item => console.log(item));
```

## Exercício 3 - Quem está na janela?
R: Sempre que executamos uma função no JavaScript, ela é associada a um contexto de execução. Esse contexto possui uma propriedade denominada ThisBinding, que pode ser acessada a qualquer momento através da palavra reservada this. O valor do this, que chamamos de contexto da função, é constante e existe enquanto este contexto de execução existir. Toda função também declarada no escopo global possui o objeto window como valor do this.

## Exercício 4 - Vou lavar sua boca com sabão!
``` javascript
let palavroes = [
    "Inconstitucionalíssimo",
    "Otorrinolaringologista",
    "Pneumoultramicroscopicossilicovulcanoconiose",
    "Oftalmotorrinolaringologista"
];

let tamanhos = palavroes.map(palavrao => palavrao.length);

console.log(tamanhos); // [ 22, 22, 44, 28 ]
```

## Exercício 5 - Tudo dentro do seu escopo
``` javascript
const equipe = {
    nome: 'Valentes da Glória',
    membros: ['Luciano', 'Maria', 'Virgínia', 'Daniela'],
    imprimeNomes: function() {
        this.membros.forEach(membro => {
            console.log(`${membro} é da equipe ${this.nome}`);
        })
    }
}

equipe.imprimeNomes();
```
