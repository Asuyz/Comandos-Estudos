## • **Sobre** 🦀  ->

° Rust é uma linguagem compilada com foco em oferecer segurança de memória, velocidade e concorrência de segura (permite múltiplas threads sem riscos) sem utilizar o **garbage** colector.

° Por ser uma linguagem compilada sem código é convertido em binário, o que garante uma execução rápida. (Como no C/C++)

° Para a compilação utilizamos ou **rustc**, seu ecossistema conta com o gerenciador de pacotes **Cargo** (como se fosse um **apt**,**dnf** ou **xbps**).

° Seus usos comuns são: OS (sistemas operacionais), games, servidores, ferramentas CLI, engines e até WebAssembly.

° Para comentar alguma linha ou adicionar comentários em Rust utilizamos: **//**.
## • **Tipos primitivos em Rust:**

| Tipo                      | Descrição                                 | Tamanho (bytes)    | Exemplo                                     |
| ------------------------- | ----------------------------------------- | ------------------ | ------------------------------------------- |
| **array**                 | Sequência de tamanho fixo `[T; N]`.       | Depende de `T × N` | `let nums: [i32; 3] = [1, 2, 3];`           |
| **bool**                  | Valor booleano (`true` / `false`).        | 1                  | `let ativo: bool = true;`                   |
| **char**                  | Caractere Unicode.                        | 4                  | `let letra: char = '🚀';`                   |
| **f32**                   | Ponto flutuante de 32 bits.               | 4                  | `let preco: f32 = 19.99;`                   |
| **f64**                   | Ponto flutuante de 64 bits (padrão).      | 8                  | `let pi: f64 = 3.1415;`                     |
| **fn**                    | Ponteiro para função.                     | 8 (em 64-bit)      | `fn dobro(x: i32) -> i32 { x * 2 }`         |
| **i8**                    | Inteiro com sinal de 8 bits.              | 1                  | `let n: i8 = -5;`                           |
| **i16**                   | Inteiro com sinal de 16 bits.             | 2                  | `let n: i16 = 32000;`                       |
| **i32**                   | Inteiro com sinal de 32 bits.             | 4                  | `let n: i32 = 100000;`                      |
| **i64**                   | Inteiro com sinal de 64 bits.             | 8                  | `let n: i64 = 9_000_000_000;`               |
| **i128**                  | Inteiro com sinal de 128 bits.            | 16                 | `let n: i128 = 12345678901234567890;`       |
| **isize**                 | Inteiro com sinal do tamanho do ponteiro. | 4 ou 8             | `let n: isize = -3;`                        |
| **u8**                    | Inteiro sem sinal de 8 bits.              | 1                  | `let n: u8 = 255;`                          |
| **u16**                   | Inteiro sem sinal de 16 bits.             | 2                  | `let n: u16 = 60000;`                       |
| **u32**                   | Inteiro sem sinal de 32 bits.             | 4                  | `let n: u32 = 4_000_000_000;`               |
| **u64**                   | Inteiro sem sinal de 64 bits.             | 8                  | `let n: u64 = 1_000_000_000_000;`           |
| **u128**                  | Inteiro sem sinal de 128 bits.            | 16                 | `let n: u128 = 10_000_000_000_000_000_000;` |
| **usize**                 | Inteiro sem sinal do tamanho do ponteiro. | 4 ou 8             | `let n: usize = 42;`                        |
| **pointer**               | Ponteiro cru (`*const`, `*mut`).          | 4 ou 8             | `let ptr: *const i32 = &10;`                |
| **reference**             | Referência segura (`&T`, `&mut T`).       | 4 ou 8             | `let x = 10; let r = &x;`                   |
| **slice**                 | Vista dinâmica de uma sequência `[T]`.    | 16                 | `let s = &arr[0..2];`                       |
| **str**                   | Fatia de string (`&str`).                 | 16                 | `let nome: &str = "Rust";`                  |
| **tuple**                 | Sequência heterogênea `(T1, T2, ..)`.     | Soma dos campos    | `let t = (42, 3.14, 'R');`                  |
| **unit**                  | Tipo vazio `()`.                          | 0                  | `let v = ();`                               |
| **f16** *(experimental)*  | Ponto flutuante de 16 bits.               | 2                  | *(não estável)*                             |
| **f128** *(experimental)* | Ponto flutuante de 128 bits.              | 16                 | *(não estável)*                             |
| **never (`!`)**           | Tipo que nunca retorna.                   | 0                  | `fn erro() -> ! { panic!("erro!"); }`       |

