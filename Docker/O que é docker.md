Docker foi criado para solucionar os problemas antes enfrentados quando se eram utilizadas máquinas virtuais.
docker cria containers que são capazes de proporcionar um ambiente completamente favorável para uma aplicação específica funcionar corretamente. Diferente das máquinas virtuais, docker apenas usa o mínimo necessário para que a aplicação funcione então não é preciso um novo sistema operacional, ocupando grande parte da RAM, etc. Apenas é compartilhado o mesmo sistema para a utilização de um container.

## Diferença de um container para uma VM
Existem algumas diferenças, entre elas a principal é essa:
- Uma VM roda um novo kernel talvez de outra arquitetura enquanto um container reaproveita o mesmo kernel na mesma arquitetura de hardware

Mas também existem outras como por exemplo:
- VM's consomem mais memória RAM e armazenamento já que precisam operar um sistema operacional completo algo que não acontece nos containers já que compartilham do mesmo kernel.
- VM's são melhores em casos de diferentes sistemas operacionais enquanto containers se mostram úteis em microsserviços e arquiteturas modernas


