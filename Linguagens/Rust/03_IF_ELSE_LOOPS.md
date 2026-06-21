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
