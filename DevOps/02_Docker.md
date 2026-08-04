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

» O container compartilha do kernel do sistema operacional do *host*. É um pacote isolado que contém somente o necessário para a aplicação rodar (código, bibliotecas, dependências e configurações), sem um sistema operacional completo.

» Cada container carrega de forma isolada as dependências da aplicação, sendo possível rodar várias instâncias de container no mesmo *host*, com versões diferentes de bibliotecas ou linguagens sem conflito.

» O isolamento é feito através de recursos do kernel do *Linux* sendo os principais:

↪ **namespaces**: Fazem cada container "pensar" que está sozinho no sistema, o mesmo enxerga seus próprios processos de forma isolada de outros containers. 

↪ **cgroups**: Limitam o quanto de CPU, mémoria e outros recursos cada container pode consumir, evitando o uso indevido dos mesmos.

↪ **chroot**: Restringe a visão do sistema de arquivos, fazendo que o container possa apenas enxergar o seu próprio diretório raiz isolado, sem acesso aos arquivos do *host*.

» O **Docker Registry** é uma nuvem de armazenamento das imagens de container, onde podemos subir (push), baixar (pull), pesquisar e compartilhar imagens por lá, sendo o registro público mais famoso, mas também existem registros privados.

------------------------------------

• **Ressalvas no uso do Docker**

» Para o melhor uso das vantagens e benefícios do Docker devemos seguri boas práticas como: 

↪ Um container deve é apenas um **serviço** e não deve ser tratado como máquina virtual.

↪ Por ser um processo do *host* não deve ter uma vida longa, precisa ser iniciado e finalizado.

↪ Não se deve armazenar dados dentro do container. Para o armazenamento de dados dinâmicos, faça o uso do recurso de criar e montar um container como um volume de dados.

↪ Para acesso aos containers Docker, o *host* deve prover recursos de segurança essenciais.

-------------------------------------

• **Automação e implantação em containers Docker**

» A Plataforma Docker possibilita o uso de ferramentas no ambiente de aplicativos que tem como objetivo reduzir o atrito, acelerar a taxa de mudança e melhorar eficiências.

» Devido a caracteristica de suportar implantação CI/CD, adotar um metodo de trabalho de "Container as a Service", possibilita ao time DevOps do desenvolvimento de código de forma colaborativa através do sistema de compartilhamento de imagens.

» Com um *pipeline* unificado, softwares e dependências podem ser facilmente compartilhados e com ambientes de produção, minimizando os conflitos entre os diferentes ambientes, garatindo uma segurança em cadeia para o conteúdo. Isso facilita a construção/testes/implantar e simplifica a implantação de diferentes infraestruturas.

------------------------------------

• **Segurança dos Containers**

» A virtualização por container tem como base propriedades semelhantes às máquinas virtuais, porém a adoção dessa tecnologia no ambiente de trabalho tem como maior obstaculo a segurança. Quando se trata em compartilhamento de recursos por meio de uma mesmo núcleo (container), vêm à tona questões sobres os riscos e vulnerabilidades.

» Para garatir que apenas o container comprometido seja impactado em uma situação de ataque, o ideal é que seja implementado uma camada de separação e isolamento.

» É possível restringir o acesso a alguns recursos específicos para um determinado usuário/grupo de usuários, enquanto outros podem ter acesso após o login no sistema. A aplicação desse sistema pode vir de tecnicas como: **DAC ou MAC**

↪ **Controle de Acesso Discricionário (DAC):**

» Ideia central: **o dono do recurso decide quem pode acessá-lo**.

- Cada arquivo/recurso tem um dono
- Esse dono pode conceder ou revogar permissões para outros usuários.
- É Baseado em ACLs (Acess Control Lists)
- **Desvantagem**: se um usuário tem acesso ao recurso/arquivo ele pode repassar esse acesso a diante (se não for restringido para tal), o controle é "solto" e depende do bom senso do dono de cada recurso.

↪ **Controle de Acesso Obrigatório (MAC):**

» Ideia Central: **um sistema (ou uma política central) decide.** 

- Existe uma política de segurança, definida centralmente (por um administrador ou pelo próprio sistema operacional) que **não pode ser sobrescrito**, nem o dono do arquivo
- Geralmente é utilizado rótulos de segurança (labels) nos usuários e recursos.
- O acesso só é possível se o rótulo do usuário for compativel com o rótulo do recurso (de acordo com a politica do sistema) 
- Diferente do **DAC** o **MAC** é um sistema muito mais rígido e seguro contra o erro humano, ou vazamento indevido, pois nem o dono do arquivo pode liberar o acesso para outros.

--------------------------------------

• **Docker Container e microserviços**

° Os containers são áreas definidas pelo Docker no servidor, onde uma estrutura de microsserviços pode ser implementada compartilhando o mesmo sistema operacional. Desse forma um microsserviço pode ser implementado de forma modular e de acordo com as necessidades de funcionamento do mesmo, onde cada microsserviço pode executar um processo único e se comunicar com outros.

° As características do Docker que possibilitaram o surgimento desses microsserviços que compõem uma determinada aplicação. Também considerando a possibilidade de desenvolver e realizar o deploy desses aplicativos de forma acelerada e a gestão independente de cada microsserviços.

------------------------------------------------------------------

• **Container Docker X Monolíticos e Microsserviços**

° Monolíticos são uma arquitetura tradicional que devido ao seu funcionamento possui um difícil escalamento, pois o aplicativo com essa estrutura se apresenta inteiro e uma unica unidade (serviços, biblotecas etc) apresentando essa dificuldade em se manter atualizado, porém com o beneficio de serem menos complexos para o gerenciamento de transações e segurança, pois possuem apenas uma entrada para a aplicação.

