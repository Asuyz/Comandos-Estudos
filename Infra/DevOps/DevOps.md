

**Tags**: [infra/devops]
↩ [[(DevOps)]]

----------------------

• **Introdução | O que é DevOps?**

» **DevOps** é uma cultura que utiliza práticas e ferramentas para aumentar a capacidade de desenvolvimento e entrega de softwares, serviços, aplicativos e outros produtos de tecnologia com alta velocidade, sem colocar o risco a estabilidade.


• **Como o DevOps funciona?**

» Os times de Dev ( Desenvolvimento ) e Ops ( sysadmins ) deixam de ser tratados como dois grupos e se tornam um único time.

» Sysadmins ( Administradores de Sistemas ) **participam desde o inicio do desenvolvimento.**

» Desenvolvedores acompanham as etapas do software **até a produção.**

» Mesmo aplicando essa cultura não é necessário que Dev vire Ops e nem o contrário, apenas é necessário saber o essencial do outro lado para existir a colaboração e não o domínio completo.

» Isso resulta em um ambiente multidisciplinar com: automação de processor manuais, maior autonomia dos desenvolvedores e menor dependência entre as áreas.

• **Benefícios do DevOps**

| **Benefício**                    | **Resumo**                                                                                                                                             |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Aumento da velocidade de entrega | Automação → mais frequência de entregas → detecção e correção de erros mais rápida → vantagem competitiva                                              |
| Escalabilidade                   | Infraestrutura como código reduz interferência manual e risco; permite escalar automaticamente conforme demanda (ex: alarme dispara expansão de infra) |
| Velocidade                       | Times com responsabilidade ponta a ponta, sem depender de outras equipes → menos espera por priorização                                                |
| Colaboração contínua             | Times compartilham responsabilidades e fluxo de trabalho, cultura de "dono" do que é entregue                                                          |
| Confiabilidade                   | Testes automatizados em vários níveis → mais confiança nas entregas                                                                                    |
| Segurança                        | Políticas automáticas: controle de acesso, permissionamento, autorização, gerenciamento de configuração                                                |

• **Práticas do DevOps**

↪ **Entregas frequentes e pequenas**: Utilizando metodologias ágeis ( SCRUM, KANBAN ).

↪ **Arquitetura de Microsserviços**: Sistemas complexos divididos em serviços pequenos, independentes, com contexto único de negócio, com comunicação via interface ( Exemplo: HTTP ). Reduzindo a sobrecarga de coordenar updates em sistemas monóliticos.

↪ **IAC - Infraestrutura como Código**: Infraestrutura tratada como código versionável, integrável continuamente via API, reaproveitável e replicável entre ambientes.

↪ **Integração Contínua ( CI )**: Testes automáticos a cada envio de código ao repositório central com o objetivo de achar erros rapidamente, melhorar sua qualidade e reduzir o tempo de validação do mesmo. 

↪ **Entrega Contínua ( CD )**: Após CI, o pacote fica pronto e confiável para ser implantado a qualquer momento.

↪ **Monitoração, Alarme, Log e Indexação**: Captura e indexação de logs para melhor rastreabilidade, causa real de problemas e dashboards em tempo real.

↪ **Comunicação e Colaboração**: Pilar cultural com o compartilhamento de informações e processos entre os times unificados.

• **Estágios e Ferramentas do ciclo DevOps**

» Os estágios do **DevOps** podem ser resumidos em: Plan → Code → Build → Test → Release → Deploy → Operate → Monitor → Plan.

