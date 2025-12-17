Migrations é uma forma de versionamento de um banco de dados, semelhante a um git.
Com as migrations, é possível realizar rollbacks para partes do código que algo não existia, por exemplo, se foi criada uma tabela por engano ela pode ser apagada ao realizar um rollback para antes dela existir.
Toda migration deve ter funções UP e DOWN

Funções UP são executadas quando a migration é executada já as DOWN são executadas quando é realizado um rollback ou algo do tipo.
As funções DOWN são como botões de emergência, elas não fazem nada até o momento que se precisa delas, aí elas são executadas.