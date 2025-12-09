O maven é basicamente uma ferramenta de gerenciamento de projetos e automação de build.


Relacionado com gerenciamento de projetos, basicamente o maven é responsável por gerenciar as dependências de um projeto como spring, hibernate, etc. Sem o maven seria necessário baixar o arquivo jar manualmente, incluir nos arquivos do projeto, etc. No geral seria bem mais trabalhoso.

O maven também é responsável por estruturar o projeto, basicamente é o maven que se responsabiliza em colocar cada parte do projeto em seu devido local como por exemplo o código fonte em `src/main/java`

Além disso, ele também realiza a configuração do projeto como qual versão do java utilizar, metadados do projeto, etc.


E relacionado a automação de build o maven consegue estar transformando o código-fonte em um programa executável com um simples comando.


O maven utiliza como "coração" do projeto um arquivo `POM.xml` que nele é onde todas as informações relacionadas a construção de um projeto com o maven, é nele também que são gerenciadas as dependências do projeto:
![[Pasted image 20251208221135.png]]


