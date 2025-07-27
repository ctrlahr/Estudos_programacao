Criptografias dês de que foram criadas utilizam um sistema de chaves. No contexto de mensagens do WhatsApp que utiliza criptografia para as mensagens um usuário envia a mensagem e ela é criptografada, sendo apenas descriptografada quando chega no seu destino por que para garantir que a mensagem seja enviada apenas para a pessoa que deve receber aquela mensagem o usuário que vai receber essa mensagem tem uma chave para descriptografar o que foi enviado, podendo assim entender a mensagem original. É a chave que permite embaralhar e desembaralhar os dados.

Dentro da criptografia existem dois tipos principais ultimamente que são as criptografias simétricas e as assimétricas.

*Simétricas:* Utilizam da mesma chave para criptografar e descriptografar os dados.

*Assimétrica:* Utiliza de um par de chaves, uma chave pública que terá a forma de criptografação  podendo ser compartilhada para qualquer um já que não é capaz de desembaralhar o conteúdo criptografado por ela e a chave privada que terá a forma de descriptografar aquele dado específico.


### Funções hash
Algorítimos de hash são uma forma de criptografar dados sensíveis de usuários.

Converter um valor em um resultado da aplicação de uma função hash é bem fácil, entretanto, o contrário não é, converter um hash para o que ele era antes não é tão simples assim, isso se dá por que as mesmas foram projetadas para serem unidirecionais.

Antes da senha com hash ser calculada e gravada no banco de dados, um conjunto aleatórios de dados chamado de salt é adicionado a ele, fazendo assim com que os hashes sejam modificados no ponto que mesmo as senhas mais óbvias não podem ser submetidas a força bruta com tabelas arco-íris.
A variante mais simples utiliza do mesmo salt para todas as senhas, entretanto, a mais complexa gera um salt único para cada senha.