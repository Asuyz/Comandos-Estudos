• **Introdução:**

° A infraestrutura baseada em container ja é uma prática bastante adotada no segmento de tecnologia, essa mesma infraestrutura pode ser realizada na nuvem ou de forma local.

» Containers são uma tecnologia de virtualização leve que permite o empacotamento de uma aplicação junto de todas as suas dependências em uma unidade isolada e portátil.

------------------------------------------------------------------

• **Gancho em Virtualização**

» Como já abordado a *virtualização* possibilitou a abstração da infraestrutura física (hardware), permitindo uma separação mais eficiente entre o *hardware* e o *sistema operacional*, com isso a *virtualização* permite, por exemplo, a instalação de vários sistemas operacionais em uma mesma infraestrutura física.

» O conceito contrário também surgiu, uma única máquina virtual instalado sob uma camada de virtualização de compreende diversos computadores abaixo dela, interpretando como se fosse um único hardware, onde sempre que uma nova demanda precisa ser atendida novos computadores são adicionados a essa infraestrutura. Com a evolução dessa arquitetura em *cluster* problemas de criação de manutenção do *VPS* (Servidor Virtual Privado) começaram a surgir, criando conceitos de virtualização por **máquina** (*H-Based*) e por **containers**.

------------------------------------------------------------------

• **Sistema Virtualizado Por Container (OS-BASED)

» É uma abordagem que, diferente da virtualização tradicional com hypervisor, não emula um hardware completo para cada instância. Em vez disso, todos os containers compartilham o mesmo kernel do sistema operacional host, e o isolamento entre eles é feito por mecanismos do próprio kernel.

↪ **Comparativo entre Container e Hypervisor**

| **Aspecto**   | **Container (OS-Based)**    | **VM (Hypervisor)**         |
| ------------- | --------------------------- | --------------------------- |
| Kernel        | Compartilhamento com o host | Cada VM possui seu Kernel   |
| Overhead      | Muito Baixo                 | Alto (Emulação de Hardware) |
| Tempo de Boot | Segundos                    | Minutos                     |
| Isolamento    | Processo/Kernel-Level       | Hardware-Level              |
| Portabilidade | Alta                        | Menor, pois é mais pesada   |
| Densidade     | Muitos Containers por Host  | Poucas VMs por Host         |

----------------------------------------------------------------

• **Containers e Microcontainers**

» Containers são uma unidade de software que aglomera o código e as dependências de uma aplicação de maneira que a mesma seja executada de forma fácil e eficaz. Isso permite e execução de uma aplicação de forma independente do sistema, pois o container é o próprio pacote executável que carrega tudo que a aplicação necessita (Definições do sistema, bibliotecas, códigos e ferramentas que são tratadas como microcontainers dentro do container). 

------------------------------------------------------------------

• **Docker** 

» Docker é uma plataforma para a criação, execução e deploy de containers, tendo o objetivo de facilitar o desenvolvimento, implantação e execução de aplicações em ambientes isolados.

» Os **principais** componentes da arquitetura do Docker se dão por:

↪ Versões que permitem instalar e executar containers nos sistemas operacionais de forma isolada (**Mac, Linux e Windows**)

↪ **Docker Daemon**: Software que roda na máquina onde foi realizada a instalação do Docker.

↪ **Docker Client**: CLI ou REST API que aceita comandos do usuário e repassa esses comandos ao **Docker Daemon**

↪ **Docker Image**: É um template. Uma imagem onde contém todos os dados e metadados necessários para executar containers a partir de uma imagem. 

↪ **Docker Container**: Detém tudo que é necessário para uma aplicação a ser executada. Cada container é criada a partir de uma imagem Docker, onde cada container é uma aplicação isolada independente.

↪ **Docker Engine**: Usado para criar imagens e containers no Docker.

↪ **Docker Dockerfile**: Um arquivo de texto que contém uma sintaxe para a criação de novas imagens Docker a partir de uma imagem base (Estado inicial de todo container)

↪ **Docker Registry**: Uma coleção de imagens hospedadas e rotuladas que, juntas, permitem a criação do sistema de arquivos de um container (Esse registro pode ser público ou privado.)

↪ **Docker HUB**: É um registro usado para hospedar e baixadr diversas imagens Docker. Pode ser visto como uma plataforma *SaaS* de compartilhamento de gerenciamento de imagens Docker.

↪ **Docker Compose**: Usado para definir aplicações usando diversos containers no Docker.

↪ **Docker Swarm**: É uma ferramenta quer permite o agrupamento (clustering) de containers Docker.


• **Como funciona o Docker**

» 























↪»°•