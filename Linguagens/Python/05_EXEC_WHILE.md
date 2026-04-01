## • **Execução com repetição (While)**

° **While** é o comando que mantém o código rodando enquanto uma condição estabelecida estiver sendo atendida.

» Exemplo:

```python
print ("oi tudo bem? (S/N)")
resposta = input()

while resposta == "S"
	print ("Bom dia")
	print ("Deseja ver a mensagem novamente?")
	resposta = input().upper

if reposta == "N"
	print("tchau)
```

» O uso **“padrão”** do `while` consiste em **inicializar uma variável, criar uma condição no `while` baseada nela, executar uma tarefa dentro do bloco e, ao final, atualizar essa variável**, mantendo a lógica mais simples e organizada.

 • **COMO SAIR DO `while`**

° Se a variável não for atualizada dentro do `while`, o código ficará preso em um **loop infinito**, repetindo para sempre.

#### » **Exemplo de loop infinito:**

```python
while True:
    print("Isso nunca vai parar sozinho!")
```

° O `while True:` é uma condição que **sempre será verdadeira**, gerando um loop eterno até ser interrompido manualmente.

° Em resumo utilizamos o `while` quando **não sabemos quantas vezes** o bloco de código precisa ser repetido. A repetição continua **enquanto a condição for verdadeira**.