
#### Como o backend sabe oque fazer em cada requisição

A forma de explicarmos para o backend oque deve ser feito é por meio da URL da requisição e do método de requisição.


#### Exemplos de uma URL

`https://www.exemplo.com/listar-produtos?filtro=maisvendidos#titulo`

- Protocolo: `https`
- Nome do Host: `www.exemplo.com`
- rota(ou caminho): `/listar-produtos`
- Parâmetros de consulta: `?filtro=mais-vendidos`
- Fragmento: `#titulo`


![[Pasted image 20240706101451.png]]

#### Métodos de requisição 

##### GET
- Obtém dados do servidor
- Exemplo: Carregar uma página web ou buscar informações de usuário.
- Basicamente diz ao backend que queremos obter algo que pode ser uma lista de dados, uma página html, etc.
##### POST
- envia dados para serem processados
- Usado quando queremos enviar informações ao backend
- Exemplo: vamos enviar dados de um formulário ao backend como um login ou um cadastro então usamos o post e passamos no corpo as informações(nome, email, senha, etc.)
##### PUT
- Atualiza dados existentes no servidor
- é exatamente igual ao POST em questão de URL entretanto sua URL possui um id ou um identificador que fala para o backend o dado que vai ser atualizado 
- Exemplo: Quando vamos alterar os dados de uma conta em um site como senha, email normalmente ao enviar o formulário o identificador é enviado junto com a requisição para dizer ao backend qual registro no banco de dados deve ser atualizado.
##### DELETE
- Remove dados do servidor
- Também recebe um id para que o backend saiba o dado exato que deve ser removido ou deletado
- Exemplo: Deletar uma conta de usuário ou remover um post de blog
