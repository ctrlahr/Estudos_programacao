
# Rest
Uma API rest é como um garçom em um restaurante, onde é falado para ele o que se quer, o que o cliente quer, ele vai escutar e depois vai até a cozinha. Avisa aos cozinheiros o que o cliente quer e posteriormente, quando o produto está pronto ele retorna com o que foi pedido.
API's rest são basicamente a mesma coisa, o usuário vai fazer uma requisição, que pode ser qualquer coisa como clicar em um botão que retorna uma lista de todos os filmes cadastrados no site por exemplo, assim que o usuário clicar no botão, a API Rest vai pegar o que o usuário quer que nesse caso é uma lista de filmes, vai consultar no banco de dados e retornará com a lista se a mesma existir.

REST significa representational state transfer.
API's rest utilizam requisições GET, POST, PUT e DELETE.

GET serve para pegar dados do banco de dados, é a forma de se obter ou consultar algo do banco. Então por exemplo no Instagram, ao pesquisar por um perfil está sendo feito um GET de todos os usuários com o que foi digitado, é um GET um pouco especial mas não deixa de ser uma consulta no banco de dados com GET.

POST é utilizado para colocar algo novo no banco, pode ser utilizado por exemplo em um cadastro de um novo usuário ou algo semelhante.

PUT serve para atualizar dados do banco, por exemplo se o usuário trocou o nome de perfil ou algo do tipo.

DELETE é bem auto explicativo, serve para deletar algo do banco.


API's REST são stateless, isso significa que cada requisição é completamente independente, as requisições não são lembradas pelo servidor, o que torna API's REST muito boas para requisições rápidas já que o servidor não terá o trabalho de verificar que usuário que pediu tal coisa, etc.

Porém, REST não é bom para transferências bancárias por exemplo, devido a suas peculiaridades.
Para operações bancárias é necessário um sistema ou um modelo de API que garanta que a operação acontecerá apenas uma vez, ela deve funcionar completamente ou não funcionar, o dinheiro não pode correr o risco de simplesmente sumir e também é necessário que seja deixado um rastro, um histórico claro do que aconteceu.



# Soap
SOAP significa simple object access protocol, ele é um protocolo mais antigo e formal para comunicação entre sistemas, é como enviar uma carta registrada com diversas camadas de envelopes, selos e comprovantes.
Uma API SOAP utiliza o XML para estruturar as requisições, uma requisição se parece com isso:
```
<envelope>
  <cabeçalho>
    <!-- Informações de segurança, autenticação -->
  </cabeçalho>
  <corpo>
    <!-- Sua requisição real aqui -->
    <transferencia>
      <valor>100</valor>
      <destino>123456</destino>
    </transferencia>
  </corpo>
</envelope>
```

API's SOAP são principalmente utilizadas quando se é necessário de bastante segurança devido a seu suporte nativo para criptografia, assinatura digital e autenticação em múltiplas camadas. Além de garantir a entrega da mensagem e ter todo um controle de ordem para garantir que cada mensagem chegará na ordem correta.

API's SOAP são utilizadas em sua grande maioria em transferências bancárias, processamento de pagamentos e em sistemas de compensação entre bancos justamente a suas características que dão segurança de que por exemplo a transferência ou acontecerá ou não, é impossível ela se perder ou algo do tipo.

Apesar de não ser veloz como uma API REST, uma API SOAP tem suas próprias características que a tornam indispensável no mundo tecnológico.


# gRPC
o gRPC é basicamente a forma moderna e de alto desempenho do google para o [[RPC]]. Muito mais rápida que suas versões anteriores ela pode chegar a ser até 10x mais rápida que uma requisição REST, sendo ideal para comunicações entre microserviços.
Porém o gRPC não é bom para browsers por exemplo, APIs REST ainda se mantem melhores e mais eficientes quando a questão é requisições online, o gRPC é mais útil para comunicações entre serviços backend como por exemplo a comunicação entre vários microserviços. 

