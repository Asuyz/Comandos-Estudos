• **Como Funciona**:

° A virtualização surgiu da necessidade para a divisão mais eficiente do hardware e do software, no padrão os softwares são instalados no sistema operacional, que está relacionado com o físico (hardware).

° Os upgrades de hardwares são upgrades "verticais", onde para tarefas mais complexas necessitamos de mais memoria, processadores mais rápidos ou memoria de vídeo mais poderosa e eficiente.

° Os clusters de computadores (são computadores interligados que dividem poder de processamento) são utilizados para resolver problemas computacionais mais complexos e criam a definição de upgrade horizontal, apenas adicionando novos computadores no cluster com base na necessidade.

° Cada computador nesse cluster mantém sua própria estrutura de OS (sistema operacional) e também seus próprios processos.

» A virtualização fez possível a **abstração do hardware, pois uma camada de software mimetiza uma infraestrutura física** que é inserida entre o hardware (real) e o OS, assim possibilitando uma separação mais eficiente destas duas camadas. A virtualização permite a instalação de vários OS em um mesmo equipamento por exemplo.

» **A máquina virtual não é nada mais que o inverso dos conceitos introduzidos (um único sistema operacional instalado sob uma única camada de virtualização) que compreende diversos computadores abaixo dela (o cluster)**.

° Ela enxerga todo o hardware dos clusters como um só, permitindo uma flexibilidade no aumento desses recursos para a máquina virtual, sempre que existe uma necessida a mais de poder computacional (processamento e memória) e sempre que a infraestrutura física for insuficiente novos computadores são adicionados nesse cluster.

------------------------------------------------------------

• **Benefícios Da Virtualização**:

° A tecnologia de virtualização permite a simulação de aplicações, servidores, armazenamento e redes, possibilitando a redução de custos, aumentar a eficiência, agilidade, escalabilidade e flexibilidade dentro da infraestrutura corporativa.

° Isso torna possível consolidar servidores, cargas de trabalho e ambientes, aumentar a utilização de recursos e acelerar a implantação de desktop e aplicativos.

» **Redução de custos**:

↪ A virtualização pode causar a redução dos investimentos de em hardware, energia e espaço físico, pois ela permite o reaproveitamento de recursos físicos que acabam ficando ociosos.

° 

» **Redução do tamanho do parque de equipamentos (datacenter)**:

↪ Com o aproveitamento eficiente de recursos, a necessidade de aquisição de novos equipamentos diminui, reduzindo os gastos gerais (instalação, refrigeração, espaço físico, manutenção, consumo de energia).

» **Gerenciamento centralizado**:

↪ Facilita o monitoramento de serviços e processos em execução, pois o gerenciamento é feito de forma centralizada (dependendo da estrategia de virtualização adotada).

» **Manutenção de sistemas legados**:

↪ Permite a simulação de hardwares que já deveriam ter sido aposentados, permitindo emular condições especificar que alguns programas legados necessitam.

» **Ambiente de testes**:

↪ Permite a simulação de hardwares e arquiteturas diferentes, permitindo teste de aplicações, por exemplo é possivel simular um arquitetura ARM (tipica de smartphones) em uma arquitetura x86-64.

» **Confiabilidade e Segurança**:

↪ Como cada máquina virtual (VM) funciona de forma independente, se um problema surgir em uma não irá afetar as demais.

» **Migrações e ampliações simplificadas**:

↪ Trocar o provedor da infraestrutura é simples pois é possivel exportar e importar a vm em ambientes diferentes com facilidade, além disso a expansão de recursos podem ser aumentadas com o compartilhamento de hardware e os upgrades horizontais que os clusters permitem.

-------------------------------------------------------

• **Por Dentro de uma Máquina Virtual**:

» **Infraestrutura**:

↪ Uma VM não nada mais que um computador simulado, possuindo processador, memoria, armazenamento, rede, interfaces e periféricos emulados, com todas as capacidades e funções de um computador físico.

° A virtualização muda fundamentalmente a maneira da computação consolidando as pools. (Pools de virtualização, ou _resource pools_, ==agrupam recursos físicos (CPU, memória, armazenamento) de múltiplos servidores em um único pool lógico==. Essa técnica maximiza a eficiência, permite o compartilhamento de recursos e facilita a movimentação dinâmica de máquinas virtuais (VMs) entre hosts para reduzir o tempo de inatividade.)

° Isso permite a execução de varias máquinas virtuais em uma máquina física assim como vários sistemas Operacionais, além de compartilhar os recursos desse computador único (CPU, memória, dispositivo de rede, armazenamento entre outros), esse software permite criar e executar máquinas é chamado de **hypervisor**.

° Com a ==Virtualização== podemos fornecer uma versão virtual de diversas tecnologias essenciais na computação, as principais são: **Hardware, Armazenamento e Redes**.

↪ **Hardware**: Um sistema operacional pode ser instalado sobre outro tipo de sistema, com seus recursos de *hardware* sendo representados via *software*.

↪ **Armazenamento**: ==SDS== (Software Defined Storage - Armazenamento Definido por Software). É uma camada de software criada sobre os discos físicos, onde os dispositivos acessam esses discos, tornando o acesso mais flexível, gerenciável e personalizável.

