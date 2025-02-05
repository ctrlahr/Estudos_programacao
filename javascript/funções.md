Funções no javascript tem a seguinte sintaxe:
```
function nomeFuncao(parametros) {
	return alguma coisa
}
```


Os parâmetros de nossa função são por padrão quando você não cria os parâmetros, `undefined` mas nós podemos alterar isso passando parâmetros que essa função irá ler:
```
function param(parametro1, parametro2)
```

Esses parâmetros podem também ser parâmetros `rest` ou seja, parâmetros que podem ser mais de um valor, como listas, etc. com isso nós conseguimos passar por exemplo uma lista como parâmetro, por exemplo:
```
function soma(...num) {
	let res = 0
	let quantidade = num.length
	for(n of num) {
		res += n
	}
	return res
}
```


### Funções anônimas
Uma função anônima é basicamente uma função que não tem um nome então como ela não tem um nome nós precisamos associar ela a uma variável por exemplo, mas também poderia ser associada a uma chave de um map, etc.



Um exemplo com uma função anônima square(quadrado) associando a uma variável:
```
let square = function (numero) {
	return numero * numero
}
let x = square(4)
```

#### Arrow functions ou lambda functions
É uma forma de declaração de função de forma anônima, ou seja, sem dar um nome a função. Sua sintaxe é a seguinte:
```
let soma = (v1, v2) => {return v1 + v2}
```
É uma forma muito dinâmica de se criar uma função, onde apenas estamos falando que vamos passar oque está dentro dos parênteses para oque está dentro das chaves. 

Se nossa função precisar de apenas um parâmetro nós não precisamos colocar os parênteses:
```
let nome = n => {return n}
```

Com o uso das arrow functions nós também não precisaríamos necessariamente usar o `return` e as chaves, poderíamos escrever de uma forma ainda mais simplificada:
```
let add = n => n + 10
```