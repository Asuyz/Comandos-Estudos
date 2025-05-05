## • **Hyper Text Markup Language**

» Html é uma linguagem para **formatação de textos, inserir imagens e ligações de hipertexto**. Não é possível programar em html pois é uma linguagem de marcação (uso de tags). 
Os navegadores apenas fazem o processo de identificação e executar o que foi especificado pelas marcações. 

° Todo documento em **HTML** apresenta elementos entre setinhas (< e >), essas são as **tags**, elas definem onde cada conteúdo (dentro delas) começam e terminam.

° Um aspecto **MUITO** importante no **html** é a indentação correta das linhas de tag propostas.

```
<tag> ... </tag>(toda tag de fechamento apresenta essa barra).
```

° Alguns elementos são chamados de vazios (void), pois não marcam uma região de texto, apenas 
inserem algo no documento.

» Todos os elementos podem ser atribuídos. Os atributos podem ou não serem obrigatórios.

° Utilize sempre letras **minúsculas** para a escrita de tags:

```html
<tag atributo1 ="valor1" atributo2="valor2">... </tag>
```

-------------------------------------------------------------------------------

## • **Estrutura básica de um documento HTML**

» **< ! DOCTYPE >** : Declaração que define a versão do HTML (HTML5) para o navegador. Deve ser a primeira linha do documento.

» **< html >** : Elemento raiz de um documento HTML. Todo o conteúdo da página deve estar dentro dessa tag.

» **< head >**  : Contém metadados da página, como título (< title >), codificação de caracteres (< meta charset = "UTF-8" >), links para CSS e scripts
° ( A tag charset + o UTF-8 dão a maior compatibilidade para caracteres especiais)

» **< body >** : Define o corpo da página, onde ficam os elementos visíveis pelo usuário, como textos, imagens e botões

#### • **EXEMPLO DE COMO FICARIA A ESTRUTURA BÁSICA DO DOCUMENTO HTML:

```html
< !DOCTYPE html >

< html lang="en" >

< head >

< meta charset="UTF-8" >

< meta name="viewport" content="width=device-width, initial-scale=1.0" >

< title>Document</title >

< /head >

< body >

< /body >

< /html >
```

-------------------------------------------------------------------------------

## • **Tags Essênciais**

° As tags essenciais do HTML são as tags mais utilizadas no desenvolvimento de um documento

» **Cabeçalhos** ( < h1 > a < h6 >).

° Os cabeçalhos < h1 > a < h6 >) são usados para estruturar o conteúdo de uma página. (< h1 >) é o mais importante e geralmente representa o título principal da página. Os demais são usados para subdividir o conteúdo hierarquicamente.

**° Ex: 

```html
<h1> titulo </h1>

<h2> Subtitulo </h2>
```

#### » **Tag (< hr >):

° A tag **hr** cria uma linha divisória no site **(Arquivo html)** 

**° Ex: 

```html
<hr>
```

» **Parágrafos** (< p >).

° A tag < p > é usada para definir parágrafos de texto. É uma das tags mais comuns para organizar informações escritas em um site.

**° Ex:** 

```html
<p> eu gosto muito de morangos </p>
```

#### » **Âncoras**
° A tag < a > criar links para outras páginas, arquivos ou seções dentro da mesma página. O atributo href define o destino do link. (**UMA DAS PRINCIPAIS TAGS PARA A ORGANIZAÇÃO DO SITE**).

° **Ex:**

```html
**< a href="https://www.exemplo.com">Visite o Exemplo </a >**
```

ou para arquivos dentro do documento:

```html
**< a href=" ./assets/sobre/sobre.html> Sobre </a >**
```

#### » **Observação:**

° Para navegar entre as pastas utilizamos o (../), a quantidade de vezes que utilizamos os dois pontos e a barra depende de onde queremos navegar.

» **Imagem**
° A tag < img > exibe imagens em uma página. O atributo src define o caminho da imagem, e alt fornece uma descrição para a acessibilidade e SEO. (é uma tag de Linha, junto com span.)

° **Ex**:

```html
**< img src=“./img/imagem.png“ alt=“Descrição da imagem.” >**
```

#### » **Listas (< ol >, < li >, < ul >)**

° As tags de listas podem ser ordenadas (< ol >, com número) ou não ordenadas (< ul >,com marcadores). Os item da lista são definidos pela tag **< li  >**.

° **Ex:** **< ul >**
```html
< li > item não ordenado 1< /li >

< li > item não ordenado 2< /li >

**< /ul >**

**< ol >**

< li > item ordenado 1< /li >

< li > item ordenado 2< /li >

**< /ol >**
```

#### » **Tabelas** **(< table >, < tr >, < td >, < th >)**

° A tag < table > cria tabelas. < tr > define uma linha, < th > representa células de cabeçalho e < td > define células de dados.

° **Ex:** < table >

```html
< tr >

< th nome </ th >

< th Idade </ th >

< /tr >

< tr >

< th André </ th >

< th 21 </ th >

< /tr >

< /table >
```