↪ **Redes**: ==SDN==(Software Defined Networking - Rede Definida por Software). É possível criar um tipo de infraestrutura (software) de redes sobre uma determinada rede física, permitindo o detalhamento de acordo com as necessidades do ambiente.

° Com todos os dispositivos físicos podendo ser representados em forma de softwares: servidores e estações se tornam **VM's**, com a rede e armazenamento se tornando **SND e SDS** construímos o **SDDC** (**Data Center Definido por Software**).

» ==***Termos (Para entendimento geral)***==

| Termo                              | Definição                                                                                                                                                                                 |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hospedeiro (_host_)**            | Trata-se da infraestrutura real, local da qual as VMs ficaram hospedadas; ele pode ter seu próprio sistema operacional (instalado diretamente no hardware, de forma convencional) ou não. |
| **Hypervisor**                     | É uma camada de _software_ localizada entre a camada de _hardware_ e o sistema operacional.                                                                                               |
| **Convidado ou hóspede (_guest_)** | É a máquina (VM) instalada sob o _hardware_ emulado.                                                                                                                                      |

-----------------------------------------

• **Tipos de Virtualização**

↪ **Virtualização de Aplicativos**: Fornece um aplicado hospedado em uma única máquina para um grande número de usuários. O usuário final não precisa de um *hardware* de alta qualidade para executar o aplicativo.(parei no segundo paragrafo.)

↪ **Sistema Virtualizado por Máquina Virtual (H-Based)**: **H-based (Hypervisor Based)** é o modelo mais comum de virtualização, onde cada VM exige um SO completo, com kernel, binários e bibliotecas próprios — o que gera alto consumo de espaço e custo de manutenção. Múltiplas VMs rodam sobre a mesma infraestrutura física, cada uma com seu **SO convidado** (guest OS) independente, enquanto o SO que roda diretamente no hardware é chamado de **SO hospedeiro** (host OS).

» O gerenciamento dessas VMs é feito pelo **Hypervisor**, camada responsável por simular o hardware e permitir que diferentes sistemas operacionais sejam executados sobre um único servidor físico. Existem dois tipos: o **Tipo 1** (bare-metal), que roda diretamente no hardware sem depender de um SO hospedeiro, e o **Tipo 2** (hosted), que roda sobre um SO hospedeiro — sendo o VirtualBox um exemplo desse segundo tipo.

↪ **Sistema Virtualizado por Container (OS-Based)**: A virtualização por OS based passou a ser difundida após o surgimento do **Docker**. A virtualização por contêiner possibilita, por exemplo, portar a sua aplicação direto de um notebook para o servidor de produção ou por uma instância virtual em uma nuvem pública.

-----------------------------------------------------------------

• **VM ou Container?**

° A grande diferença entre esses tipos de virtualização são que os containers são executados como um processo isolado dentro do host e compartilham o mesmo *Kernel (SO)*, enquanto a *VM* possui um *OS* completo para cada máquina virtual

| **Virtual machine**                   | **Container**                           |
| ------------------------------------- | --------------------------------------- |
| Desempenho limitado                   | Desempenho nativo                       |
| Virtualização em nível de hardware    | Virtualização de SO                     |
| Aloca memória necessária              | Requer menos espaço de memória          |
| Cada VM é executada em seu próprio SO | Todos os containers compartilham o SO   |
| Tempo de inicialização em minutos     | Tempo de inicialização em milissegundos |

» **VM**: É a melhor opção quando se tem uma grande variedade de instâncias de SOs (OS) para gerenciar ou quando precisamos executar vários aplicativos em diversos servidores.

» **Container** é a melhor opção quando sua prioridade é executar o maior número de aplicativos em um menor número de servidores.

° Comparando a virtualização por container com máquinas virtuais (**H-Based**) é possível afirmar que a **OS-Based** possui mais vulnerabilidades em quesitos de isolamento de segurança, mas apresentam maior flexibilidade em seu uso.

° A utilização das duas formas em um mesmo ambiente de trabalho é totalmente normal e é utilizada para obter a funcionalidade máxima do ambiente.

------------------------------------------------------------

• **Mais sobre o Hypervisor**

° O hypervisor veio como uma forma de ultrapassar as possíveis limitações da arquitetura e custos altos na utilização de servidores, como citado acima eles podem ser executados no **hardware físico** (chamados de *bare-metal*) ou via sistema operacial (*hosted*). Os **hypervisores** são categorizados pelo modelo de implantação, se são do tipo monolíticos ou microkernelizados.

↪ **Hypervisor Monolítico**: As máquinas virtuais são gerenciadas pelo *hypervisor* e os drivers são hospedados e isso trás benefícios no uso. Um dos benefícios é que geralmente não precisaremos de um controle na partição principal ou no sistema operacional, pois os sistemas operacionais *visitantes* interagem direto com o hardware utilizado via *hypervisor*, o único empecilho é a quantidade de modelos de hardware diferentes dificultando o desenvolvimento específico do *hypervisor*.

