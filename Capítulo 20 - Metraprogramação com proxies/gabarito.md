# Gabarito

## Exercício 1 - Praticamenteo um sósia
**R:** Proxies são objetos que representam outros objetos e através da metaprogração conseguem interceptar e customizar operações fundamentais em objetos, como:
- Acessar e setar um propriedade (nova ou não)
- Enumerar e deletar propriedades

## Exercício 2 - Meta o quê?
**R:** Podemos nos arriscar a definir que a metaprogramação nada mais é que a programação de programas que manipulam a si mesmo e/ou a outros programas. Um metaprograma é todo programa que atua sobre ele mesmo ou outro, seja no formato fonte, binário ou em uma representação abstrata em memória.

## Exercício 3 - Sorria, você está sendo filmado
``` javascript
const livroProxy = new Proxy(Livro, {
  get(alvo, prop) {
    console.log(`${prop} foi acessada`);
    return alvo[prop];
  }
});

livroProxy.titulo; // titulo foi solicitado!
livroProxy.autor; // autor foi solicitado!
```

## Exercício 4 - Aqui você não seta nada!
``` javascript
const livroProxy = new Proxy(Livro, {
  get(alvo, prop) {
    console.log(`${prop} foi acessada`);
    return alvo[prop];
  },

  set(alvo, prop) {
    console.log(`${prop} foi setada`);
    return alvo[prop];
  }
});


livroProxy.titulo; // titulo foi solicitado!
livroProxy.autor; // autor foi solicitado!

livroProxy.titulo = 'ECMAScript 7'; // titulo foi setada!
```

## Exercício 5 - Só aceitamos dinheiro vivo
``` javascript
const validador = {
    set(Compras, propriedade, valor) {
        let valorAPagar = Compras.valorAPagar;
        console.log(valorAPagar);
        if(propriedade === 'valorPago' && valor < valorAPagar) {
            throw new TypeError('Valor insuficiente!');
        }

        Compras[propriedade] = valor;
    }
}

let comprasValidador = new Proxy({}, validador);
comprasValidador.valorAPagar = 100;
comprasValidador.valorPago = 10; // Valor insuficiente!
```

## Exercício 6 - Fim da farsa, Usurpadora!
``` javascript
const usurpadora = {
  get(PaolaBracho, propriedade) {
    if(propriedade === 'dinheiro' || propriedade === 'marido') {
      console.log('A Usurpadora está atacando!');
    }
  }
}

const {proxy:paola, revoke} = Proxy.revocable({}, usurpadora);
paola.dinheiro; // A Usurpadora está atacando!

revoke();

paola.marido; // TypeError: Cannot perform 'get' on a proxy that has been revoked
```
