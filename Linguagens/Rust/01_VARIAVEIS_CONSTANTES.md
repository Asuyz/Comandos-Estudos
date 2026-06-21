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
