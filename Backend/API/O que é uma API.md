Uma Api é responsável pela comunicação de dois sistemas distintos, então ela serve como um intermediário entre dois sistemas, por exemplo:
	em uma aplicação que faz o consumo de uma Api que contem informações de filmes, essa aplicação tem Um sistema "A" que é justamente a aplicação e esse sistema "A"  tem que de alguma forma se comunicar com um sistema B que pode ser um servidor que tem todas as informações desejadas dentro de um servidor para que essa comunicação aconteça, é utilizado de uma Api como intermediadora entre os sistemas.
	Basicamente, é realizado pela API um request do sistema "A" para o sistema "B" e  o sistema "B" dá uma response ou uma resposta de volta ao sistema "A", no contexto da aplicação de informações de filmes isso aconteceria por exemplo se fosse necessário obter as informações de um filme por exemplo "Homem Aranha", a aplicação "A" enviaria ao  servidor(aplicação "B") uma request das informações do filme "Homem Aranha" e o servidor retornaria essas informações se as mesmas existissem.

 Api's podem ser públicas e divulgadas na internet para qualquer pessoa utilizar por exemplo a Api "ViaCep" , é uma Api que fornece informações de vários CEP's pelo brasil, existe também a "OMDb API" que é a Api utilizada para consultas de filmes



Existem 8 principais tipos de Api, são elas as SOAP, REST, GRAPHQL, gRPC, WebSocket, Webhook, MQTT, AMQP
![[Pasted image 20250718122229.png]]

*Api's REST:*
Uma API REST é um tipo de API que se comunica por meio de requisições HTTP, podendo ser requisições PUT, POST, DELETE e GET.
o usuário pede algo por uma requisição então por exemplo, os dados de um usuário específico que está no banco de dados, então é feita uma requisição GET para o banco de dados, e o banco de dados devolve algo.