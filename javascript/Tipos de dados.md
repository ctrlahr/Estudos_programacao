
## Tipos primitivos

#### number
Os tipos primitivos number são aqueles que não números então por exemplo, 1, 54, 4.16. Todos esses são considerados pelo javascript como numbers e diferentemente de outras linguagens o javascript não separa números decimais de inteiros então não temos por exemplo o tipo float/double como seria em outras linguagens.

#### string
São cadeias de caracteres, ou seja, nomes, CPF, números de telefone, etc. Podem ser representadas com aspas simples, duplas ou até mesmo com crase. No javascript não há diferença entre o uso de aspas simples ou duplas mas entre crase há. Somente com o uso da crase e do `${}` nós conseguimos realizar uma interpolação.
#### undefined
O undefined é basicamente o tipo que se refere a quando algo não está definido representa uma variável que foi criada mas não inicializada. Então por exemplo quando criamos uma variavel assim `var nome;` essa variavel não recebeu valor eu apenas defini ela. Nesse caso, se fosse executado o comando `console.log` e como parâmetro passarmos a variavel nome seria retornado "undefined" pois apenas criamos uma variavel mas não demos valor a mesma. Isso acontece também quando o hoisting é utilizado já que ele apenas move a declaração da variavel para o escopo acima.
#### null
O tipo null é frequentemente utilizado quando queremos criar uma variavel e atribuir um valor a ela só depois no código já que em muitas vezes inicializar a variável é de extrema importância para o funcionamento do código então com o uso do null podemos inicializar aquela variavel e darmos um valor a ela só quando for necessário no código. Ou seja, o null é utilizado para representar a ausência de valor, a falta de algo.
#### boolean
São representados a partir de true ou false, são tipos lógicos podendo ser ou verdadeiros ou falso. Por exemplo se perguntarmos ao computador se 5 é maior que 4 ele retornaria true assim como se perguntarmos se 5 é maior que 6 ele retornaria false.

#### bigint
Um bigint é um valor introduzido recentemente ao javascript e ele basicamente se refere a numeros muito grandes dentro do javascript. Ele é representado pela letra "n" no final do número. Então por exemplo:
`var num = 239540798305722097435209743590823749805273407509274359082437509872n`
essa variável é um bigint pois ela apresenta o "n" no final do número gigante. Esse tipo é utilizado quando queremos fazer cálculos entre números muito grandes já que se fosse feito esse mesmo cálculo com números inteiros o resultado apareceria de forma errada.

#### symbol
Symbols são basicamente um tipo primitivo que armazenam um valor único na memória. Ou seja, mesmo se criarmos symbols de valor idêntico, quando formos comparar eles terão valor diferente:
```
let sym1 = Symbol()
let sym2 = Symbol()

console.log(sym1 == sym2)// Retornará false
```

Para declararmos um symbol basta apenas utilizarmos a função `Symbol()` e passar uma descrição opcional se quisermos, sendo muito utilizado apenas para auxiliar o programador na hora de se debugar o código.
Um valor symbol apenas é igual a outro valor se seu identificador for o mesmo, então, se no exemplo dado acima tivéssemos passado algum identificador para esses symbols nós o valor retornado seria true. 
Para podermos retornar a chave, o registrador de um symbol podemos usar o método:
```
Symbol.KeyFor(nome_do_symbol)
```

#### Object
Os objetos são estruturas de dados complexas que podem conter várias propriedades e métodos. Eles são fundamentais em JavaScript. Um exemplo de um objeto podemos citar os maps:
```
let pessoa = {
	nome: "jorge",
	idade: 17,
	cidade: "Afogados Da Ingazeira"
}
```

