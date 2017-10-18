# acesso_cloud_kubernetes
Nesse repositório são descritas as formas de acessos dos usuários a nuvem CaaS/PaaS (_Containers as a service/Platform as a Service/_) kubernetes do IFSC-SJE. Também são descritos seus namespaces e limitações.


## Compreender a motivação para usar namespaces([retirado daqui](https://kubernetes.io/docs/tasks/administer-cluster/namespaces/) e traduzido pelo google translate):

Um único cluster deve ser capaz de satisfazer as necessidades de múltiplos usuários ou grupos de usuários (doravante, uma "comunidade de usuários").

__Os namespaces Kubernetes ajudam diferentes projetos, equipes ou clientes a compartilhar um cluster Kubernetes.__

__Ele faz isso fornecendo o seguinte:__

* Um escopo para [Nomes](https://kubernetes.io/docs/concepts/overview/working-with-objects/names/).
* Um mecanismo para anexar autorização e política a uma subseção do cluster.

__Cada comunidade de usuários quer ser capaz de trabalhar isoladamente de outras comunidades.__

__Cada comunidade de usuários tem sua própria:__

* Recursos (pods, serviços, controladores de replicação, etc.)
* Políticas (que podem ou não podem realizar ações em sua comunidade)
* Restrições (esta comunidade tem permissão dessa quantidade de cota, etc.)

__Um operador de cluster pode criar um espaço de nomes para cada comunidade de usuários exclusivo.__

__O espaço de nomes fornece um escopo exclusivo para:__

* Recursos nomeados (para evitar colisões básicas de nomeação)
* Autoridade de gerenciamento delegada para usuários confiáveis
* Capacidade de limitar o consumo de recursos da comunidade

__Os casos de uso incluem:__

* Como um operador de cluster, eu quero apoiar múltiplas comunidades de usuários em um único cluster.
* Como operador de cluster, eu quero delegar autoridade para partições do cluster para usuários confiáveis nessas comunidades.
* Como operador de cluster, eu quero limitar a quantidade de recursos que cada comunidade pode consumir para limitar o impacto a outras comunidades que usam o cluster.
* Como um usuário de cluster, eu quero interagir com recursos que são pertinentes para minha comunidade de usuários em isolamento do que outras comunidades de usuários estão fazendo no cluster.


## Possuímos os seguintes namespaces:
* producao
* testes
* desenvolvimento
* alunos
* professores
* ensino
* projetos
