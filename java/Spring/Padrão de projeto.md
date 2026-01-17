Um padrão de projeto é uma solução para problemas que acontecem no desenvolvimento de uma aplicação, elas são estruturas ou templates que ajudam a organizar o código de forma mais eficiente, escalável para assim evitar erros no futuro. 
Os padrões de projetos resolvem problemas recorrentes como organização de código, separação de responsabilidades, facilidade de manutenção e testabilidade, eles oferecem uma linguagem comum entre desenvolvedores e promovem boas práticas de programação.


## O que é um monolito
Um monolito é basicamente quando todos os códigos estão em um mesmo lugar.


## Arquitetura por camadas
Sendo muito boa em projetos médios para pequenos, a arquitetura por camadas utiliza de um padrão de camadas dessa forma: 
![[Pasted image 20250703125011.png]]

*Controller:*
controller é a camada mais perto do usuário, é a camada onde o usuário consome o produto. podendo ser por exemplo um like em uma postagem no instagram. esse consumo é enviado para a camada de service


*Service:*
service é a camada onde vai todo o código bruto da aplicação. é onde é recebido a requisição do usuário. É no service onde vão ficar as funções da aplicação.


*Repository:*
Repository é a camada responsável por acessar o banco de dados, ela abstrai toda a lógica de persistência(salvar, buscar, deletar dados), para criar ela basta criar a interface repository correspondente a entidade e usar simplesmente a anotação `@Repository` e estender de `JpaRepository` passando como parâmetros a entidade desejada e o tipo de dado do ID da entidade, por padrão quando é estendido de `JpaRepository` alguns métodos básicos vem prontos, são eles `save`, `findById`, `findAll`, `delete`, etc.

Abaixo um exemplo da criação de um repository para uma entidade nomeada de Author sem a adição de nenhum método extra:
![[Pasted image 20260112223230.png]]


*Banco de dados:*
Banco de dados é a camada onde está o banco de dados do projeto é onde as informações serão guardadas.



Se necessário também é possível criar outra camada de segurança, sendo ela com o uso do `DTO`

*DTO:*
DTO é um objeto simples utilizado unicamente para transferir dados entre camadas, ele é utilizado principalmente por que permite com que a entidade não seja exposta diretamente e pode controlar quais dados que são enviados/recebidos.

Para criar um DTO é necessário o seguinte:

Primeiro é necessário criar a classe e passar os atributos que se deseja expor logo depois adicionar construtores `NoArgs` e `AllArgs`. Além de métodos `Get` e `Set`, isso pode ser feito pelo lombok sem problemas:
![[Pasted image 20260112225051.png]]

Agora, é  necessário o uso do mapper, para isso, primeiramente ele deve ser criado. Depois de criado usa-se a anotação `@Component` para que não seja preciso criar o objeto manualmente, depois cria-se o método de conversão de entidade para DTO:
![[Pasted image 20260112230415.png]]

Depois é necessário realizar uma verificação de segurança para ver se algo foi passado, por que se nada for passado isso pode quebrar o código:
![[Pasted image 20260112231007.png]]

Depois é preciso criar o DTO vazio para servir de recipiente onde será colocado os dados copiados da entidade:
![[Pasted image 20260112231349.png]]

E posteriormente converter os tipos de entidade para DTO e retornar o DTO:
![[Pasted image 20260112231615.png]]


E para finalizar é só fazer o processo inverso, agora estar fazendo a parte de converter de DTO para entity:
![[Pasted image 20260112232143.png]]



Como um bônus, é possível também utilizar um método para converter uma lista inteira de uma vez, o que pode ser muito útil algumas vezes. Isso é feito por meio de um método `toDTOList`:
![[Pasted image 20260112233236.png]]




