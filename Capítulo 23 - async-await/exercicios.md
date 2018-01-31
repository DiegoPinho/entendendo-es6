# Exercícios

Nestes exercícios vamos rever como funcionam as novidades trazidas pelo ES8 (ES2017) com o async/await.

## Exercício 1 - Await a second!
O que acontece quando tentamos utilizar o `await` em uma Promise fora de uma função marcada com `async`?

## Exercício 2 - Tire esse then da minha frente!
Refatore a função a seguir para funcionar utilizando async/await.

``` javascript
function showGitHubUser(username) {
	const url = `https://api.github.com/users/${username}`;
	fetch(url)
		.then(response => response.json())
		.then(user => {
			console.log(user);
		})
}
```

## Exercício 3 - Na minha máquina funciona...
Como fazemos para tratar erros quando estamos trabalhando com async/await? Refatore o código do exercício anterior para lidar com estes casos.

## Exercício 4 - Cuidado com a concorrência
Refatore o código a seguir para deixar as requisições paralelas utilizando o `Promise.all`.

``` javascript
async function showGitHubUserAndRepos(username) {
  const userPromise = fetchFromGitHub(`/users/${username}`);
	const reposPromise = fetchFromGitHub(`/repos/${username}`);
  
	const user = await userPromise;
	const repos = await reposPromise;
	
	console.log(user.name);
	console.log(respos.length);
}
```

## Exercício 5 - Nunca é tarde demais para mudar
Refatore o código a seguir para que ao invés de usar callbacks, ele funcione com Promises e usando a sintaxe de async/await.

``` javascript
function doSomething(callback) {
  console.log('i did something');
  callback();
}

doSomething(function(){
  console.log('i did something AFTER!');
})
```