

## BigO
No java Big O é utilizado para descrever a eficiência de um algorítimo, especificamente como o tempo de execução ou o uso de memória crescem à medida que o tamanho da entrada aumenta.
É uma notação que expressa a complexidade de uma algorítimo em termos de crescimento e descreve o comportamento do algorítimo conforme a entrada se torna cada vez maior.
Entre as notações de Big O temos, complexidade constante representada por `O(1)`, complexidade logarítmica representada por `O(log n)`.

Abaixo estão as principais notações Big O:
![[Pasted image 20250721103857.png]]
#### Complexidade constante
Algorítimos de complexidade constante se referem a algorítimos que o tempo de execução ou o uso de memória não aumentam com o tamanho da entrada no programa. Então não importa quando o programa precise fazer, seu custo de memória e seu tempo para executar a ação não vão mudar.
Então tudo é executado em tempo e custo de memória fixo. Como exemplo tempos operações aritméticas simples; soma, subtração, divisão e multiplicação, verificar se um número é par ou impar,  entre outros.

#### Complexidade logarítmica


#### Complexidade linear


#### Complexidade linear-logarítmica


#### Complexidade quadrática


#### Complexidade cúbica


#### Complexidade exponencial


#### Complexidade fatorial



Um bom exemplo é um for, a maioria dos loops for no java tem uma complexidade `O(n)` ou linear, por que o tempo de execução do loop aumenta proporcionalmente ao número de elementos que ele processa, então se uma lista precisa iterar sobre 2000 elementos o valor vai ser um mas se ela precisar iterar sobre 1 000 000 de elementos, ela terá outro tempo de execução, demorando mais para realizar toda a iteração.

O ideal é sempre buscar não ter algorítimos mas quando isso não se torna possível é bom sempre buscar algorítimos de complexidade constante ou `O(1)` por que eles são constantes então não importa a alteração que for feita, não vai mudar seu tempo de execução.