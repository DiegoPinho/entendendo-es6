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

## Exercício 3 -
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
