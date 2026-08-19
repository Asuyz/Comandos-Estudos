
**Tags**: [infra/containers/k8s]
↩ [[!Infra]]

° Pré-requisitos - [[Docker]]: conceito de imagem, container, registry

• **Introdução**

» É uma plataforma open source para orquestração de containers, que automatiza o deployment, escalonamento, balanceamento de carga e gerenciamento de aplicações containerizadas em um cluster de máquinas, abstraindo essa infraestrutura como se fosse um único sistema. Suas principais **caracteristicas** são:

| **Recurso**               | Descrição                                                                                                |
| ------------------------- | -------------------------------------------------------------------------------------------------------- |
| Organização em clusters   | Organização em _clusters_                                                                                |
| Automatização de execução | Automatização de execução de containers                                                                  |
| Replicação                | Replicação de container                                                                                  |
| Autoescalonamento         | Autoescalonamento dos containers                                                                         |
| Suporte a Docker          | Suporte a containers Docker                                                                              |
| Volumes persistentes      | Suporte a volumes persistentes remotos                                                                   |
| Integrações               | Capacidade de integração com serviços de segurança, rede, armazenamento, monitoramento, medição e outros |

» Dentre as funcionalidades desempenhadas pelo Kubernetes, temos:

| **Funcionalidade**            | Descrição                                                                                                                                                            |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gerenciamento de implantações | Gerenciamento e automatização de grande parte das implantações e atualizações de aplicativos                                                                         |
| Otimização de hardware        | Otimização do uso do hardware, aumentando a disponibilidade dos recursos para executar os aplicativos                                                                |
| Orquestração multi-cloud      | Capacidade de orquestrar containers em _clouds_ privadas, públicas ou híbridas e também em múltiplos _hosts_                                                         |
| Autorrecuperação              | Garante a integridade e assegura que os aplicativos sejam autorrecuperáveis em seus containers, com reinício, posicionamento, escalonamento automáticos e replicação |
| Agilidade de escala           | É mais ágil para escalar aplicativos em containers e todos os recursos relacionados                                                                                  |

----------------------------------------------------------------

• **Arquitetura do Kubernetes**

» A arquitetura do Kubernetes segue um esquema de *mestre-trabalador* (control plane + worker nodes), sendo seus principais componentes:

↪ **Control Plane**: Ele é responsável por tomar decisões globais e detectar/responder a eventos que surgirem.

↪ **Interface de comunicação - Kubectl**

» É uma interface de linha de comando que se comunica com um *cluster* Kubernetes por meio de uma API a partir de um computador local, estando sob comando de um DevOps.

| **Componentes Do Control Plane** | Desc                                                                                                                                                                                |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **kube-apiserver**               | - Ponto de entrada central para todas as operações REST<br>- Todos os componentes (e o `kubectl`) se comunicam através dele<br>- Valida e processa requisições                      |
| **etcd**                         | - Banco de dados chave-valor distribuído<br>- Armazena todo o estado do cluster (configurações, secrets, status dos objetos)<br>- Fonte única de verdade do Kubernetes              |
| **kube-scheduler**               | - Decide em qual node cada novo Pod será executado<br>- Considera recursos disponíveis (CPU, memória), afinidade, taints/tolerations, etc.                                          |
| **kube-controller-manager**      | - Executa os "controllers" que monitoram o estado do cluster e tentam convergir para o estado desejado<br>- Exemplos: Node Controller, ReplicaSet Controller, Deployment Controller |
| **cloud-controller-manager**     | - Integra o Kubernetes com APIs de provedores de nuvem (AWS, Azure, GCP)<br>- Gerencia recursos como load balancers e volumes específicos da nuvem                                  |

↪ **Worker Nodes**: São as máquinas onde as cargas de trabalho (aplicações) rodam.

» **Kubernetes Nodes**: é uma VM (_virtual machine_) ou uma máquina física em um determinado _cluster_, controlada no Kubernetes. É responsável pela execução dos seus aplicativos, que são agrupados pelos _pods_. Um nó contém os serviços Docker (container runtime), Kubelet e Kube-Proxy.

| **Componentes Do Worker Nodes** | Desc                                                                                                                                                      |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **kubelet**                     | - Agente que roda em cada node<br>- Garante que os containers descritos nos PodSpecs estejam rodando e saudáveis<br>- Se comunica com o container runtime |
| **kube-proxy**                  | - Gerencia as regras de rede em cada node<br>- Permite comunicação entre Pods e serviços (Services)                                                       |
| **Container Runtime**           | Software responsável por executar os containers (containerd, CRI-O, etc.)                                                                                 |

