a conexão do postgres com o Dbeaver é relativamente simples e intuitiva, primeiro o postgres deve estar rodando então no terminal, basta apenas executar os comandos:


```
sudo systemctl start postgresql
```

```
sudo systemctl enable posgresql
```

Ou, se apenas quiser verificar se já está em funcionamento:
```
sudo systemctl status postgresql
```


Depois, no Dbeaver, criar uma nova conexão e informar que é uma conexão postgres. Configurar a conexão e depois criar o banco de dados.


## Erro do database não aparecer depois de fechar e abrir o DBeaver
Durante a criação do projeto enfrentei um problema que foi eu ter criado o database, porém depois de ter fechado o DBeaver o mesmo sumiu, a solução foi criar uma nova conexão do tipo PostgreSQL e passar que o banco de dados seria o meu, no caso, passar o nome que era o meu database junto com as informações que já estavam nele anteriormente:
![[Pasted image 20250720111506.png]]

No geral, foi preciso:
- Clicar no botão de nova conexão
- Escolher PostgreSQL
- Preencher os campos de `host` como localhost, `port` como a mesma que estava antes, `database` como restaurant-api que era o nome do database e o `user` e a `senha` como os mesmos que estavam anteriormente.