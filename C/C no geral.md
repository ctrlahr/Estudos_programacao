C foi uma linguagem que foi criada com o intuito de facilitar a comunicação com o processador pois a mais utilizada na época era o assembly e cada processador tinha uma versão diferente de assembly, com divergências entre elas.

C foi uma das primeiras linguagens de alto nível.

A linguagem C é muito utilizada em sistemas operacionais, sistemas desktop, sistemas embarcados, telecomunicações e até mesmo alguns sistemas web no backend usufruindo do web assembly.

C é uma linguagem compilada, isso faz com que C seja mais rápido que linguagens interpretadas como python.

C não tem suporte a orientação a objetos, somente o C++.

A biblioteca stdio vai estar em praticamente todos os programas pois é ela que faz com que o usuário entenda o que está acontecendo com o programa, Como por exemplo, até o próprio `printf()` faz parte dessa biblioteca.

C é uma linguagem que no final de uma linha de código é necessário um `;` para indicar que aquela linha finalizou.

### Especificadores de formato do scanf:

![[Pasted image 20250226201607.png]]

A função `scanf()` é uma função que é utilizada para capturar entradas do teclado do usuário, ela deve ser utilizada de forma semelhante ao `printf()`:
```
int idade = 0;

printf("Digite uma idade");
scanf("%d", &idade)
```
- Primeiro criamos uma variável que vai armazenar os valores recebidos pela função scanf. 
- Depois é utilizado do `printf()` para informar ao usuário o que deve ser escrito
- E por ultimo é utilizada do `scanf()` Para ler os dados, entre aspas duplas precisa ser informado o especificador de formato, então, se o valor que será lido é um valor inteiro o especificador de formato será o `%d` já que ele é referente ao tipo de dado inteiro. Depois precisamos passar em qual variável que será armazenado o valor lido junto de um "&"(e comercial).


## Operadores

![[Pasted image 20250304130423.png]]

![[Pasted image 20250304133431.png]]

![[Pasted image 20250304140110.png]]


![[Pasted image 20250304140653.png]]


