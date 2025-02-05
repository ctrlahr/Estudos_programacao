
##### Imprimir algo na tela
para imprimirmos algo no terminal utilizamos o comando `puts` e utilizado tanto aspas simples como aspas duplas, dessa forma:
```
puts 'Hello world!'
```

##### Input no terminal
Para conseguir abrir uma caixa de texto no terminal em ruby nós temos que criar uma variavel para armazenar a resposta que for dada e como valor para essa variavel nós darmos a função `gets`, dessa forma por exemplo:
```
puts "qual o seu nome?"
nome = gets
print "olá #{nome}"
```


##### Estrutura de dados
No ruby nós temos apenas dois tipos de estrutura de dados sendo eles o Array e o hash.

###### Array
No Ruby, uma estrutura de dado `Array` é uma coleção ordenada de elementos, que pode conter diferentes tipos de dados, como inteiros, strings, ou até mesmo outros arrays. Para criarmos um array nós podemos ou já definir um array e o atribuirmos a uma variavel depois com a função `Array.new` ou já atribuir a uma variavel, assim: `meu_array = [...]`

###### Métodos de um Array
- `append` - Adiciona um item ao final da lista de um Array
- `.sort` - Ordena os itens de um Array
- `.reverse` - Reverte a ordem dos itens de um Array
- `<<` - Adiciona novos elementos a um Array ao final da lista
- `.uniq` - Remove todos os elementos duplicados
- `.count` - Retorna a quantidade de elementos de um Array

###### Hash
Uma estrutura de dado de tipo hash é muito parecida com um Array, entretanto ela além de utilizar as {} ele necessita de uma chave e um valor. Como um dicionário no python por exemplo. Ele fuciona assim:
```
meu_hash = {primeiro_nome: "jorge", ultimo_nome: "bento"}
```

###### Métodos de um hash
- `.keys` - Retorna um Array com todas as chaves de um hash
- `.values` - Retorna todos os valores de um hash
- `.count` - Retorna a quantidade de elementos presentes em um hash

###### Observações sobre o hash
- Para passarmos uma chave de um hash para por exemplo printar essa chave nós precisamos passar ela como um valor symbol ou seja com os ":" na frente então por exemplo acima que temos o hash "meu_hash" se nós quiséssemos mostrar a chave "primeiro_nome" nós teríamos que fazer assim: `puts meu_hash[:primeiro_nome]`


##### Tipos de dados 
###### Symbol
Um valor symbol é um tipo de dado que se parece com uma string entretanto ele apresenta algumas distinções como por exemplo
- ele é representado sempre com ":" antes, assim por exemplo: `:alguma_coisa`
- Não são permitidas concatenações nem interpolações com symbols 
- são imutáveis

###### nil
nil é o tipo de dado que representa o tipo nulo, ou seja. Que representa a ausência de algo, a ausência de um valor, conteúdo. Por exemplo, se estivermos falando para o código nos falar oque está no índice 3 da variavel que está armazenando "eae" ele irá retornar nil. Assim:
```
palavra = "eae"
puts palavra[3] => nil 
```


##### Formas de formatação/coisas uteis 


- `.upcase` - Retorna a string em letras maiúsculas
- `.capitalize` - Retorna a string com a primeira letra maiúscula
- `.size` - Conta a quantidade de letras que há na string contando com os espaços
- `.delete("...")` - Remove todas as ocorrências da letra que foi informada. Por exemplo, na palavra rio se eu usar o `.delete` e passar como parâmetro a letra "o" o que vai ser retornado será "ri" pois nós retiramos as ocorrências de "o"
- `.gsub("...", "...")` - Substitui todas as ocorrências do que for informado pelo outro parâmetro informado
- `.to_i` - Converte uma string em um número inteiro
- `to_f` - Converte uma String em um número float
- `.between?(...)` - verifica se a variavel ou oq for passado está entre os parâmetros passados
- `.class` - Retorna o tipo de dado de algo(String, int, etc.)
- `\n` - é uma quebra de linha
- `\` - é utilizada para informar ao ruby que por exemplo as aspas dentro de uma string são literais, mas pode ser utilizado para informar que qualquer caractere especial é um caractere literal. Ou seja, nós não estamos fechando a string. Assim: `"meu nome é \"Jorge luís""`
- `<<` é utilizado para adicionarmos mais alguma coisa a uma string, então por exemplo. Se temos uma variavel de nome "var" que está armazenando "oi" e fizermos `var << " mano"` essa variavel terá valor de `oi mano`
- `rand(...)` - Usado para a randomização de um numero. Se for usado só sem passar nada, nenhum parâmetro ele apenas gera um número aleatório mas se for dado limites como por exemplo entre 1 e 5(`rand(1..5`) ele gera um número de 1 a 5 por exemplo,