### ° **Tipos e variáveis** 

° Para declaramos uma variável no Rust utilizamos a palavra **let + (nome da variável)**. 

° Por padrão as variáveis serão sempre **imutáveis** (não confundir com constantes) e para podermos modificar seus valores utilizamos: **mut**.

### » **Exemplos**:

```Rust

Let variavel : i8 = 127
//I8 = Inteiro de 8 bits (Intervalo de -128 ate 127)
//Depois dos : definimos o tipo (bool, array, etc;)

Let mut variavel 2 : u8 = 255
//U8 = unsigned de 8 bits (bytes) (intervalo de 0 ate 255)
//mut permite que modifiquemos o valor da variavel no futuro.

//Exemplo de print:

println!("variavel = {}", variavel)
//No print é necessário passar o parâmetro no fim para exibir o valor)

```

------------------------------------------------------------

## ° **Constantes**

° A diferença entre **constantes e variáveis** é:

» Variável tem um endereço de memória alocado onde um valor foi adicionado.

» **Constantes** não armazenam valor em memória e são executadas em tempo de **compilação (rustc) e não em tempo de execução**.

° São declaradas com **const** e **não podem ser mutáveis**.

° Precisamos indicar sempre o tipo (não é subentendido igual nas variáveis onde é possível em alguns casos omitir).

° As constantes podem ser utilizadas em qualquer lugar do código, inclusive fora da função **main**.

### » **Exemplo**:

```Rust

Const PI: f64 = 3.14159;
// f64 = Ponto flutuante de 64 bits
fn main(){
	println!("O valor de PI é: {}", PI);
}

```

------------------------------------------------------------

## ° **Recursos Específicos e Gerais**

» **Escopo** -> Valores fora do bloco de código não existem em outro.

» No rust é possivelmente redeclarar variáveis de forma fácil.
Exemplo:

```Rust
//
Let Var:F32 = 2.5 // Esse valor é descartado
Let Var:F32 = 2.6 // Esse valor é o novo valor da variavel

// Quando compilarmos o código o valor de 2.6 será exibido.
```

° Um escopo dentro do outro **herda** o valor do escopo externo, esse conceito se chama **shadowing**

## ° **Funções**

» Se não especificamos o retorno de uma **FN** ela não retorna nada, não é possível **omitir** o seu retorno

° **Exemplo de FN com retorno:**

```Rust
Fn soma (a:i32,b:i32) -> i32 // a arrow function (->) é o nosso retorno
```

» Quando queremos **retornar** algo no Rust a nossa expressão **não terá o ponto e virgula em seu final (;)**, esse conceito se chama de **supressed (supressão)**.


## ° **Expressão if**

» O comportamento funciona da mesma forma das outras linguagens (**if -> if/else -> else**).

» O Rust pode ler valores como expressão então no lugar de **if/else** podemos usar:

```Rust
let condicao = if idade >18{maior}else{menor};
// depois do = o valor dentro vira a condição do if/else
```

» O valor de diferente em Rust é representando dessa maneira: **!=**

## ° **Loops**

» Laços de repetição (loops) funcionam quase da mesma forma de qualquer outra linguagem.

» **While**: Lê a condição no **inicio**.

» **Do While (em Rust)**: Lê ao final (loop com instrução **break**).

» **Continue** faz seu loop ler outro bloco antes de voltar ao principal.

» **Range e for** no Rust percorrem em intervalos:

```Rust
For i in 1..11 
For i in 1.. =10

```

» No primeiro exemplo do **for i** o índice não percorre até o final ele sempre ira parar 1 valor antes do determinado (igual o segundo exemplo, porém a forma de escrita fica mais clara).

## ° **Match Statement**

» Se trata de uma estrutura de **controle** presente no Rust (não sendo comum em outras linguagens), onde o fluxo de execução é determinado por correspondência de padrões (_pattern matching_), permitindo tratar múltiplos casos de forma segura, expressiva e exaustiva.

° **Exemplo:**

```Rust
Let result = match numero{
1=>"um"
2=>"dois"
_=>"outro"}
```



•°»