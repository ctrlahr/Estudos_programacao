# Dockerfiles
Dockerfiles são arquivos dentro da aplicação que são como um projeto dá arquitetura da aplicação para garantir o funcionamento de forma correta.
É dentro dos dockerfiles que terão as informações necessárias para gerar a imagem do docker

# Imagens
As imagens tem tudo necessário para rodar a aplicação, dessa forma, quando criadas pelos dockerfiles elas armazenam as dependências do projeto para estar funcionando.
então a imagem daquela aplicação está `Static` 

# Containers
Por outro lado, os containers são instâncias de uma imagem então basicamente containers são imagens porém rodando. isso significa que ao invés de serem imagens `Static` um container tem um imagem `running` já que pega a imagem que estava parada e a coloca para funcionar. A imagem contem as informações do ambiente e a instância, nesse caso o container, roda a imagem.
Ao iniciar um container um processo é inicializado na máquina hospedeira. Dessa forma é possível existir vários containers rodando em um só hospedeiro, assim como também é possível ter várias instâncias do mesmo container funcionando ao mesmo tempo na mesma máquina.

# Registros
Registros são um Hub, eles concentram imagens do docker para que sejam reutilizadas em um outro momento por outras pessoas ou pelo próprio time de produção. Existem diversos hubs por ai como por exemplo o da AWS, Azure, dockerhub que concentra imagens da própria comunidade, entre outros.