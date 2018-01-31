# Gabarito

## Exercício 1 - Await a second!
**R:** Simplesmente não funciona. O `await` precisa estar sempre envolta de uma função marcada com a palavra `async`.

## Exercício 2 - Tire esse then da minha frente!
``` javascript
async function showGitHubUser(username) {
	const url = `https://api.github.com/users/${username}`;
	const response = await fetch(url);
	const user = await response.json();
	console.log(user);
}
```

## Exercício 3 - Na minha máquina funciona...
**R:** É necessário encapsular o código dentro de um try/catch. Para o caso do exercício anterior, o código ficaria assim:

``` javascript
async function showGitHubUser(username) {
	try {
    const url = `https://api.github.com/users/${username}`;
	  const response = await fetch(url);
	  const user = await response.json();
	  console.log(user);
  } catch(err) {
    // Se a promise for rejeitada por algum motivo, este fluxo será executado
    console.log(err);
  }
}
```

## Exercício 4 - Cuidado com a concorrência
``` javascript
async function showGitHubUserAndRepos(username) {
  const [user, repos] = await Promise.all([
    fetchFromGitHub(`/users/${username}`),
    fetchFromGitHub(`/users/${username}/repos`)
  ]);
	
	console.log(user.name);
	console.log(respos.length);
}
```

## Exercício 5 - Nunca é tarde demais para mudar
``` javascript
function doSomethingPromisefy() {
  return new Promise((resolve, reject) => {
    resolve(console.log('i did something'));
  })
}

(async () => {
  await doSomethingPromisefy();
  console.log('i did something AFTER!');
})();
```
