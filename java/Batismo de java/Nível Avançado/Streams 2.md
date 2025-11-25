O motivo de usar streams é para tornar o código menos verboso pois, ao converter por exemplo  uma lista para uma stream se torna menos verboso realizar algumas operações específicas por as streams já terem funções específicas. 
Então por exemplo, se é necessário realizar uma ordenação em uma lista, isso é bem menos trabalhoso e verboso ao transformar a lista em uma stream por streams já terem uma operação própria de ordenação.

Todo o esquema das streams funciona à partir de lambda functions, é necessário utiliza-las para por exemplo estar fazendo uma verificação de se algo começa com uma letra específica ou algo do tipo.

As streams as vezes podem até mesmo ser interpretadas com camadas, segue o código abaixo:
![[Pasted image 20251117213328.png]]

Nesse código está sendo feita uma filtragem para pegar apenas os elementos de uma lista que começam com "a" ou "b" para depois deixa-los maiúsculos.
Isso é feito com as streams quase como em camadas
- Na primeira camada é utilizado o `filter()` para estar filtrando apenas o desejado(Nesse caso pegar apenas as palavras que começam com "a" ou "b" dentro de uma lista)
- Na segunda camada é feito um mapeamento, ou seja, é transformado cada item da lista no que for informado que nesse caso é deixa-los em caixa alta.
- E por último, na terceira camada é utilizado o `forEach()` afim de pegar cada elemento da stream para executar algo, nesse caso é um print, mostrando assim todos os elementos da stream na tela.

Streams tem diferentes tipos de operações, são elas as operações intermediárias e terminais.

Operações intermediárias são aquelas que modificam algo da stream, elas são responsáveis por transformar a stream, então operações como o `filter()` ou o `map()` são operações intermediárias pelo fato de modificarem as streams 

Já as operações terminais são responsáveis para encerrar uma stream, operações terminais sempre estão no final de uma stream pois são responsáveis por justamente terminar uma stream.


Para selecionar especificamente um atributo de dentro de uma classe é necessário que a classe tenha um getter, assim ele poderá ser utilizado em conjunto com a operação map, dessa forma: 
![[Pasted image 20251124232051.png]]


## Operações intermediárias

*Distinct()*
A operação distinct é utilizada para realizar uma remoção de itens duplicados dentro de uma stream, garantindo que a stream possui apenas itens únicos.



## Operações finais 

*Reduce()*
A operação reduce resumidamente reduz toda uma stream a um único valor. Se for uma stream de int's, esse valor será um int, caso contrário pode ser um optional, por exemplo.

Essa operação tem uma sintaxe um pouco diferente, é necessário informar o valor inicial, o acumulador, o elemento e por fim a operação que deve ser feita.

Esse é um exemplo utilizado para somar todos os elementos de uma lista:
![[Pasted image 20251119224625.png]]
- Nesse caso o valor inicial foi de 0
- O acumulador a
- O elemento b
- E a operação, foi uma operação de soma entre a e b


*Limit()* 
A operação `Limit()` é utilizada para limitar o quanto será mostrado ou o quanto será armazenado a uma stream.
Ela pode ser utilizada, por exemplo, para fazer que de uma lista com 10 números, apenas os três primeiros sejam exibidos:
![[Pasted image 20251119230228.png]]




