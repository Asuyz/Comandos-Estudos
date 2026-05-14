• **Como Funciona**:

° A virtualização surgiu da necessidade para a divisão mais eficiente do hardware e do software, no padrão os softwares são instalados no sistema operacional, que está relacionado com o físico (hardware).

° Os upgrades de hardwares são upgrades "verticais", onde para tarefas mais complexas necessitamos de mais memoria, processadores mais rápidos ou memoria de vídeo mais poderosa e eficiente.

° Os clusters de computadores (são computadores interligados que dividem poder de processamento) são utilizados para resolver problemas computacionais mais complexos e criam a definição de upgrade horizontal, apenas adicionando novos computadores no cluster com base na necessidade.

° Cada computador nesse cluster mantém sua própria estrutura de OS (sistema operacional) e também seus próprios processos.

» A virtualização fez possível a **abstração do hardware, pois uma camada de software mimetiza uma infraestrutura física** que é inserida entre o hardware (real) e o OS, assim possibilitando uma separação mais eficiente destas duas camadas. A virtualização permite a instalação de vários OS em um mesmo equipamento por exemplo.

» **A máquina virtual não é nada mais que o inverso dos conceitos introduzidos (um único sistema operacional instalado sob uma única camada de virtualização) que compreende diversos computadores abaixo dela (o cluster)**.

° Ela enxerga todo o hardware dos clusters como um só, permitindo uma flexibilidade no aumento desses recursos para a máquina virtual, sempre que existe uma necessida a mais de poder computacional (processamento, memória ram ou de vídeo) e sempre que a infraestrutura física for insuficiente novos computadores são adicionados nesse cluster.

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

° (parei fig 5)


»°•

