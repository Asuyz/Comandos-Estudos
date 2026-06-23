• **Introdução:**

° A computação em nuvem surgiu com a intenção de proporcionar disponibilidade e acesso de recursos por meio da internet. Com isso Alterando a forma como plataformas de *hardware* e *software* são exploradas.

° O *cloud computing* não pode ser estudado sem a menção da tecnologia de virtualização, como abordado a virtualização permite a divisão de recursos para vários ambiente independentes, sem essa tecnologia cada aplicação precisaria de um servidor próprio e isso aumentaria exponencialmente os custos e recursos para rodar essas aplicações.

° Outro ponto em que a virtualização é de extrema importância para o *cloud computing* é a capacidade de adicionar ou remover recursos sem a interrupção de aplicações em andamento.

----------------------------------------------------------------

• **Infraestrutura Virtual**

° A infraestrutura virtual oferece a possibilidade de gestão de recursos agrupados da organização. Permite a gestão responsiva do usos dos recursos para o melhor investimento em infraestrutura.

» Os principais tipos de **virtualização utilizados são**:

» **Virtualização computacional**: (Abordada no capitulo anterior) 

↪ A virtualização *computacional* é uma técnica para abstrair o *hardware* físico de um sistema operacional. A dissociação do *hardware* físico do sistema operacional permite que vários sistemas operacionais sejam executados simultaneamente dentro de um sistema de computação físico ou cluster.

° Com isso permitindo a criação de várias máquinas virtuais onde cada máquina virtual pode rodar aplicações de formas isoladas.

° É obtida por meio de um *hypervisor* (software de virtualização instalado no sistema de computação físico.)

» **Virtualização de Armazenamento**:

↪ A virtualização de *armazenamento* é a técnica de abstrair os recursos de armazenamento físico para a criação de um armazenamento *virtual*

° Permite consolidar múltiplos dispositivos de armazenamento físico em um único conjunto lógico, disponibilizado como volumes virtuais para os sistemas e aplicações.

° O *software* de virtualização de armazenamento pode ser incorporado como um sistema de computação independente ou como um recurso do *hypervisor*.

» No contexto de um sistema de armazenamento, existem **dois** tipos principais de *virtualização*:

 - **Virtualização de blocos:** usada nesse contexto, refere-se à abstração (separação) do armazenamento lógico (partição) do armazenamento físico, permitindo que ele seja acessado sem considerar o armazenamento físico ou a estrutura heterogênea. Essa separação proporciona aos administradores maior flexibilidade na forma como gerenciam o armazenamento para os usuários finais.

- **Virtualização de arquivos:** aborda os desafios do NAS (*Network-Attached Storage*), eliminando as dependências entre os dados acessados no nível do arquivo e o local onde os arquivos estão fisicamente armazenados. Isso oferece oportunidades para otimizar o uso do armazenamento, consolidar servidores e realizar migrações de arquivos sem interrupções.

» **Virtualização de Rede**:

↪ A virtualização de rede tem a capacidade de abstrair os recursos físicos da rede para a criação de recursos virtuais, também tendo a capacidade de dividir uma rede física em várias redes virtuais, como as LANs virtuais e SANs virtuais.

° Como na virtualização de armazenamento, a virtualização de *redes* pode ser um software separado ou usado como recurso do *hypervisor*

» **Alguns tipos diferentes de redes virtuais**

- **Virtual LAN (VLAN):** uma LAN virtual é uma rede virtual que consiste em comutadores virtuais e/ou físicos, os quais dividem uma LAN em segmentos lógicos menores. Uma VLAN agrupa os nós com um conjunto comum de requisitos funcionais, independentemente da localização física desses nós.

- **Private Virtual LAN (PVLAN):** uma VLAN privada é uma extensão do padrão VLAN e segmenta ainda mais os nós de uma VLAN em VLANs secundárias. Uma PVLAN é composta de uma VLAN primária e uma ou mais VLANs secundárias ou privadas.

- **Virtual Extensible LAN (VXLAN):** uma rede virtual extensível é uma rede de sobreposição (overlay) na camada 2 do modelo OSI, construída sobre uma rede de camada 3. Uma rede de sobreposição é uma rede virtual criada sobre uma infraestrutura de rede existente.

------------------------------------------------------------------

• **Cloud Computing**

° Cloud computing é um modelo que permite o acesso à um pool compartilhado de recursos de computação, como redes, servidores, armazenamentos, aplicativos e serviços que podem ser facilmente fornecidos com pouco esforço de gerenciamento ou interação com o provedor desses serviços.

° Esses recursos são acessados por meio de uma rede ou de uma intranet.

° Os serviços fornecidos por via do *cloud computing* facilitam a obtenção de recursos por empresas menores assim diminuindo os custos das operações da mesma.

» **Características Essenciais:**

↪ **Autoatendimento sob demanda**

↪ **Amplo acesso à Rede**

↪ **Agrupamento de recursos**

↪ **Elasticidade Rápida**

↪ **Serviço mensurável**

---------------------------------------------------------------

»°•↪
