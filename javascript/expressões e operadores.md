## Operadores relacionais
Um operador relacional compara seus operandos e retorna um valor booleano dependendo se a operação for verdadeira ou falsa
#### in
usamos o operador in para verificar se algo está presente dentro de outra coisa, assim, ele nos retornará um valor booleano indicando se está ou não presente:
```
nomePropriedadeOuNumero in nomeObjeto;
```
- Nesse exemplo estamos verificando se uma propriedade ou índice existe dentro de um objeto ou de um array, nesse caso um objeto de nome "nomeObjeto"

#### instanceof
O operador instanceof retorna verdadeiro se o objeto especificado for do tipo de outro objeto especificado e false se ele não for. sua sintaxe é:
```
nomeObjeto instanceof tipoObjeto
```
- "nomeObjeto" é o objeto que será comparado com "tipoObjeto" e "tipoObjeto" é um tipo de objeto que vamos perguntar se "nomeObjeto" é igual.


## Operadores bitwise ou bit a bit
Os operadores bitwise tratam seus operandos como um conjunto de 32bits em vez de tratá-los como números decimais, ou etc. 
Os operadores bitwise podem ser resumidos da seguinte forma:


|                    Operador                    | Expressão | Descrição                                                                                                                |
| :--------------------------------------------: | :-------: | ------------------------------------------------------------------------------------------------------------------------ |
|                      AND                       |   a & b   | Retorna 1 para cada posição que os bits da posição correspondente de ambos operadores sejam uns                          |
|                       OR                       |  a \| b   | Retorna um 0 para cada posição em que os bits da posição correspondente de ambos os operandos sejam zeros.               |
|                      XOR                       |   a ^ b   | Retorna 0 para cada posição em que os bits da posição correspondente são os mesmos e 1 para diferentes                   |
|                      NOT                       |    ~ a    | Inverte os bits do operando                                                                                              |
|            Deslocamento a esquerda             |  a << b   | Desloca `a` em representação binária `b` bits à direita, descartando bits excedentes.                                    |
| Deslocamento a direita com propagação de sinal |  a >> b   | Desloca `a` em representação binária `b` bits a direita descartando bits excedentes.                                     |
| Deslocamento a direita com preenchimento zero  |  a >>> b  | Desloca `a` em representação binária `b` bits a direita, descartando bits excedentes e preenchendo com zeros à esquerda. |


## Operadores de bigint 
A maioria dos operadores que fucionam nos numbers podem ser utilizados também nos bigint. 