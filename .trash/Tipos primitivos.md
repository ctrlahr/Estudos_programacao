## inteiros
existem outros tipos dentro dos números inteiros, são eles o tipo byte, short, int e long, eles ocupam diferentes espaços na memória e armazenam em intervalos igualmente diferentes.

| Tipo  | Intervalo                                              | bits na memória |
| ----- | ------------------------------------------------------ | --------------- |
| byte  | -128 - 127                                             | 8 bits          |
| short | -32.768 - 32.767                                       | 16 bits         |
| int   | -2.247.483.649 - 2.147.483.647                         | 32 bits         |
| long  | -9.223.372.036.854.775.808 - 9.223.372.036.854.775.807 | 64 bits         |
- O tipo long precisa terminar com um "L" para definir que é um número do tipo long.

## Números decimais
No java existem dois tipos diferentes para armazenar números decimais, são eles o float e o double. Nesse caso os tipos se diferenciam principalmente pela precisão, sendo a precisão do tipo float simples e a do tipo double dupla, essa precisão se dá devido a quantidade de números que cada um tem a capacidade de armazenar após o ponto:

| Tipo   | Precisão         | Bits na memória |
| ------ | ---------------- | --------------- |
| float  | precisão simples | 32 bits         |
| double | precisão dupla   | 64 bits         |
- O tipo float necessita de um f no final do número para definir como um float.

## Stings
As stings armazenam palavras e frases, são utilizadas aspas duplas. Vale citar que ao utilizar o tipo String ele deverá estar escrito com "S" maiúsculo pois no java o tipo string não é um tipo primitivo como os outros mais sim uma classe interna.

## Char
O tipo char armazena apenas um único caractere, então frases não podem ser atribuídas a uma variável de tipo char por ela apenas suporta caracteres únicos como "a", "b", "c", etc.
Além de que chars devem ser representados com aspas simples.

## Boolean
O tipo booleano apenas armazena True ou false.