
**•  Introdução do Figma**

» Figma é uma plataforma para construção de interfaces e protótipos. Com essa ferramenta podemos construir o design de produtos digitais (sites e aplicativos de dispositivos móveis) ou até para pequenas telas.

» Trabalhamos com Frame Works (que são resoluções do dispositivo(s) que queremos trabalhar).

**° Sobre os botões do software:**

**° Barra Superior:**

» Menu Principal (Figma logo): Acesso a arquivos, configurações, preferências e plugins.

» Nome do Arquivo/Projeto: Mostrado ao centro.

» Botões de Compartilhar, Apresentar e Comentários: À direita, facilitam colaboração.

**° Painel Lateral Esquerdo:**

» Camadas (Layers): Lista todos os elementos visuais da sua tela.

» Assets: Componentes reutilizáveis (botões, ícones, etc.).

» Páginas: Organização do seu projeto em múltiplas páginas.

**° Tela de Trabalho (Canvas)**:

» Área principal onde você desenha e organiza seus frames (telas, artboards).

» Suporta múltiplos frames e protótipos lado a lado.

**° Painel Lateral Direito**

» Design: Ajustes visuais como cores, tipografia, tamanhos, sombras, bordas.

» Prototype: Configurações de interação (links entre telas, transições).

» Inspect: Informações para desenvolvedores (códigos CSS, medidas, cores).

**° Barra de Ferramentas (Topo da Tela de Trabalho)**

» Ferramentas básicas de desenho e manipulação:

» Move/Select: Mover e selecionar elementos.

» Frame: Criar telas/artboards.

» Shapes: Formas geométricas.

» Text: Inserção de texto.

» Hand: Navegar pela tela.

» Comment: Inserir comentários.

-------------------------------------------------------------------------------

**• Formas geométricas no Figma:** 

° **Retângulo**: Pode ter bordas arredondadas ajustadas no painel de design.

° **Linha**: A forma mais simples, sem preenchimento, apenas com borda (_stroke_).

° **Flecha**: Semelhante à linha, mas com uma ponta específica.

° **Polígono**: Começa como um triângulo, e podemos ajustar a quantidade de lados.

° **Estrela**: Permite controlar a quantidade de pontas e espessura.

° **Imagem**: Insere uma imagem em um retângulo, que pode ser redimensionado.

-----------------------------------------------

° **Alinhamento do Texto**

° Selecione a caixa de texto e, na barra lateral direita (painel de propriedades):

° Esquerda (Left Align): padrão.

° Centro (Center Align): centraliza o texto na caixa.

° Direita (Right Align).

° Justificado (Justify Text): 🔸 Figma NÃO oferece 
justificação nativa. Mas você pode simular justificado ajustando manualmente a largura da caixa de texto e usando espaçamento entre palavras.

° Com o plugin **Justify Text** para forçar justificação.

° **Sublinhado e Tachado (Strikethrough)**

° Selecione o texto > no painel direito, clique no ícone de sublinhado (U) ou tachado (S riscado).

° **Também pode usar os atalhos:**

° Ctrl + U para sublinhar

° Ctrl + Shift + X para tachado

° **Espaçamento de Texto**

° Letter spacing (Espaçamento entre caracteres):

° Ajusta o espaço horizontal entre letras.

° Line height (Altura da linha):

° Define o espaçamento vertical entre linhas de texto.

° Paragraph spacing (Espaçamento entre parágrafos):

° Clique no ícone “…” (Mais opções) dentro da seção de texto para ativar espaçamento entre parágrafos.

° **Listas Numeradas e Marcadores**

° O Figma não possui listas automáticas, mas você pode criar manualmente:

° Use • (Alt+7 no teclado numérico) para listas com marcadores.

° Ou digite números manualmente (1., 2., etc).

**O plugin "Bullets" automatiza isso e gera listas reais no Figma**:

° **Reticências / Texto cortado com "..."**

° Para mostrar "…" quando o texto ultrapassa a caixa:

° No painel direito, ative a opção "Truncation / Text overflow" com reticências (…).

° Também pode usar a configuração “Auto Width / Auto Height / Fixed Size” para controlar o comportamento da caixa de texto.

• **RESUMO DAS FUNCIONALIDADES:**

| --Função--              | --Onde encontrar--        |
| ----------------------- | ------------------------- |
| Fonte, tamanho, peso    | Painel direito (Text)     |
| Sublinhado              | Ícones no painel Text     |
| Espaçamento de letras   | “Letter spacing”          |
| Espaçamento de linhas   | “Line height”             |
| Espaço entre parágrafos | Menu “…” no Text          |
| Reticências (ellipsis)  | Comportamento do text box |
| Listas                  | Manualmente ou com plugin |

------------------------------------------------------------------------------
 • **GRUPOS E FRAMES: **
 
» Os grupos no Figma servem para **organizar elementos juntos** em um único bloco. Quando você agrupa objetos (textos, formas, ícones), eles passam a se mover, redimensionar e alinhar como uma unidade.

» **CRIAÇÃO DE GRUPOS:**
 
° Pressione `Ctrl + G` (Windows) ou `Cmd + G` (Mac). Ou clique com o botão direito e escolha 
**"Group Selection"**.

» **PARA DESAGRUPAR**:

° Selecione o grupo e pressione `Shift + Ctrl + G` (Windows) ou `Shift + Cmd + G` (Mac).

° Pressione `Ctrl + G` (Windows) ou `Cmd + G` (Mac). Ou clique com o botão direito e escolha 
Ou clique com o botão direito > **"Ungroup"**.

» **DIFERENÇAS ENTRE GRUPOS E FRAMES:**

|Recurso|Group|Frame|
|---|---|---|
|Organização|Agrupa elementos|Contêiner real (como uma “div” no HTML)|
|Layouts|Não suporta auto layout|Suporta Auto Layout, grids, constraints|
|Recursos|Básico, leve|Robusto e versátil|
|Uso ideal|Agrupamento rápido e simples|Estruturação, layout, responsividade|

•°»