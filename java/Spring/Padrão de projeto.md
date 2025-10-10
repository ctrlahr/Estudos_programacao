Um padrão de projeto é uma solução para problemas que acontecem no desenvolvimento de uma aplicação, elas são estruturas ou templates que ajudam a organizar o código de forma mais eficiente, escalável para assim evitar erros no futuro. 
Os padrões de projetos resolvem problemas recorrentes como organização de código, separação de responsabilidades, facilidade de manutenção e testabilidade, eles oferecem uma linguagem comum entre desenvolvedores e promovem boas práticas de programação.


## O que é um monolito
Um monolito é basicamente quando todos os códigos estão em um mesmo lugar.


## Arquitetura por camadas
Sendo muito boa em projetos médios para pequenos, a arquitetura por camadas utiliza de um padrão de camadas dessa forma: 
![[Pasted image 20250703125011.png]]
- controller é a camada mais perto do usuário, é a camada onde o usuário consome o produto. podendo ser por exemplo um like em uma postagem no instagram. esse consumo é enviado para a camada de service
- service é a camada onde vai todo o código bruto da aplicação. é onde é recebido a requisição do usuário.
- Repository age como uma camada mediadora com a camada de banco de dados.
- Banco de dados é a camada onde está o banco de dados do projeto é onde as informações serão guardadas.

