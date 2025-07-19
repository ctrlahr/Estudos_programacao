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