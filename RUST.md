## • **Sobre** 🦀  ->

° Rust é uma linguagem compilada com foco em oferecer segurança de memória, velocidade e concorrência de segura (permite múltiplas threads sem riscos) sem utilizar o **garbage** colector.

° Por ser uma linguagem compilada sem código é convertido em binário, o que garante uma execução rápida. (Como no C/C++)

° Para a compilação utilizamos ou **rustc**, seu ecossistema conta com o gerenciador de pacotes **Cargo** (como se fosse um **apt**,**dnf** ou **xbps**).

° Seus usos comuns são: OS (sistemas operacionais), games, servidores, ferramentas CLI, engines e até WebAssembly.

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

(*Conteúdo ainda será passado*)


•°»