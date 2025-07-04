

## H2
Para fazer a conexão com o Db H2 é necessário abrir o console do H2 no navegador depois de claro, já ter instalado as dependências referentes a ele, com isso, vai ser necessário ir até o aplication.properties e quase que copiar o que está no console:


![[Pasted image 20250704145726.png]]

![[Pasted image 20250704150354.png]]


É necessário também fazer configurações de delay para fechar e se o H2 vai fechar quando sair da aplicação, para isso basta colocar na frente da configuração de Url :
![[Pasted image 20250704153144.png]]
- É importante que não tenham espaços.


Depois de toda a configuração, agora acessando o painel do console é possível entrar no banco de dados por meio do usuário e da senha definidos no arquivo de configuração.

Arquivos sensíveis como senhas, url e username do banco de dados precisam ser guardados em um local em que ninguém além de quem necessita consiga ter acesso, isso serve também para os commits no github, então, não é legal dar commit no github com o aplication.properties com a url, senha e username para acessar o banco de dados, é por isso que se utiliza de um arquivo que deve ficar na raiz do projeto que se chama `.env`, esse arquivo é utilizado para criar variáveis genéricas e é nele que deve ser guardado dados sensíveis:
![[Pasted image 20250704160202.png]]

dessa forma, no aplication.properties o que estaria nos campos de username, url e senha seria a variável de ambiente criada no `.env`:
![[Pasted image 20250704160641.png]]

Mas somente isso não é funcional, é necessário fazer outro passo que é criar variáveis de ambiente

No arquivo de execução do projeto precisa ir em edit configurations
![[Pasted image 20250704161539.png]]

Depois criar uma nova application
![[Pasted image 20250704161610.png]]

É necessário dar o nome da application como o nome do projeto e depois selecionar o arquivo main que vai estar depois em build and run onde está `Main class`
![[Pasted image 20250704161637.png]]

Depois precisa ir em variáveis de ambiente
![[Pasted image 20250704161655.png]]

E por fim, cadastrar as variáveis de ambiente
![[Pasted image 20250704161340.png]]



Ainda existe um último passo que é escrever no arquivo do `.gitignore` que o arquivo `.env` vai ser ignorado:
![[Pasted image 20250704162551.png]]