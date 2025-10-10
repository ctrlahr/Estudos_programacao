Para criar um projeto com o intellij idea free é preciso abrir um site da comunidade chamado spring initializr:
![[Pasted image 20250627012355.png]]
- Nessa imagem temos a primeira opção que é a de project e tem três opções, gradle com groovy, gradle com kotlin e maven, o maven controla as dependências do projeto assim como o groovy.
- Depois tem a opção de linguagem onde tem java, kotlin e groovy.
- Depois a versão do Spring.
- Tem também a aba de dependências que são quase como extensões, são extensões como drivers para banco de dados, auto-refreshers, etc.
- Após isso tem o "project metadata" onde tem:
	- *Group*: group é quem está controlando o projeto então geralmente é a empresa controladora ou o dono, etc. Existe uma particularidade que no spring é escrito ao contrário o "link" então o que a empresa controladora seria por exemplo google.com fica com.google.
	- *Artifact*: É o nome da pasta do projeto. Então ele vai nomear a pasta do projeto.
	- *Name*: É o nome do projeto. Então ele vai nomear o projeto como um todo.
	- *Description*: É simplesmente a descrição do projeto.
	- *Package name*: É o nome do package, é uma boa convenção que ele seja o mesmo do nome da pasta do projeto(artifact)
	- *Packaging*: É a maneira que o projeto será envelopado
	- *Java*: É a versão do java.



## Processo padrão de criação de um projeto
1. Criação do projeto no geral
2. Definição e separação dos arquivos do projeto de acordo com um [[Padrão de projeto]].
3. Criação dos primeiros modelos.
4. Criação do arquivo controller para criação da primeira [[Criação de rotas|| rota]] e das rotas seguintes.
5. [[Transformar classes em entidades de um banco de dados|| Transformação de classes em entidades]] de um banco de dados.
6. 