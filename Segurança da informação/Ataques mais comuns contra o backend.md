
# SQL injection
Um ataque do tipo SQL injection se consiste em queries indesejadas serem executadas para o backend através da aplicação. Então, por exemplo. Enviar um DELETE de algum usuário específico ou as vezes até de todos os usuários.

O SQL injection pode ser executado de algumas maneiras:

## Classic SQL injection
A maneira clássica é simplesmente escrevendo uma querie SQL em um local onde a aplicação usa o input do usuário para montar uma querie, pode ser em uma URL, em um formulário desprotegido do frontend, etc. Qualquer lugar que sirva de montagem para uma querie já basta.

é possível negligenciar uma parte de uma querie utilizando os caracteres de comentário do SQL depois de uma aspas simples (`'--`), se essa forma for utilizada por exemplo em uma sessão de login, mais especificamente na área do email, é possível ganhar acesso a conta de alguém sabendo unicamente o email.
Para isso basta durante a requisição no insomnia por exemplo, depois do email passar uma aspas simples seguida de dois hifens:
![[Pasted image 20260303215440.png]]

Isso dá certo por que ao escrever os caracteres de comentário do SQL, isso encerra a string por causa da vírgula simples única e comenta todo o resto da requisição, então se por exemplo, para dar um select na tabela era necessário o email e a senha, essa querie, quando comentada todo o resto depois do email torna a senha algo desnecessário para executar a querie, nesse caso, realizando a querie SELECT mesmo sem ter a senha.
![[Pasted image 20260303220223.png]]

O classic SQL injection tem duas maneiras de ser executado.

- A primeira delas é forçando um erro na aplicação, o que talvez divulgue informações confidenciais. Essa forma é chamada de Error-based

- Já a segunda é usando o operador UNION para combinar resultados de outras tabelas e anexar uma segunda query, por  exemplo, em um sistema que a query original é 
	`SELECT nome, email FROM produtos WHERE id = INPUT`, usando o UNION, depois fica assim
	`0 UNION SELECT username, password FROM users --`, fazendo a query ser mais do que deveria ser e divulgando assim conteúdos sensíveis e confidenciais.

### Como se proteger
A primeira parte essencial é NUNCA executar SQL no frontend pois todo o código do frontend fica disponível na ferramenta de desenvolvedor dos navegadores, permitindo até mesmo alterações temporárias, o que pode fazer com que uma querie seja executada afim de conseguir algum dado sensível.

 A segunda parte necessária é utilizar bind variables.
 Bind variables são utilizadas como parâmetros no momento da consulta SQL, elas são representadas com "?", então é necessário utilizar as bind variables e complementar depois no código, falando o que elas representam.