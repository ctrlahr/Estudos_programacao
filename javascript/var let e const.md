
## Var
Usamos "var" quando queremos declarar uma variável da forma convencional, ou seja, ou globalmente ou em escopo de função. Quando queremos dar outro valor a uma variável já criada não precisamos escrever o var apenas o nome daquela variável e darmos um novo valor a ela. As variáveis podem ser ou de escopo global ou de escopo de função, ou seja, se uma variavel foi criada fora de uma função então ela é de escopo global, já se ela foi criada dentro de uma função ela é de escopo de função e só pode ser utilizada dentro daquela função.
```
var saudacoes = "Opa, eae" #Escopo global
function novaFuncao() {
	var ola = "olá" #Escopo de função
}
```

Por padrão se apenas escrevermos o nome da variável e passarmos seu valor sem atribuir "var" a ela o javascript tem por padrão que será uma var, então por exemplo:
```
ano = 2024
```
Nesse exemplo o javascript vai entender isso como uma criação de var.

##### Hoisting 
O hoisting no javascript acontece com variáveis e com funções, mas oque é o hoisting? 
Basicamente o hoisting é um mecanismo do javascript que faz com que todas as declarações de variáveis e de funções sejam movidas para o topo do seu escopo antes da execução do código, então por exemplo:
```
ola = "olá mundo"
console.log(ola)
var ola;
```
Nesse exemplo nós só estamos declarando a variavel "ola" depois de já darmos o valor a ela. Basicamente o javascript iria ver o código e executar o hoisting ou seja, ele iria colocar a declaração da variavel para o topo do seu escopo:
```
var ola;
ola = "olá mundo"
console.log(ola)
```

## Let
As maiores diferenças do "var", e do "let" são que por exemplo:
- O let ele tem escopo de bloco e o var não, ou seja, aquela variavel só poderá ser utilizada dentro do seu escopo.
- O let ele não pode ser declarado duas vezes, mas seu valor pode ser atualizado, então se escrevermos `let ola = ola` e mais para frente no código escrevermos de novo o `let ola = ola` um erro irá acontecer, justamente por que variáveis declaradas com let não podem ser declaradas novamente.
- O hoisting não fuciona em variáveis declaradas com o let

## Const
variáveis declaradas com const não podem ser alteradas nem atualizadas em nenhuma parte do código, ou seja, quando damos um valor a uma constante aquele valor só pode ser alterado na matriz daquela constante, ou seja, na sua declaração. Uma constante tem escopo de bloco, isso significa que quando uma constante é definida dentro de uma função por exemplo, ela só poderá ser utilizada dentro daquela mesma função. Sendo de grande importância quando queremos atribuir um valor fixo e que nunca vai mudar a algo.
```
const saudacoes = "olá mundo"
const saudadcoes = "olá" // Retornará um erro!
saudacoes = "eae" // Também retornará um erro!
```

Esse atributo das constantes, de ser imutável é quebrado quando falamos de objetos declarados com const. Ou seja, quando por exemplos definimos um dicionário com const.
```
const saudacoes = {
	palavras: "Olá",
	vezes: 4
}


// Isso não será possivel
Const saudacoes = {
	palaras: "eae",
	vezes: 5
} 


// Mas isso será:
saudacoes.palavras = "eae"
saudacoes.vezes = 
```