#### » **Formulários() **

° A tag < form > define um formulário para entrada de dados. < input > permite inserir informações, < label >
associa um rótulo ao campo, < textarea > cria uma área de texto e < button > envia o formulário.

° **Ex:**

```html
< form action="/enviar" method="post" >

< label for="nome" >Nome:< /label >

< input type="text" id="nome" name="nome" >

< label for="mensagem" >Mensagem:< /label >

< textarea id="mensagem" name="mensagem" >< /textarea >

< button type="submit" >Enviar< /button >

< /form >
```

#### • **Divisões e Semântica**

» Essas Tags organizam a estrutura da sua página:

```html
< div > é uma divisão genérica para agrupar elementos.

< span > estiliza trechos de texto inline.

< header > contém o cabeçalho da página ou seção.

< footer > representa o rodapé.

< main > envolve o conteúdo principal.

< section > agrupa conteúdo relacionado.

< article > representa um conteúdo independente.

< nav > contém links de navegação.

< aside > exibe conteúdos laterais.
```

## ° **Atributos Globais**

» **Classes:**

» class:

° Define uma ou mais classes **CSS** para o elemento, permitindo a estilização e manipulação via **java script**

```html
<div class="container"></div>
```

#### » **id:**

° Identificador único para o elemento na página. Usado para estilização específica no CSS e seleção direta no JavaScript.

```html
< h1 id="titulo" >< / h1 >
```

#### » **Estilização:**

 » **style:**

° Aplica estilos CSS diretamente no elemento, mas não é recomendado para grandes projetos (possui uma gama variada do que se pode estilizar como: fonte, tamanho de fonte, cor entre outras.)

```html
< p style="color: red;" >< /p >
```

#### » **Dados extras no html**

° Atributo personalizado para armazenar dados extras no HTML, acessíveis via JavaScript.

```html
< button data-user="JohnDue"> Clique </button >
```

#### » **Meta Tags para SEO:**

» **< meta >**

° Define metadados do documento, como descrição e palavras-chave, ajudando na indexação pelos motores de busca.

```html
<meta name="description" content="Descrição breve da página">
```

**< title >**

° Define o título da página exibido na aba do navegador e nos resultados de pesquisa. Deve ser curto e relevante.

```html
<title >Minha Página Incrível< /title>
```

» **< link >**

° Indica a URL/PATH relativo de um arquivo css, de estilos para ser carregado no documento HTML que estiver carregando a tag.

```html
<link rel=“stylesheet” href=“./css/style.css">
```

° Ou pode indicar URL principal de uma página para evitar conteúdo duplicado nos mecanismos de busca.

```html
<link rel="canonical" href="https://www.exemplo.com/pagina-principal">
```
-------------------------------------------------------------------------------

## • **HTML Semântico e acessibilidaade**

» **ARIA roles, alt, aria-label**

° O HTML semântico melhora a estrutura e a acessibilidade da página. Algumas práticas importantes: Uso de ARIA Roles: Como role="navigation", que informa a leitores de tela a função do elemento. Atributo alt em imagens: Essencial para acessibilidade e SEO, descreve o conteúdo da imagem. Atributo aria-label: Adiciona descrições acessíveis a elementos interativos que não têm texto visível. Essas práticas tornam a navegação mais inclusiva para pessoas com deficiência visual e ajudam motores de busca a entender melhor o conteúdo da página.

° **Ex:**

```html
< nav role="navigation" aria-label="Menu principal" >

< ul>

< li> < a  href = "#home"> Início< /a >< /li >

< li>< a href="#sobre" >Sobre < /a> </li >

< li>< a  href = "#contato ">Contato< /a ></li >

< /ul >

< /nav>

< img src="logo.png" alt="Logotipo da empresa" >

< button aria-label="Fechar janela">X</button >
```
-------------------------------------------------------------------------------

## • **Redimensionar imagens:**

» Existem duas formas de corrigir o tamanho das imagens.

» **Dentro do código**:

° **width** » Modifica as dimensões de largura.

° **height** » Modifica as dimensões de altura.

» **EVITAR** utilizar esses atributos no código, o correto seria separar a personalização pelo **CSS**.

• **Figure e Figcaption**

» Essas tags transformam imagens em semântica e ordenam as legendas de forma correta caso haja separação (visualização em bloco).

° Figure » Onde se coloca a **imagem**.

° Figcaption

° **Ex:**

```html
 <div>

                <figure>

                    <img src="../img/parceiros.jpg" alt="Lorem ipsum" width="10%" >

                    <figcaption>Legenda</figcaption>

                </figure>

  

                <figure>

                    <img src="../img/parceiros.jpg" alt="Lorem ipsum" width="10%" >

                    <figcaption>Legenda</figcaption>

                </figure>

  

                <figure>

                    <img src="../img/parceiros.jpg" alt="Lorem ipsum" width="10%" >

                    <figcaption>Legenda</figcaption>

                </figure>

  

 </div>
```
