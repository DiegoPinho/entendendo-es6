# Gabarito

## Exercício 1 - Meu primeiro módulozinho
- src/config.js

``` javascript
const nome = 'ECMAScript 6';
export default nome;
```
- index.js

``` javascript
import nome from './src/config';
console.log(nome);
```

## Exercício 2 - Um ou outro, mas não os dois!
- src/config.js

``` javascript
const nome = 'ECMAScript 6';
const chave = 'chave';
export default nome;
export {chave};
```

- index.js

``` javascript
import nome, {chave} from './src/config';

console.log(nome); // ECMAscript 6
console.log(chave); // chave
```

## Exercício 3 - Classe para todos
- src/telefone.js

``` javascript
class Telefone {
    constructor(modelo, numero){
        this.modelo = modelo;
        this.numero = numero;
    }
}

export default Telefone;
```

- index.js

``` javascript
import nome, {chave} from './src/config';
import Telefone from './src/telefone';

console.log(nome); // ECMAscript 6
console.log(chave); // chave

const tel = new Telefone('iphone', 971136132);
console.log(`numero: ${tel.numero} | modelo: ${tel.modelo}`);
```

## Exercício 4 - Trocando os nomes
- src/config.js

``` javascript
export const url = 'http://entendendoes6.com.br';
```

- index.js

``` javascript
import { url as link } from './src/config';

console.log(link); // http://entendendoes6.com.br
```

## Exercício 5 - Exportação de funções

- src/printer.js

``` javascript
export default function printNoConsole(mensagem) {
  console.log(mensagem);
}
```

- index.js

``` javascript
import printer from './src/printer';

printer('Olá, esta é uma mensagem!');
```
