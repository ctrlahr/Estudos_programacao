

## BigO
No Java Big O é utilizado para descrever a eficiência de um algorítimo, medindo a complexidade de um algorítimo, especificamente como o tempo de execução ou o uso de memória crescem à medida que o tamanho da entrada aumenta.
É uma notação que expressa a complexidade de uma algorítimo em termos de crescimento e descreve o comportamento do algorítimo conforme a entrada se torna cada vez maior.
Entre as notações de Big O temos, complexidade constante representada por `O(1)`, complexidade logarítmica representada por `O(log n)`.
Big O é principalmente uma medida de escalabilidade dos algorítimos servindo para medir a escalabilidade temporal e espacial dos algorítimos, sendo quase que uma forma de perguntar para o algorítimo se ele é escalável, se conforme a aplicação crescer ela vai se manter performática.

### Escalabilidade espacial


### Escalabilidade temporal




Abaixo estão as principais notações Big O:
![[Pasted image 20250721103857.png]]
#### Complexidade constante
Algorítimos de complexidade constante se referem a algorítimos que o tempo de execução ou o uso de memória não aumentam com o tamanho da entrada no programa. Então não importa quando o programa precise fazer, seu custo de memória e seu tempo para executar a ação não vão mudar.
Então tudo é executado em tempo e custo de memória fixo. Como exemplo tempos operações aritméticas simples; soma, subtração, divisão e multiplicação, verificar se um número é par ou impar,  entre outros.
Um outro exemplo é ao utilizar o método `get()` em [[Array list||array lists]], por que independentemente se a lista tiver uma quantidade exorbitante de itens ainda estará sendo procurado por um index específico. Assim, ele nunca vai depender do tamanho da lista.

#### Complexidade logarítmica


#### Complexidade linear
Algorítimos de complexidade linear sempre vão depender do tamanho da lista, se a lista for muito grande, dependendo de qual estrutura de dados estiver sendo utilizada, o algorítimo terá uma complexidade linear.
Então por exemplo:
Um for para iterar sobre os elementos de um [[Array list||array list]], printando cada um, esse algorítimo será de complexidade linear por que quanto mais o [[Array list||array list]] aumente de tamanho, ou seja, conforme novos elementos sejam adicionados a ele mais demorado será a execução desse algorítimo.

#### Complexidade linear-logarítmica


#### Complexidade quadrática
Um algorítimo de complexidade quadrática é por exemplo algorítimos com nested loops(Loops dentro de loops) se antes com um único `for` a complexidade era linear, com dois `for` a complexidade se torna quadrática por que ela está sendo dobrada.

#### Complexidade cúbica


#### Complexidade exponencial


#### Complexidade fatorial



Um bom exemplo é um for, a maioria dos loops for no java tem uma complexidade `O(n)` ou linear, por que o tempo de execução do loop aumenta proporcionalmente ao número de elementos que ele processa, então se uma lista precisa iterar sobre 2000 elementos o valor vai ser um mas se ela precisar iterar sobre 1 000 000 de elementos, ela terá outro tempo de execução, demorando mais para realizar toda a iteração.

O ideal é sempre buscar não ter algorítimos mas quando isso não se torna possível é bom sempre buscar algorítimos de complexidade constante ou `O(1)` por que eles são constantes então não importa a alteração que for feita, não vai mudar seu tempo de execução.