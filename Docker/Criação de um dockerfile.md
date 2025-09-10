A primeira necessidade é criar o arquivo dockerfile, ele precisa estar na raiz do projeto.
Depois, precisa importar o maven para conseguir realizar o build da aplicação, para isso existe uma imagem do maven já existente:
![[Pasted image 20250908091712.png]]

depois de pegar o maven é necessário levar todos os arquivos da aplicação para dentro do container já que eles o material que deve ser armazenado em um container. 
Isso é feito com o comando `COPY`:
![[Pasted image 20250908092011.png]]
- Se a pasta `app/src` não existir o docker automaticamente criará ela. 
- Nesse caso está sendo copiada toda a pasta `src` para dentro de `app/src` 
- Depois também é necessário copiar o arquivo `pom.xml` por causa das dependências.
- e, posteriormente, é utilizado o comando `WORKDIR` para mudar o diretório de trabalho atual, funcionando como o comando `cd` no terminal.


Depois, quando estiver no diretório app vai ser necessário realizar a instalação das dependências como maven e o build da aplicação, isso será feito por meio de um comando do próprio maven para fazer a instalação das dependências e gerar o build da aplicação, esse comando é o `RUN mvn clean install`:
![[Pasted image 20250908092924.png]]
Também será copiado o arquivo `.jar` de build que foi gerado e copiar para `/app/jar`:
