
## Global
O escopo global basicamente se refere a variáveis que tem acesso global, ou seja, por todo o código. Uma variável declarada com "var" ela tem escopo global, em qualquer local do código 
você terá acesso a essa variável, podendo chamar ela ou fazer oque vc quiser e precisar:
```
var teste = "eae"
function ola {
	console.log("eae")
}

console.log(teste)
```

## Function
Um escopo de function é basicamente tudo que está presente dentro de uma função, pontos que a diferencia do escopo block é que por exemplo ao criar uma variável com var o escopo de function é respeitado porém o de block não, então tudo que estiver dentro de uma função está dentro do escopo de function:
```
function minha_funcao {
	let nome = "Jorge"
}
console.log(nome)// Retornará o erro undefined pois, a variável nome foi definida dentro do escopo function e só existe dentro daquele escopo
```

## Block
O escopo block é referente a por exemplo, condicionais, laços de repetição, try, catch, etc. Esse escopo foi adicionado na versão do EcmaScript 6 (ES6) junto das formas de declaração de variáveis let e const que respeitam esse escopo de block:
```
vezes = 4
if (vezes > 5) {
	let ola = "Olá, mundo!"
}
console.log(ola)// Retornará um erro pois estamos definindo uma variável dentro de um escopo de block.
```