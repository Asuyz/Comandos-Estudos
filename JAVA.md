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
```
\b » Backspace
\f » Form Feed
\n » Nova Linha
\r » Retorno
\t » Tabulação 
\ " » Aspas
\ '  » Apostrofo
\ \ » Barra Invertida
```

**Funções matemáticas com java:**

```
Adição » +
Subtração » - 
Multiplicação » *
Divisão » /
Resto da divisão inteira » %
Sinal negativo » - (-x)
Sinal positivo » + (+x)
Incremento unitário » ++ (x++)
Decremento unitário » -- (x--)
```
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
• **ENCAPSULAMENTO**.

° Encapsulamento ou **data hidding** é mais um dos conceitos da programação orientada a objetos. Trata-se de um mecanismo que possibilita restringir o acesso a atributos e métodos. Esses conteúdos encapsulados (privados) podem ser acessados pelo **get** e **set**.

» **Método Get**

° Seu objetivo: Obter (ler) o valor de atributo privado.
» Exemplo: e você tem um atributo `nome`, o método `getNome()` vai retornar o valor dele.

```
public class Pessoa {
    private String nome;

    public String getNome() {
        return nome;
    }
}
```

» **Método Set**

° Seu objetivo: Definir (alterar) o valor de um atributo privado.
» Exemplo: Se quiser mudar o valor de `nome`, você usa `setNome("Novo Nome")`.

```
public class Pessoa {
    private String nome;

    public void setNome(String novoNome) {
        this.nome = novoNome;
    }
}
```

» Usamos os métodos **get e set** para o **encapsulamento** (que se trata da ação de proteger os dados internos da classe). Também para a **validação** (validar valores antes de definir. Ex: não permitir `idade` negativa ) e por ultimo para o **controle** (evitar modificações diretas que podem causar bugs no código).

» Visualização de ambos no código:

```
public void setNomeDoAtributo (tipo_do_atributo nomeDoAtributo) {
	this.nomeDoAtributo = nomeDoAtributo;

}
public tipo_do_atributo getNomeDoAtributo (){
	return nomeDoAtributo;

}
```
• **OPERADORES RELACIONAIS E LÓGICOS**.

» Os operadores relacionais em Java permitem a comparação entre dois valores ou expressões, retornando um resultado logico (verdadeiro ou falso).

» Os operadores lógicos em Java permitem a analise entre os resultados de duas ou mais valores ou expressões.

```
Operadores Relacionais:

° Igual (==)
° Diferente (!=)
° Maior que (>)
° Maior ou igual a (>=)
° Menor (<)
° Menor ou igual a (<=)

Operadores Lógicos:

° E lógico ou AND (&&)
° Ou lógico ou OR (||)
° Negação lógico ou NOT (!)
```

• **ESTRUTURA DE DECISÃO**

° Em Java podemos utilizar a estrutura de decisão **if - else/else if (sem elif como python)** para permitir o programa analisar uma certa condição e escolher  a linha de código que será executada com base no resultado da condição 

° O comando **if - else** funciona da seguinte forma: o programa analisa a condição (parênteses do comando if) e se esta retorna verdadeiro ele executará o bloco de comandos logo abaixo. Caso a condição retorne valor falso, o bloco de comandos a ser executado é o que fica logo abaixo do comando else.

° Sintaxe:

```
if (condicao) {
    // código se a condição for verdadeira
} else if (outraCondicao) {
    // código se a outra condição for verdadeira
} else {
    // código se nenhuma das condições acima for verdadeira
}
```

° Exemplo com valores:

```
int idade = 18;

if (idade < 18) {
    System.out.println("Menor de idade");
} else if (idade == 18) {
    System.out.println("Tem exatamente 18 anos");
} else {
    System.out.println("Maior de idade");
}
```

° **PONTOS IMPORTANTES DO IF-ELSE:**

» As condições vão entre **parênteses `( )`**.

» Os blocos de código vão entre **chaves `{ }`**.

» Pode comparar com `==`, `!=`, `<`, `>`, `<=`, `>=`. (Operadores Relacionais)

» Para condições compostas, dá pra usar `&&` (E) e `||` (OU). (Operadores Lógicos)

• **TRY - CATCH**

° Quando executamos códigos em Java, diversos erros podem acontecer: erros de codificação por parte do programador, erros devidos a entrada de valores incorretos entre outras possibilidades. Quando erros ocorrem o Java normalmente irá interromper a execução do programa e exibir alguma mensagem de erro. O termo técnico para isso é: o Java irá “jogar uma exceção” (throw an exception).

° O comando **try** permite definir um bloco de comandos que terá o proposito de buscar erros enquanto o programa testado é executado.

° O comando catch permite definir um bloco de comandos a ser executado quando um erro é encontrado. O comando try e catch “andam sempre juntos”.

° Ambos os comandos "andam juntos"

» Sintaxe:

```
try {
    // código que pode lançar uma exceção
} catch (TipoDaExcecao nomeVariavel) {
    // tratamento da exceção
}
```

° Exemplo com valores:

```
public class ExemploTryCatch {
    public static void main(String[] args) {
        try {
            int resultado = 10 / 0; // isso vai causar uma exceção
            System.out.println("Resultado: " + resultado);
        } catch (ArithmeticException e) {
            System.out.println("Erro: divisão por zero!");
        }
    }
}
```

° **ALGUNS PONTOS DO TRY - CATCH:**

» O código dentro do `try` é **tentado**.

» Se der erro, o `catch` **captura** a exceção e executa o que estiver dentro dele.

» Você pode usar vários `catch` se quiser tratar tipos diferentes de erro.

» Dá pra usar `finally {}` se quiser um bloco que **sempre execute**, com ou sem erro (opcional).


°»