» Os **objetos** trabalhados no Kubernetes são:

- **Pod**: menor unidade implantável, geralmente com 1 container
- **Deployment**: gerencia ReplicaSets e garante o número desejado de réplicas
- **Service**: expõe Pods como um serviço de rede estável
- **Namespace**: isolamento lógico dentro do cluster

------------------------------------------------------------------

• **Funcionamento do Kubernetes**

» Kubernetes baseia seu funcionamento através de camadas: a camada mais alta desempenha o papel de *gateway* para o acesso ao container e os níveis mais baixos (*pods*), esses criam uma camada extra de abstração que contém toda a complexidade necessária para trabalhar, por exemplo, com rede armazenamento compartilhado, entre outros serviços. 

» O DevOps interage com a camada mais alta por meio da comunicação com a API Server, a principal API do servidor. O usuário final interage com os pods, por meio de clientes e bibliotecas, os **Kube-Proxy**.

» É necessário um plano declarativo de controle (**Kubernetes Control Plane**) no formado JSON ou YAML, para definir o que deve ser criado e gerenciado.

» Esse plano é utilizado pelo servidor mestre para identificar qual é o estado atual do sistema e quais são os requisitos para a execução do aplicativo/serviço na infraestrutura. O aplicativo/serviço que foi definido está contido dentro do **pod** e eles representam a ultima camada do Kubernetes.

• **MiniKube**

» O Minikube é uma ferramenta que permite simular, na própria máquina local, o comportamento de uma aplicação rodando em um cluster Kubernetes sem a necessidade de configurar um cluster completo. Ele cria um cluster Kubernetes simplificado, com um único *node* (instância), voltado para testes e deploys em ambiente de desenvolvimento.

» Nos sistemas operacionais **Windows e macOS**, é necessário um hypervisor para o funcionamento do Minikube. Já em ambientes Linux, isso não é necessário, pois o Minikube pode rodar diretamente sobre o Docker.


------------------------------------------------------------------

• **Kubernetes e Docker**

» O **Kubernetes** e o **Docker Swarm** são ambos ferramentas de orquestração de *clusters*
e são comparados por conta disso. 

» Porém o Papel do Kubernetes é utilizar o Docker para criar containers nos nós do *clusters* e tem como responsabilidade controlar, gerenciar e monitorar o estado dos containers Docker ao longo do cluster.

» O **Docker swarm** é nativo do **Docker** e desempenha as mesmas funcionalidades do **Kubernetes** apresentando variações técnicas e funcionais como:

- Funcionalidade limitada.
- Tolerância a falhas limitada.
- Os serviços podem ser dimensionados manualmente.

» Com essas diferenças o Kubernetes é mais confiável no mercado de tecnologia, contando com recursos de dimensionamento automático e politícas de alta disponibilidade.

---------------------------------------------------------------------

• **Kubernetes e Microsserviços**

» Os recrusos oferecidos pelo Kuberntes são essenciais para o contexto de microsserviços. Por conta disso o uso do **Kubernetes gerenciando um container Docker** se tornou uma prática extremamente poderosa para a implantação dos microsserviços, especialmente os de grande porte.

-----------------------------------------------------------------

• **Kubernetes | Open Shift | Open Stack**

» A comparação entre **Kubernetes**, **Open Shift e Open Stack** não pode ser realizada por conta das suas tecnologias independentes e diferentes na sua essência, usados separadamente um dos outros.

» Segue uma breve descrição dessas três tecnologias.

↪ **Kubernetes**:

» Desempenha o papel de sistema operacional no nível de containers com a responsabilidade de execução da orquestração de containers.

↪ **Open Shift** 

» Incorporou o **Kubernetes** para oferecer funcionalidades além do gerenciamento de containers e foi otimizado para rodar em infraestruturas de *cloud* públicas ou privadas.


↪ **Open Stack**

» Responsável por gerenciar grandes quantidades de recursos computacionais que envolvem processamento, armazenamento e rede. Oferecendo uma plataforma para o gerenciamento da infraestrutura responsável por executar seus servidores.

-------------------------------------------------------------------


° **Relacionados**
- [[Comandos_Kubernetes]]




