

## Escopo estático
Static é tudo que pode ser acessado sem a necessidade de ser criado um objeto, ou seja, tudo que não é estático necessita que um objeto seja instanciado.
Justamente por isso que a função main de códigos java recebe o `Static`, dessa forma essa função pode ser criada sem antes ter sido instanciada.
É possível ter métodos estáticos dentro de classes comuns, um método estático em uma classe consegue ser chamado sem a necessidade da declaração de um objeto específico:
Na classe ninja:
![[Pasted image 20250709210027.png]]

Na classe main:
![[Pasted image 20250709210103.png]]

Então o método poderia ser acessado diretamente a partir da classe sem a necessidade de por exemplo um objeto `Sasuke` ser criado.


## Variáveis globais
Variáveis globais são variáveis que podem ser acessadas de qualquer local, elas devem ficar fora do escopo do método main 