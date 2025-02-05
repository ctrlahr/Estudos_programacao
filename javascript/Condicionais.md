## if
A sintaxe básica do if é: 
```
if(condição) {
	oque será executado
}
```

também é possivel executarmos uma condicional if sem as chaves, dessa forma:
```
if(condição) executar aqui se for verdadeira
```

# else
A sintaxe básica do else é:
```
else {
	oque será executado
}
```

O else também pode ser executado sem as chaves, dessa forma:
```
else executar esse outro código
```

O else não é necessariamente obrigatório depois de um if, se o código não apresentar um else ele será executado sem erros:
```
if(num > 3) {
	console.log('isso é oq o if executa')
}
console.log('isso seria oq o else iria executar')
```

## else if
A sintaxe básica do else if é:
```
else if(condição) {
	oque será executado
}
```


## switch
As instruções switch são suas amigas aqui - elas tomam uma única expressão / valor como uma entrada e, em seguida, examinam várias opções até encontrarem um que corresponda a esse valor, executando o código correspondente que o acompanha.
Sua sintaxe é assim em pseudocódigo:
```
switch(expressão) {
	case escolha1:
		rode esse código
		break
	case escolha2:
		rode esse código então
		break
	// Inclua até a quantidade de casos que você precisar

	default:
		Por padrão, apenas execute esse código
}
```
- Usamos o switch e passamos uma expressão ou um valor dentro dos parênteses.
- para cada caso que pode acontecer nós adicionamos um `case` e um `break` ao final do caso.
- incluímos um valor default, ou seja, que será executado se nenhum dos casos acontecer.

Como exemplo de uma estrutura em código mesmo sem ser pseudocódigo nós temos:
```
let num = 1
switch(num) {
	case 1:
		console.log('1')
		break
	case 2:
		console.log('2')
		break
	case 3:
		console.log('3')
		break
	default:
		console.log('Não conseguimos ler seu número')
    
```