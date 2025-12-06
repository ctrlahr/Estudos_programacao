Threads no java são blocos de código que conseguem estar sendo executados de forma paralela ou quase paralela ao resto do código. Basicamente com as threads é possível executar múltiplas tarefas simultaneamente.
Todo o código java que é escrito roda dentro de uma thread principal, sendo ela chamada de "main thread" mas é possível criar threads adicionais, dessa forma, executando simultaneamente outros blocos de código.

Entretanto, threads podem acontecer de duas formas diferente e isso depende exclusivamente da máquina em que elas estão rodando. É aí que entra o paralelismo x concorrência:

*Paralelismo X concorrência:*
Se o computador que a thread está sendo executada tem múltiplos núcleos de processador então as threads serão executadas de forma simultânea, com cada núcleo processando uma thread diferente ao mesmo tempo.
Se o caso não é esse e na verdade o computador que está sendo executada a thread tem menos núcleos que  threads então entra o conceito de concorrência, basicamente o sistema operacional alterna rapidamente entre as diferentes threads dando a cada uma um pequeno intervalo de tempo de processamento, isso faz parecer que está sendo executado de forma simultânea, mas na verdade não está.


Existem algumas formas de se criar uma thread as principais são 
Estendendo da classe thread durante a criação de uma classe.
Implementando a interface `runnable` 
Ou de uma forma que não precisa criar uma classe é colocando dentro de um método lambda.


*Estendendo da classe thread:*
![[Pasted image 20251204223132.png]]

![[Pasted image 20251204223146.png]]

Dessa forma apenas é necessário criar uma classe que vai estender a classe threads, dentro dessa classe tem o que deve ser executado simultaneamente pela thread.


*Implementando a interface runnable:*
![[Pasted image 20251204223631.png]]

![[Pasted image 20251204223854.png]]

Nesse caso a criação do objeto é um pouco diferente, é necessário declarar aquele objeto como uma thread. Por padrão, ao implementar a interface `Runnable` a única coisa que vem é uma função run como pode ser visto no código da interface:
![[Pasted image 20251204224030.png]]

então se o objeto for criado da mesma forma que anteriormente(Na implementação pela classe thread) funcionaria mas o código estaria sendo executado ainda na thread main e não em uma separada e de forma simultânea.
Para realmente fazer uma thread implementando a interface runnable é necessário declarar o objeto como do tipo thread:
![[Pasted image 20251204224307.png]]


*Método lambda:*
![[Pasted image 20251204224807.png]]

Essa é a forma mais simples e a mais utilizada atualmente, ela usa uma expressão lambda para estar rodando uma thread. dentro do método é colocado o que deve ser executado simultaneamente.
É CRUCIAL que ao chamar a função seja utilizado o método `start()` ao invés do `Run()` por que o método `start` cria uma nova thread enquanto o `run` roda na thread que já está, nesse caso, rodando na `main`


# Virtual threads
As  virtual threads são uma revolução de como threads funcionam no java. Elas tornam a forma como o java lida com a concorrência bem mais rápida e acessível.

Basicamente as virtual threads são leves e ao invés de serem gerenciadas e processadas pelo sistema operacional do usuário,  necessitando de uma máquina com boas especificações para se obter melhores resultados, elas são gerenciadas e processadas pela própria JVM, tornando possível a criação de várias threads sem gerar problemas de performance.

Virtual threads tem algumas formas de serem criadas, porém, as principais são:

`Thread.startVirtualThread()`:
![[Pasted image 20251205225403.png]]
Aqui está sendo  criada a thread virtual e logo depois sendo chamada. É necessário sempre tratar o erro `InterruptedExeption` e essa é a primeira forma, utilizando do [[Tratamento de erros| Try, Catch]] para pegar o erro e trata-lo


![[Pasted image 20251205225441.png]]
![[Pasted image 20251205225426.png]]
Essa é a segunda forma de tratar o `InterruptedExeption` que é basicamente utilizando um [[Tratamento de erros| throws]] para falar que a JVM vai lidar com qualquer erro que acontecer.

Essa é a forma ideal de se criar uma virtual thread para algo mais prático, pois é simples e direto.
