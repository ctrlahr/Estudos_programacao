Existem algumas diferenças, entre elas a principal é essa:
- Uma VM roda um novo kernel talvez de outra arquitetura enquanto um container reaproveita o mesmo kernel na mesma arquitetura de hardware

Mas também existem outras como por exemplo:
- VM's consomem mais memória RAM e armazenamento já que precisam operar um sistema operacional completo algo que não acontece nos containers já que compartilham do mesmo kernel.
- VM's são melhores em casos de diferentes sistemas operacionais enquanto containers se mostram úteis em microsserviços e arquiteturas modernas