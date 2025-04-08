• **Cascading Style Sheets  (CSS)*

-------------------------------------------------------------------------------

•  **IMPORTANTE SEMPRE ZERAR OS VALORES DE CSS DO NAVEGADOR**

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

» **O ( * ) é o seletor global**.

**• Ou:**

```
<link rel="stylesheet" href="https://necolas.github.io/normalize.css/8.0.1/normalize.css">
```

» Normalize.css, que **não zera**, mas **uniformiza o estilo entre os navegadores**.

-------------------------------------------------------------------------------

**» Css é a parte de apresentação de aplicações (visual).**

° Para o desenvolvimento de aplicações em **HTML e CSS3** utilizamos os sites **W3C e MDM** para consulta de informações envolvendo ambas.

° Para a validação de arquivos utilizamos o site do **W3C** (Validator W3C) conforme os padrões para a criação e a interpretação de conteúdos para a Web.

• **3 Tipos de CSS**:

° Inline.

° Interno.

° Externo.

» Inline:

° As modificações de estilo (cor, tamanho de fonte, entre outras) é realizada no meio da estrutura do HTML (nas tags). (NÃO UTILIZAR)

» Interno:

° Aplica as modificações dentro da tag **< head >>**. (Evite utilizar).

» Externo:

° Cria uma parte externa para a aplicação do CSS, deixando o código mais limpo e podendo realizar mudanças no design de forma mais efetiva.

° Todas as tags são **SELETORES** e podem ser usadas com exceção das:

» Head.

» Meta.

» Title.

» Link.

» Style.

° Para o apontamento de arquivos, é preciso direcionar com: **(./) ou (../)**.

• **Regra para a personalização do CSS**

° Para personalizar os elementos do **HTML**  com o **CSS** devemos seguir esse padrão:

```
p {color #f00; font-size :20px}

° P - é o seletor (tag).
° Seguido do seletor devemos passar as propriedades (as propriedades são o color e o font-size nesse exemplo e em seguidas os valores {#f00 e 2opx}).
° Aqui podemos usar qualquer seletor menos os citados acima.
```

° Para usar os **IDS** no **CSS**:

```
#(id escolhido){

}

Ex:

#titulo{
font-size:20px
color: rgb 255,255,255
}
```

• **Propriedade Shorthand**

° É uma forma de escrever várias propriedades CSS **em uma única linha**.

° Ao invés de escrever várias regras separadas, você usa **uma linha compacta** pra economizar código e deixar mais limpo.

```
/* Forma longa (longhand) */
margin-top: 10px;
margin-right: 20px;
margin-bottom: 10px;
margin-left: 20px;

/* Forma abreviada (shorthand) */
margin: 10px 20px;
Onde o primeiro valor representa o eixo Y e o segundo o eixo X.
```

• **Class**:

° Uma **classe** em CSS é uma forma de dar estilo a elementos HTML.  
Você declara ela no CSS com um `.` (ponto), e no HTML você usa `class="nome-da-classe"`.

° **Exemplo de uso de classe:**

```
<a href="#home" class="nav-link">Home</a>
    <a href="#sobre" class="nav-link">Sobre</a>
    <a href="#servicos" class="nav-link">Serviços</a>
    <a href="#contato" class="nav-link">Contato</a>
```



•°»
