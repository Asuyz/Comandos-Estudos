• **OpenShift**

» O OpenShift tem grande adesão no mundo corporativo por oferecer componentes além do Kubernetes, ofertando os mesmos como projeto encapsulado. Ele surgiu da necessidade de trabalho com mecanismos de controle e processos mais burocráticos, que são deficientes no Kubernetes.

» Uma de suas características mais importantes é o fato de inerentemente um **sistema distribuído**, o que beneficia o desenvolvimento e implementação de aplicativos na nuvem. Também é fundamento na arquitetura *baseada em microsserviços*, que é importantíssimo para prover funcionalidades diversas, de acordo com a necessidade de cada projeto único. 

» OpenShift é uma plataforma *open source* relacionada à nuvem que usa a tecnologia de **conteinerização**, seguindo os principais conceitos do Kubernetes. Além da orquestração de containers de forma independente da plataforma que são executados, ele auxilia no processo de gerenciamento de containers e também disponibiliza uma interface do usuário baseada na web. Oferece uma **PaaS** e disponibiliza uma integração facilitada com outras ferramentas e **SDKs** (Software Development Kit) para diferentes linguagens. Dentre os diversos serviços oferecidos pelo OpenShift, temos:

↪ **Recursos de CI/CD** (Integração continua/ Entregas continuas)

↪ Politicas-padrão de segurança rígidas, tendo como parte integrante o Controle de Acesso Baseado em Função ( **RBAC** ) para restringir o acesso para usuários autorizados

↪ **Health Check** das aplicações e containers que estão sendo gerenciados

↪ Permite a execução em serviços em nuvem como: **Google Compute Engine, AWS e outros**

↪ Gerenciamento de **configurações e logs**

↪ Facilidades de **implantação e testes**, excluindo a necessidade de manuseio de servidores físicos ou virtuais

------------------------------------------------------

• **Arquitetura do Openshift

``` 
Cluster (Kubernetes, gerenciado pelo OpenShift)
  └── Node (máquina física ou virtual)
        └── Pod (agrupador de containers)
              └── Container (aplicação em si, baseada em Docker)
```  

• **Componentes principais:

↪ **API / Authentication**  

» Porta de entrada para tudo. Controla o acesso às APIs do OpenShift e do Kubernetes. Autenticação via certificados SSL ou OAuth.

↪ **Data Store (etcd)**  

» O "banco de dados" do cluster. Armazena o estado atual de todos os componentes — quem existe, onde está rodando, qual a configuração.

↪ **Scheduler**  

» Decide _onde_ cada carga de trabalho vai rodar, distribuindo pods entre os nodes disponíveis do jeito mais eficiente possível.

↪ **Management / Replication**  

» Processo contínuo que monitora o estado real do cluster, compara com o estado desejado (salvo no etcd) e corrige divergências. É gerenciado por _controllers_ especializados:

- Replication Controller
- Endpoint Controller
- Namespace Controller
- Service Account Controller

» O fluxo da arquitetura do OpenShift pode ser resumido em:

↪ Uma requisição passa pela **API**

↪ O **Scheduler** decide onde alocar essa requisição.

↪ O resultado é registrado no **Date Store**

↪ **Management/Replication** garante que esse estado se mantenha, corrigindo automaticamente se algo sair do esperando ( ex: um **pod** cair ).

• **Funcionamento do Openshift**

» 