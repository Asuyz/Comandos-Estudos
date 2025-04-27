• **Building Relational Data base**

» Criação de um banco de dados.

**OBS » Para transformar o banco de dados em linha de código devemos sempre clicar na setinha azul no ORACLE DATA MODELER, depois no inferior da janela clicar em "engenharia" (A entidade azul ficará amarela), depois na opção chamada GENERATE DDL**..

° Primeiramente começamos criando as **entidades** (quadrados no **Oracle Data Modeler**) para o armazenamento e correlação de informações.

° Podemos dar **relações** (Linhas que se conectam entre as entidades) e atributos (Informações) para as nossas **entidades** e definir a **cardinalidade** entre elas.

• **Relações** 

» Uma relação no Oracle Data Modeler é uma conexão entre duas ou mais entidades que define como os dados estão interligados. Ela representa a associação entre tabelas no banco de dados, permitindo que você especifique como os dados de uma tabela se relacionam com os dados de outra. As relações podem ser de diferentes tipos, como um-para-um, um-para-muitos ou muitos-para-muitos, e são fundamentais para a estruturação e organização do modelo de dados, ajudando a garantir a integridade referencial e a eficiência nas consultas.


» A representação dos **diferentes tipos de relações** é feita a partir da **cardinalidade (simbolos presentes nas relações/linhas)** e seus símbolos podem ser:

° **0 ou O** - Representa zero
° **I** - Representa um
° **⋌** (É similar com o asterisco) - Representa muitos

» Todos esses símbolos podem ser utilizados **juntos**, ou seja é possível criar uma relações totalmente flexíveis.

• **Tipos de relações**:

» Um-para-muitos.

» Muitos-para-muitos.

» Um-para-um.

-------------------------------------------------------------------------------

• **Atributos**

» Utilizamos para a definição de características das nossas **entidades**.

° Cada empresa possui um **padrão** de definição de atributos (nomenclatura/escrita), para uma melhor organização.

° Atributos podem ou não serem obrigatórios e eles são diferidos entre:

» ° Bolinha - Atributo opcional.
» * - Atributo obrigatório. 

° Os atributos podem ser divididos entre tipos de dados diferentes:

**» Domínio
» Lógico
» Distinto
» Estruturado
» Coleção**

° Podemos alocar **bytes** para o armazenamento de informações (números/caracteres), existem vários tipos mas os mais comuns são:

» **Numérico** -  Para o armazenamento de números, onde os bytes representam as casas decimais e a vírgula é representada pela escala (caso for necessário um número que não seja inteiro).

° **Exemplo:**

» Se em um banco de dados estivermos armazenando o atributo **atura** precisamos de alocar três bytes de espaço (3 casas decimais) e duas casas de espaço na parte de **scale** (números depois da vírgula). Então ficara algo como: 1,80 (metros) = 3 bytes (3 casas) e 2 scale (2 números depois da vírgula). **Obs » uma melhor representação dessa situação seria medir a altura em centímetros pois usaríamos apenas 3 bytes de espaço (economizando a memória no disco e na nuvem).**

» **Varchar** - Aloca uma quantia de bytes (que você pode definir) para o armazenamento de informações (caracteres) e os bytes não utilizados são apenas liberados no disco **físico** e não na nuvem (na nuvem a quantidade estabelecida de bytes será a quantidade definida).

» **Char** - Preenche o restante dos bytes alocados (não utilizados) por caracteres em branco (essa opção é **pouco** utilizada.)

» **Nchar/Nvarchar** - Utiliza 2 Bytes por caractere para armazenar os caracteres que fogem dos 256 "padrões" (utilizados para ideogramas ou outra línguas que fogem do abecedário "padrão").

• **Chaves**

° **Chave primária**

» A implementação da chave primeira na **entidade** garante a unicidade dos dados 

° **Chave estrangeira**

» Trás informações para outra **entidade** são representadas por um F (chaves estrangeiras garantem uma melhor organização do banco de dados).

-------------------------------------------------------------------------------

• **Entidade Associativa:**

° Criamos uma entidade associativa para garantir a integridade referencial dos dados em uma relacao N:N (Muitos para Muitos existentes). Podemos nomear essa entidade com a soma dos dois nomes das entidades que farão relação com essa entidade associativa.

» A entidade associativa sempre terão as chaves estrangeiras das entidades que ela esta fazendo relação e essas chaves sempre serão primarias.

° **Ex:** As Entidades Professor e Alunos formam a entidade associativa Professor-Aluno.

• **Diferença entre as linhas no Oracle Data Modeler**

° As linhas (relações) podem ter dois tipos de condições:

» Linha cheia - As chaves estrangeiras irão fazer parte da chave primaria. 

» Linha tracejada - As chaves estrangeiras não irão fazer parte da chave primaria.















•°»
