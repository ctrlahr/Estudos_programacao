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