↪ **Hypervisor Microkernelizado**: Nesse modelo o *hypervisor* possui um tipo de S.O (Systems Operation) atuando na raiz (root) ou na partição principal, com isso não é necessário drivers desenvolvidos especificamente para o *hypervisor*. Essa partição fornece o necessário para o acesso direto do hardware do **host**. Os drivers dos hardwares físicos são instalados no sistema operacional em execução na partição principal, não sendo necessário a instalação dos drivers nos sistemas operacionais **visitantes** (**guests**), dessa forma o sistema visitante acessa o hardware físico se comunicando direto com a partição principal.

↪ **Virtualização Total**: Nesse modelo o sistema *visitante* (**guest**) não é capaz de entender se está sendo executado em um ambiente virtual. Portanto, se comporta como estivesse sendo executado em um ambiente real. Com isso podemos instalar um *OS* na máquina virtual sem precisar de nenhum tipo de modificação ou configuração para seu funcionamento, todos os recursos são entregues pelo hypervisor na maior parte das vezes, essa técnica é mais utilizado em sistemas como *Windows e MacOs*, pois o código fechad não permitem mudanças para reconhecerem que estão em um ambiente virtual.

» A principal vantagem desse meio é a quantidade minima de restrições para o que pode ser virtualizado, como consequência temos uma perca de desempenho, pois não há trabalho mútuo entre o *guest* e o *hypervisor*.  

↪ **Para-Virtualização**: Nesse modelo o sistema *guest* entende que está sendo virtualizado, e com isso as instruções privilegiadas são executadas de forma diferente, diretamente no hardware sem a necessidade de um software como o *hypervisor*. A grande maioria dos recursos não são interpretados como recursos pelo *hypervisor*, resultando em um ganho de performance (especialmente em instruções I/Os de rede e disco).

|                        |                                                         |
| ---------------------- | ------------------------------------------------------- |
| Benefícios da técnica  | Melhor utilização de recursos ao oferecer virtualização |
| Relação com desempenho | Desempenho superior à virtualização total               |

» Nesse modelo exige a necessidade de alteração do *kernel*, sendo somente disponíveis em sistemas onde o código fonte pode ser alterado

---------------------------------------------------------

• **Tipos de configuração de rede**

» Para lidar com uma rede de máquinas virtuais é necessário o entendimento de configurações de rede que são oferecidas, as mais comuns são:

↪ **HOST-ONLY**: Cria uma *LAN* privada compartilhada entre o *host* e suas máquinas virtuais. As Máquinas virtuais nessa rede não podem se comunicar com computadores externos.

↪ **NAT/SHARED**: As máquinas virtuais podem acessar outros computadores na *LAN* ou internet, mas as conexões serão vindos do *host do IP*. Os outros computadores não podem iniciar conexões com as máquinas virtuais a menos que seja configurado o redirecionamento de portas (*post-forwarding*) no computador *host*.

↪ **BRIDGED**: As Máquinas virtuais compartilham o adaptador de Internet físico do host, mas possuem os próprios endereços *IPs* e *MACs*. Elas Aparecem na mesma sub-rede do *host*. Essa é a unica configuração que permite que outros computadores inciem conexões de entrada na máquina virtual, também é a unica configuração que permite outras máquinas externas (*roteador ou firewall*), distingam o tráfego das máquinas virtuais.

| **Configuração**                      | Host-Only | NAT | Bridge |
| ------------------------------------- | --------- | --- | ------ |
| VMs podem acessar outras VMs          | Sim       | Sim | Sim    |
| VMs podem acessar o hospedeiro        | Sim       | Sim | Sim    |
| VMs podem acessar outros computadores | Não       | Sim | Sim    |
| O hospedeiro pode acessar VMs         | Sim       | Sim | Sim    |
| Outros computadores podem acessar VMs | Não       | Não | Sim    |

----------------------------------------------------------

• **Considerações Extras**

↪ **Recursos Adicionais das VMs**: Os softwares VMWare e o VirtualBox oferecem a opção de instalar recursos adicionais na máquina virtual, que facilitam com que o sistema *host* interage com a VM, especialmente o compartilhamento de arquivos entre os dois. Esses softwares permitem, entre outras possibilidades a instalação de um driver para a placa de vídeo virtual, permitindo a emulação de um desktop em "tela cheia".

↪ **Pastas Compartilhadas**: Esse é um recurso que possibilita a troca de informações entre o *host* e a VM, assim possibilitando arquivos estarem disponíveis nos dois sistemas. É recomendado utilizar esse recurso marcando a pasta em questão como **somente-leitura**.

↪ **Snapshots**: Snapshots em máquinas virtuais (VMs) funcionam como pontos de restauração que salvam o estado da máquina em um momento específico. Eles podem armazenar informações como o disco virtual, configurações da VM e até mesmo a memória RAM, dependendo do hypervisor utilizado. Isso permite retornar rapidamente ao estado anterior caso alguma atualização, instalação ou configuração cause problemas. É uma técnica muito utilizada em laboratórios, homelabs, ambientes de teste e manutenção de servidores virtuais.

------------------------------------------------------------

 