| Estágio | O que acontece                                                                                      | Ferramentas utilizadas                                       |
| ------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Plan    | Dev e sysadmin estimam e fatiam atividades com práticas ágeis                                       | Jira                                                         |
| Code    | Codificação do software e da infra como código                                                      | Git, Confluence, Jira                                        |
| Build   | Código e dependências são baixados, compilados, empacotados; alguns testes básicos já rodam aqui    | Maven, Gradle                                                |
| Test    | Testes unitários, smoke test, integração, regressão, ponta a ponta + testes de infraestrutura       | JUnit (unitário), Selenium (fluxos/telas), TestInfra (infra) |
| Release | Lançamento automatizado da versão via pipeline (pode ter etapas de aprovação e múltiplos ambientes) | Jenkins, CodeShip                                            |
| Deploy  | Instalação automatizada do software e infra, uso de contêineres                                     | Docker, AWS                                                  |
| Operate | Operação, escalonamento, manutenção; orquestração de contêineres                                    | Kubernetes, Apache Mesos, Ansible                            |
| Monitor | Acompanhamento em tempo real, troubleshooting, dashboards                                           | Splunk, Datadog, Nagios                                      |

• **Sobre as Ferramentas Citadas**:

- **Git**: controle de versão distribuído; permite múltiplas pessoas editando o mesmo arquivo (branches, merges).

- **Maven vs Gradle**: Maven automatiza build e dependências via XML; Gradle segue os mesmos conceitos, mas usa uma DSL baseada em Groovy (mais flexível).

- **Docker x Máquina Virtual**: a diferença central é que o Docker **não precisa de um SO convidado** — ele usa o SO do host (via Docker Engine), enquanto uma VM tradicional roda um Guest OS completo por aplicação. Isso torna os contêineres mais leves.

- **Kubernetes / Apache Mesos**: orquestradores de contêiner _open source_. Automatizam implantação, dimensionamento e gestão de apps, criando uma camada de abstração sobre a infra (tratam múltiplos hosts como um cluster único). Oferecem:
    - **Load balance** (balanceamento de carga)
    - **Service discovery** (descoberta automática de serviços)
    - **Self healing** (autorrecuperação de contêineres com problema)

- **Ansible**: ferramenta de automação para gerenciar múltiplas máquinas via SSH, sem precisar de agentes instalados nas máquinas-alvo.

• **Escalonamento de Infraestrutura**

↪ **Vertical**: Aumenta os recursos do **host** como: CPU, memória, disco entre outros, sendo o escalonamento mais caro e possuindo limite **físico**.

↪ **Horizontal**: Aumenta a quantidade de hosts, distribuindo o trabalho. Prática recomendada para microsserviços. Utilizando **containers e orquestradores** preparados para essa prática.

----------------------------------------------------------

• **DevSecOps**

» Segurança é discutida historicamente só após o software chegar na sua etapa de produção ou logo após um incidente

» Para evitar isso existe um movimento conhecido como: **Shifting Security Left**: foca em mover a preocupação com segurança para o **início** do ciclo (a "esquerda" do fluxo Dev → Test → Staging → Production).

• **Vantagens da aplicação do DevSecOps:

- Segurança distribuída dentro da organização (não é só de um time)

- Vulnerabilidades identificadas e resolvidas **antes** da entrega

- Consciência de segurança disseminada entre os times

- Software mais seguro e com mais qualidade

- Redução de custo para identificar/resolver problemas de segurança (quanto mais cedo detecta, mais barato corrigir)

----------------------------------------------------

• **Resumo dos conteúdos abordados**:

- **DevOps = cultura**, não ferramenta nem cargo.

- Problema original: Dev (quer mudar rápido) vs Ops (quer estabilidade) → times separados, metas conflitantes.

- Solução: **unificar times**, responsabilidade ponta a ponta, automação de tudo que é manual.

- Benefícios: velocidade, escalabilidade, colaboração, confiabilidade, segurança.
- Práticas centrais: entregas pequenas e frequentes, microsserviços, IaC, CI/CD, monitoração, comunicação.

- Ciclo infinito: Plan → Code → Build → Test → Release → Deploy → Operate → Monitor.

- Segurança não é etapa final: **DevSecOps** traz segurança para o começo do ciclo (shift left).

--------

