
## Estrutura For
O for é uma estrutura de repetição definido ou seja, nós vamos fazer uso dela quando tivermos noção sobre a quantidade de vezes que vamos ter que iterar sobre algo. A sintaxe do for dentro do javascript é a seguinte:
```
for(ini;condicao;cont) {
	...
}
```
- Sendo `ini` a inicialização de uma variável temporária que será incrementada
- `condicao` sendo oque vai avalizar basicamente se o loop continuará em execução
- `cont` sendo basicamente o controle, onde vamos por exemplo aumentar o valor da variável de controle ou diminuir.
Um exemplo:
```
for(let i = 0; i < 10; i++) {
	console.log(i)
}
```

Também é possivel omitir as informações em uma estrutura for mas temos que em algum momento colocar um break para o código não ficar rodando infinitamente:
```
var i = 0
for(;;) {
	if (i > 3) break
	console.log(i)
	i++
}
```

Em resumo o for é uma estrutura que continua a realizar sua iteração enquanto a condição passada for verdadeira, enquanto a condição retornar um true.

## Estrutura for in
O for in é utilizado por exemplo para quando queremos iterar sobre os elementos de um array, sua sintaxe é assim:
```
for(i in num) {
	console.log(num[i])
}
```
Podemos traduzir como, para cada elemento na variavel/lista passada faça isso. 
Fuciona basicamente como o for in do python também.


## Estrutura for of
O for of ele itera diretamente sobre os elementos de uma coleção, então digamos que nós temos um array com os numeros 10, 20, 30 e 40. Se fossemos utilizar o for in para printar os elementos desse array teríamos que passar como parâmetro a nossa variável temporária como índice dessa lista: `console.log(num[i])`, já com o for of nós basicamente já estamos acessando os elementos daquela lista então precisaríamos só passar o nome da nossa variável temporária:
```
for(n of num) {
	console.log(n)
}
```
Podemos traduzir essa estrutura como para cada elemento dessa variavel faça isso.

Podemos também iterar sobre até mesmo uma string, dessa forma:
```
let nome = 'jorge'
for(letra in jorge) {
	console.log(letra)
} 
// Saida:
j
o
r
g
e
```


## Estrutura while
A estrutura de repetição while é uma estrutura de loop indefinido pois iremos utilizar quando não temos ciência da quantidade de vezes que vamos ter que iterar, repetir, aquela tal coisa.
Pode ser traduzido para, enquanto essa condição passada for verdadeira ele vai executar essa estrutura de comandos que foi passada, se essa condição por falsa ele vai sair e finalizar a iteração do nosso programa. 
A sintaxe básica do while é assim por exemplo:
```
let n = 0
while(n < 10) {
	console.log(n)
	n++
}
```

Para criarmos um loop infinito basta colocarmos um true, ou seja, "enquanto verdadeiro executar isso":
```
while(true) {
	console.log(n)
	n++
}
```


## Estrutura "do while"
Assim como o while, o do while irá executar enquanto a condição passada for verdadeira e também é uma estrutura de loop indefinida.
Basicamente as diferenças do "do while" para o "while" são as seguintes:
- No while a primeira coisa que fazemos é o teste lógico e no "do while" nós primeiro executamos os códigos
- No "do while" nós temos a garantia que o bloco irá ser executado pelo menos uma vez se a condição imposta não for verdadeira, diferentemente do "while" pois se a condição se mostrar falsa no "while" logo que a iteração começar ele já pula para fora e não executa o bloco de comandos passados depois.


A estrutura do "do while" é assim:
```
do {
	...
} while(expressão_lógica)
```
Podemos traduzir para por exemplo, faça isso enquanto isso for verdadeiro.

## Estrutura break 
O break é uma expressão que gera uma interrupção em uma execução, ou seja, ele encerra aquela iteração que estava sendo feita.
Por exemplo:
```
let n = 0
let max = 1000
while(n < max) {
	console.log(n)
	if(n > 10) {
		break
	}
	n++
}
console.log('Fim do programa')
```
- Nessa estrutura quando a variável n tiver um valor maior que 10 ele irá encerrar aquela interação, ou seja, ele vai sair daquele laço de repetição então irá finalmente executar o ultimo código que printa "fim do programa".


## Estrutura continue
Quando executado dentro de um loop ele para somente aquela iteração e pula para a próxima, ou seja, ele continua naquele loop somente cancela a iteração corrente.
Temos como exemplo:
```
let n = 0
let max = 1000
let pares = 0
for(;n < max; n++) {
	if(n % 2 != 0) {
		continue
	}
	pares++
}
console.log(`Quantidade de pares ${pares}`) // Saida: 500
console.log('Fim do programa')
```
- Basicamente oque acontece nessa estrutura é que nós falamos no if que se o resto da divisão da variável n por 2 for diferente de 0 nós vamos continuar para a próxima iteração, ou seja, não vamos executar os códigos que estiverem abaixo.

## Utilização da label com break ou continue
Nós podemos utilizar a label junto com o break ou com o continue para garantir um controle a mais do nosso código, e é bastante simples o seu uso, sendo assim:
```
let i, j;

loop1: for (i = 0; i < 3; i++) {
  //O primeiro 'for' é etiquetado com "loop1"
  loop2: for (j = 0; j < 3; j++) {
    //O segundo é etiquetado com "loop2"
    if (i == 1 && j == 1) {
      continue loop1;
    } else {
      console.log("i = " + i + ", j = " + j);
    }
  }
}
```
- Basicamente oque fazemos aqui é indicando exatamente qual o loop que queremos que continue. 

Exemplo com break:
```
let allPass = true;
let i, j;
top: for (i = 0; items.length; i++)
  for (j = 0; j < tests.length; i++)
    if (!tests[j].pass(items[i])) {
      allPass = false;
      break top;
    }
```