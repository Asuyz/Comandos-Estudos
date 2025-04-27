• **COMPUTACIONAL THINKING USING PYTHON**

° Finalidade dessa matéria é desenvolver o pensamento computacional (logica funcional base para outras linguagens) usando Python.

° Desenvolvimento de algoritmos (Serie de passos **FINITOS** para a resolução de um problema).

» Uma linguagem de programação é utilizada para a comunicação entre o alto nível e o baixo nível (binário).

» É a Ferramenta para moldar o computador para nossas necessidades.

--------------------------------------------------------------------------------

• **Entrada e  Saída de Dados**

° **Entrada**: Usamos a função `input()` para receber dados do usuário.  

° **Saída**: Usamos a função `print()` para exibir mensagens na tela. 

```
nome = input("Digite seu nome: ")
#Entrada de dados

print("Olá,", nome)
#Saida de dados
```
---

•  **Variáveis: Criação e Modificação**

° **Criar uma variável** é só **atribuir** um valor a ela.  

° **Modificar** é **atribuir um novo valor**.

``` 
#Criação de variáveis

idade = 20
cidade = "São Paulo"

#Modificação de variáveis

idade = idade + 1  # agora idade vale 21
cidade = "Rio de Janeiro"  # mudando o valor de cidade

print("Idade:", idade)
print("Cidade:", cidade)

```

---

•  **Execução Condicional: `if`, `else`**

° Permite **executar diferentes blocos de código** dependendo de uma condição verdadeira ou falsa.

```
#Execução condicional
nota = float(input("Digite sua nota: "))

if nota >= 7:
    print("Aprovado!")
else:
    print("Reprovado.")
```

° Se a nota for maior ou igual a 7 → imprime "Aprovado!"

° Se for menor → imprime "Reprovado."

---

•  **Resumo Rápido em Tabela**:

| Conceito            | Função usada / Exemplo       |
| ------------------- | ---------------------------- |
| Entrada de dados    | `input()`                    |
| Saída de dados      | `print()`                    |
| Criar variáveis     | `nome = "Maria"`             |
| Modificar variáveis | `idade = idade + 1`          |
| Condicional simples | `if condição: ... else: ...` |

---

• **Execução com repetição (While)**

° While é o comando que mantém o código rodando enquanto uma condição estabelecida estiver sendo atendida.

» Exemplo:

```
print ("oi tudo bem? (S/N)")
resposta = input()

while resposta == "S"
	print ("Bom dia")
	print ("Deseja ver a mensagem novamente?")
	resposta = input().upper

if reposta == "N"
	print("tchau)
```

» O uso **"padrão"** do while vem da seguinte forma:

° 1 - Inicialização da variável.

° 2 - While (Condição envolvendo a variável).

» Tarefa envolvendo a variável.

» Atualização da variável.  

° A atualização da logica da variável fica no fim do código isso deixa a logica mais simples e limpa.

 • **COMO SAIR DO `while`**

° Se a variável não for atualizada dentro do `while`, o código ficará preso em um **loop infinito**, repetindo para sempre.

» **Exemplo de loop infinito:**

```
while True:
    print("Isso nunca vai parar sozinho!")
```

° O `while True:` é uma condição que **sempre será verdadeira**, gerando um loop eterno até ser interrompido manualmente.

° Em resumo utilizamos o `while` quando **não sabemos quantas vezes** o bloco de código precisa ser repetido. A repetição continua **enquanto a condição for verdadeira**.



»°•