° Em contrapartida temos a arquitetura de microsserviços e aplicativos baseadas em container. Nessa arquitetura cada componente da aplicação realiza uma única função e a executa de forma independente. Essa arquitetura baseada em container abriga microsserviços, facilitando a implantação do aplicativo que ocorre de forma modular e individual, causando o minimo impacto possível na disponibilidade geral do sistema.

• **Exemplo comportamental de cada tipo nos containers**:

↪ **Arquitetura Monolítica**:

» Dentro de um container Docker, o aplicativo node.js de uma arquitetura monolítica se comporta como um único bloco para implantação e é executado como um único serviço, compartilhando os recursos disponíveis para todos os demais containers. Em uma situação de pico de demanda, seria preciso escalar toda a estrutura, pois o monolítico não permite o dimensionamento de partes individuais do aplicativo. A função principal do node.js é distribuir o tráfego para os operadores que compõem o aplicativo monolítico.

↪ **Arquitetura de Microsserviços**:

» O aplicativo node.js de uma arquitetura de microsserviços em um container Docker é composto por recursos individuais que rodam como serviço independente dentro do seu próprio container. Cada recurso pode ser atualizado e escalada separadamente. No cluster principal do node.js, um microsserviço se comunica com os outros por meio de uma API.

------------------------------------------------------------------

• **Armazenamento no Docker e persistência de dados**

» O Docker gerencia seu sistema de arquivos nas imagens e nos containers em execução, sendo totalmente baseado no conceito de layers (camadas).

» Uma imagem do Docker é composta por diversas camadas. Cada camada representa auma instrução no Dockerfile da imagem. As camadas são empilhadas umas sobre as outras, quando criamos um novo container, adicionamos uma nova camada *writable* sobre as camadas subjacentes.

» Para que seja possível o gerenciamento das interações e os conteúdos das camadas de imagem e das camadas do container *writable*, é necessário fazer o uso de drivers de armazenamento ( *storage drivers* ). Os Drivers de armazenamento é responsável por escrever na camada *writable* de um container. Cada driver de armazenamento trata a implementação de forma diferente, podendo ser por **volume**, por **montagem de ligação** ou por **montagem tmpfs** (Caso esteja no Linux). Todas essas formas usam a tecnologia de cópia na gravação ( **CoW - Copy-on-Write** ) e camadas de imagens empilháveis.

↪ **Em resumo**:

» O Docker organiza tudo em **camadas (layers)**:

- Uma **imagem** é formada por várias camadas empilhadas, cada uma correspondendo a uma instrução do Dockerfile.
- Ao rodar um **container**, é adicionada uma nova camada **writable** (gravável) sobre as camadas da imagem (que são somente leitura).
- Os **storage drivers** gerenciam como essas camadas interagem e são escritas — cada driver implementa isso de um jeito diferente (volume, bind mount ou tmpfs no Linux).
- Todos eles usam **Copy-on-Write (CoW)**: em vez de duplicar dados, o sistema só copia e modifica um arquivo quando ele precisa ser alterado, economizando espaço e tornando os containers leves.

• **Maneiras que a persistência de dados é realizada**:

↪ **Montagens de ligação** ( Bind Mounts ):

» Estão em qualquer lugar do host, mas podem ser modificadas por outros aplicativos. As montagens de ligação são vindas diretamente do Docker e são muito eficientes, mas dependentes do sistema de arquivos da máquina **host** que possui uma estrutura de diretórios especifica. Um arquivo ou diretório precisa existir da máquina *host* do container Docker.

↪ **Montagens tmpfs** ( Temporary Filesystem Mounts ):

» Estão no espaço da memória do host e nunca são gravados no sistema de arquivos da máquina *host*. 

» Considere o uso dessa montagem no caso de o container gerar dados de estado não persistentes. Esse tipo de armazenamento evita gravadas dados na camada gravável do container e aumenta seu desempenho.

• **Persistindo Dados no Ambiente Docker**

» Os volumes são considerados a **melhor forma de resolver a persistência de dados em um container**, pois o conteúdo do volume fica fora do ciclo de vida do container, sendo essa também a melhor forma de evitar problemas de desempenho, por conta que os volumes não aumentam o tamanho dos containers que o utilizam.

» Os volumes são gerenciados pelo próprio Docker, por isso, é o mecanismo preferido de persistência utilizado pelos containers Docker.

------------------------------------------------------------------

• **Docker Compose**

» Docker Compose é um gerenciador de containers tendo a principal função de executar vários containers como um único serviço. Se por exemplo existe a necessidade de subir dois containers com função diferentes podemos criar um único arquivo que inicia os dois containers como serviço, sem a necessidade de iniciar cada um de forma separada, tudo isso sendo possível com esse arquivo de configuração.

» O docker-compose.yml ou (.yaml) é semelhante ao Dockerfile, escrito em **YAML**. Dentro desse arquivo podemos definir cada container como serviço e configurar todos os parâmetros necessários, como: **Serviços, Redes, Volumes, Configurações entre outros**.

» A principal vantagem do Docker compose é diminuir a responsabilidade de desenvolvedor ou do *sysadmin* no gerenciamento do *deploy*, pois o compose encapsula os comandos e todas as dependências que a sua aplicaçãoi necessita para executar em qualquer ambiente.

» **Exemplo de um docker-compose**:


```
version: "3.9"
services:
  exemplo-web:
    build:
      context: ./dir
      dockerfile: Dockerfile-alternate
      args:
        versao: 1
    ports:
      - "5432:5432"

```

------------------------------------------------------------------

↪»°•