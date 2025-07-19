Essa pasta trata dos meus aprendizados enquanto estou fazendo o projeto de cadastro de usuários em um restaurante para reservar mesas


## Projeto

API:
- Registrar reservas de mesas
- Controlar o status das reservas e das mesas
- Bloquear reservas quando a mesa estiver ocupada


Tabela de mesa:
- Id da mesa 
- Status da mesa(ocupada/não ocupada)
- foreign key para a tabela de usuário, para relacionar o usuário que estiver ocupando a mesa naquele momento.


Tabela do usuário:
- Id do usuário
- Nome
- Email
- Senha(ver se deixo a senha no Db ou se deixo ela em local mais seguro, no geral, ver como posso proteger essa senha e esse email do usuário na hora do cadastro dele).
- Foreign key para a tabela de mesas.