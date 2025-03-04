
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