##### Interpolação no ruby
Uma interpolação é basicamente oque no python nós fazemos com o "f" antes da string e colocando `${...}`, basicamente é uma forma de juntar elementos em uma string e ela no ruby é utilizada por meio do `#{...}` por exemplo:
```
curso = programação
"curso de #{curso}"

# Saida:
curso de programação
```

##### Diferença de aspas simples para aspas duplas
- As aspas simples não suportam  carácteres especiais. Então por exemplo, se nós quisermos imprimir algo na tela e quisermos colocar uma quebra de linha nessa String ou até mesmo fazer uma interpolação temos que utilizar as aspas duplas pois se forem utilizadas as simples o `/n` da quebra de linha por exemplo ficaria a mostra e não cumpriria com sua função

##### Criação de variáveis
 As variáveis são definidas de forma dinâmica, ou seja. nós não precisamos informar na hora de criar uma variavel se ela é um número, uma string, etc. Para criarmos uma variavel nós falamos o nome dela e passamos oque ela vai receber, da mesma forma que no python. assim:
```
profissao = "programador"
# ou então
resposta = 42
```


##### Condicionais 

###### if
A condicional if no ruby é escrita de forma facil, assim:
```
if num == 1
	puts "oi"
```

###### elsif
Elsif é uma condição no ruby que fuciona como o elif no python ou como o elseif no dart. basicamente fuciona para darmos uma condição a mais ao nosso código e ela também é facilmente utilizada. Assim por exemplo:
```
elsif num == 2
	puts "olá"
```

###### else
O else fuciona como os else's de outras linguagens também, diz uma coisa pra acontecer se as condições acima não se mostrarem verdadeiras
```
else
	puts "caraca, eae"
```

###### case e when
O case e o when podem ser utilizados para meio que substituir o if e elsif elas podem ser traduzidas como caso isso, quando for assim faça isso, quando for isso faça isso. E ela também pode ser usada junto do else dessa forma por exemplo:
```
case num
when == 1
	puts "oi"
when == 2
	puts "olá"
else
	puts "caraca, eae"
end
```

##### laços de repetição

###### for
A estrutura for é utilizada quando temos um limite da repetição, por exemplo, queremos imprimir o numero 10,  5 vezes, ai utilizamos ele, assim por exemplo:
```
for x in 5
	puts 10
end
```

###### while
Diferentemente do for o while nós utilizamos quando queremos criar um loop mas não sabemos o limite desse loop, por exemplo se quisermos imprimir um número e acrescentar um a mais a esse número até ele se tornar 10, podemos utilizar o while. Dessa forma:
```
while num != 10
	num += 1
	puts num
end
```


###### until
O bloco de código associado a ela só é executado a menos que determinada condição seja satisfeita, ou seja, para que o código seja executado é necessário que a condição retorne _false_ por exemplo para checarmos se um usuário digitou um numero entre 1 e 5 como foi pedido, se ele não fez isso o loop continuará até ele informar um número que está entre 1 e 5. Assim: 
````
until resposta.between(1, 5)
	print("por favor digite novamente o número de 1 a 5")
	resposta = gets.to_i
```