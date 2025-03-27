• **Domain Design Driven Using Java**

° **Programação orientada a objetos** »  Identificar os objetos e destrincha-las podendo utilizar a abstração como um dos meios(imaginar as propriedades do objetos. Ex: Navio {Tripulação, Carga, Capacidade). Abstração pode ser correta dependendo da sua ***aplicação.**

° **Encapsulamento** » é um princípio de design de código, geralmente ligado a **programação** orientada, que nos orienta a esconder as funcionalidades e funcionamento do nosso código dentro de pequenas unidades (normalmente métodos e funções).

° **Modularidade** » Consiste em método de design onde as linhas de código são formadas por módulos independentes e intercambiáveis.
° Reutilização de códigos (nesse caso .js) já realizados para projetos diferentes .

° **Classes e Objetos**  » classe é um rascunho de como o objeto será realizado  {Toda Classe tem atributos e métodos.} Ex: Classe » {+Tamanho: Type/ +Cor: Type} = **Atributos** /  {Latir(Type):Type/ MoverCauda(type):Type} = **Métodos** 
⌞ Herança é a técnica que permite a criação de classes a partir de outras classes reaproveitando atributos e métodos.

° **Hierarquia** » é a classificação de tipos de objetos , denotando objetos como instanciações de classes.

° **Polimorfismo** » É a capacidade de tratar **Objetos** de classes diferentes de forma uniforme. 
⌞ Tipos de **Polimorfismo**:
» **Sobrecarga** » ocorre quando uma classe possui vários métodos com o mesmo nome, mas com parâmetros diferentes.

» **Sobrescrita** » ocorre quando uma classe filha redefine um método da classe pai, implementando um comportamento específico para aquela classe.

--------------------------------------------------------------------
° **Tipos de variáveis em Java**
    ⌞ Java é uma linguagem fortemente tipada.

° Variáveis ficam armazenadas na memória primaria (memória ram).
⌞ Tipos de variáveis **primitivas:
     ─ Char = 16 Bits
     ─ Byte = 8 Bits
     ─ Int = 32 Bits 
     ─ Short = 16 Bits
     ─ Long =  64 Bits
     ─ Float = 32 Bits
     ─ Double = 64 Bits
     ─ Boolean = 8 Bits (True or False)**
⌞ Tipos de variaveis não **primitivas:
     ─ String = O número de bits dependera da sua extensão (Cadeira de caracteres use aspas dentro do parênteses )**.
⌞ As variáveis **BYTE, INT, SHORT E LONG SÃO UTILIZADAS PARA NÚMEROS INTEIROS, SUA DISTINÇÃO ENTRE ELES É A SUA QUANTIDADE DE ARMAZENTAMENTO (QUANTO MAIS BITS MAIOR SUA CAPACIDADE).**

⌞ As variáveis **FLOAT E DOUBLE SÃO UTILIZADAS PARA NÚMERO REAIS.

⌞ E a variável **BOOLEAN É UTILIZADA PARA VERDADEIRO OU FALSO (TIPO LÓGICO).

» Toda Classe Primitiva tem uma Classe não primitiva **Oposta**.

° **Sequência de Escape (Caracteres  Especiais):**

\b » Backspace
\f » Form Feed
\n » Nova Linha
\r » Retorno
\t » Tabulação 
\ " » Aspas
\ '  » Apostrofo
\ \ » Barra Invertida

° **Funções matemáticas com java:**

Adição » +
Subtração » - 
Multiplicação » *
Divisão » /
Resto da divisão inteira » %
Sinal negativo » - (-x)
Sinal positivo » + (+x)
Incremento unitário » ++ (x++)
Decremento unitário » -- (x--)

--------------------------------------------------------------------

° **INTELLIJ - Plataforma para a programação em Java utilizada.** 

» Utilizamos a ultima versão estável do **java** (Versão 21).

» Não escrevemos a linha de código completa programando em java e sim completamos a linha com o **TAB**.

-------------------------------------------------------------------------------

• **CLASSES EM JAVA**

° Classe é um molde, ao se definir uma classe podem ser criados **diversos** objetos a partir dela

» Uma classe é composta por seu **Nome, seus atributos e métodos**
° Nomes de classes se iniciam com letra maiúscula e cada nova primeira palavra se usa também letra maiúscula
° Nomes de atributos e dos métodos se iniciam com letra minúscula e cada nova palavra a primeira letra é maiúscula.

° **Modificador**
» Indica o modo de acesso por outras classes, define a sua **visibilidade**.

° Para **Classes**:
° **Public** » a classe pode ser acessada por qualquer outra rede.
° **Default** » a classe pode ser acessada por outras classes no mesmo pacote, esse modificador é utilizado quando não se especifica um modificador. 

° **Para atributos e métodos**:
° **Public** ( No diagrama o public é representado por um +).
° **Private** » Só pode ser acessado pela pessoa que a criou. (Representado por um - no diagrama).
° **Default**
° **Protected*** » O código somente é acessado no mesmo pacote e por subclasses. (Representado por um # no diagrama).

° Os tipos de **atributos e métodos** são os mesmos das **variáveis**.
» Atributo faz parte da classe (se comporta como uma variável).

• **Métodos** (Pode ser considerado um mini programa).
» É um bloco de código que só é executado quando é chamado (usado).

° Podemos ter métodos onde é possível passar dados (valores), chamado de parâmetros (passagem dos parâmetros são opcionais).
» Utilizamos métodos para **reutilizar** códigos (definir o código apenas uma vez e usa-lo diversas vezes).

° **Tipos de métodos**

° Métodos com **retorno**
» Retorna a informação digitada (Geralmente atribuída a alguma variável), e o programa principal continua. 

° Métodos sem **retorno**
» Não retorna o valor, apenas sinaliza e o programa continua.

• **SINTAXE DE UM MÉTODOS**

° **Com retorno**
» **modificador** **tipo** nomeDoMetodo (lista-de-parâmetros (opcional)) { 
código do corpo

**return** valor-de-retorno (tem que ser o mesmo valor do mesmo **TIPO**)

}

° **Sem retorno**

» **modificador** **void** nomeDoMetodo (lista-de-parâmetros) { 

código do corpo
}
 
-------------------------------------------------------------------------------


°»


