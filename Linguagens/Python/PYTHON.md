## • **COMPUTACIONAL THINKING USING PYTHON**

° Finalidade dessa matéria é desenvolver o pensamento computacional (logica funcional base para outras linguagens) usando Python.

° Desenvolvimento de algoritmos (Serie de passos **FINITOS** para a resolução de um problema).

» Uma linguagem de programação é utilizada para a comunicação entre o alto nível e o baixo nível (binário).

» É a Ferramenta para moldar o computador para nossas necessidades.

--------------------------------------------------------------------------------

## • **Entrada e  Saída de Dados**

° **Entrada**: Usamos a função `input()` para receber dados do usuário.  

° **Saída**: Usamos a função `print()` para exibir mensagens na tela. 

```python
nome = input("Digite seu nome: ")
#Entrada de dados

print("Olá,", nome)
#Saida de dados
```
---

## •  **Variáveis: Criação e Modificação**

° **Criar uma variável** é só **atribuir** um valor a ela.  

° **Modificar** é **atribuir um novo valor**.

```python
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

## •  **Execução Condicional: `if`, `else`**

° Permite **executar diferentes blocos de código** dependendo de uma condição verdadeira ou falsa.

```python
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

## •  **Resumo Rápido em Tabela**:

| Conceito            | Função usada / Exemplo       |
| ------------------- | ---------------------------- |
| Entrada de dados    | `input()`                    |
| Saída de dados      | `print()`                    |
| Criar variáveis     | `nome = "Maria"`             |
| Modificar variáveis | `idade = idade + 1`          |
| Condicional simples | `if condição: ... else: ...` |

---

## • **Execução com repetição (While)**

° While é o comando que mantém o código rodando enquanto uma condição estabelecida estiver sendo atendida.

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

» O uso **"padrão"** do while vem da seguinte forma:

° 1 - Inicialização da variável.

° 2 - While (Condição envolvendo a variável).

» Tarefa envolvendo a variável.

» Atualização da variável.  

° A atualização da logica da variável fica no fim do código isso deixa a logica mais simples e limpa.

 • **COMO SAIR DO `while`**

° Se a variável não for atualizada dentro do `while`, o código ficará preso em um **loop infinito**, repetindo para sempre.

#### » **Exemplo de loop infinito:**

```python
while True:
    print("Isso nunca vai parar sozinho!")
```

° O `while True:` é uma condição que **sempre será verdadeira**, gerando um loop eterno até ser interrompido manualmente.

° Em resumo utilizamos o `while` quando **não sabemos quantas vezes** o bloco de código precisa ser repetido. A repetição continua **enquanto a condição for verdadeira**.

--------------------------------------

## » **Funções**

° Funções são blocos de código que executam tarefas especificas. As funções ajudam a **organizar, reutilizar e evitar repetição no código**. Em Python podemos utilizar funções já prontas (como `print()` e `len()`) ou criar com a palavra chave ```def.```

° Por exemplo, se precisarmos somar dois números em diversos pontos no nosso código podemos, é preferível criarmos a função `somar()` para evitar a repetição.

#### ° **Exemplos:**

```python

## Sintaxe Básica ##

def saudacao(nome):
	print(f"oi,{nome}!")

## Chamando a funcao ##

saudacao("Andre")

## Com Retorno: ##

def somar(a, b):
    return a + b

resultado = somar(3, 5)
print(resultado)  # 8

## Argumento com valor Padrao ##

def boas_vindas(nome="Visitante")
	print(f"Bem-vindo, {nome}!")

boas_vindas() ##Bem-vindo, Visitante!
boas_vindas(Lara) ##Bem-vindo, Lara!


```

-----------------------------------

## ° **Listas e Sequências**

° Listas são **estruturas que armazenam coleções de dados**. São usadas quando você precisa guardar vários valores em uma única variável, como uma lista de nomes, números ou itens.

° Existem **diferentes** tipos:

° `list`: mutável e ordenada.
 
° `tuple`: imutável e ordenada.

° `set`: mutável e **não ordenada**, sem itens repetidos.

° `str`: também é uma sequência (de caracteres).

° Essas sequências permitem acessar itens por índice, percorrer com `for`, usar fatias (`slicing`), verificar se um item está presente (`in`) e muito mais.

° Vale lembrar que a leitura da lista começa com **ZERO**. 

#### ° **Exemplos:**

```python

## Coleção Ordenada de mutável de itens (LISTA) ##

frutas = ["maçã", "banana", "uva"]
print(frutas[1])  # banana

frutas.append("laranja")
print(frutas)  # ["maçã", "banana", "uva", "laranja"]

## Coleção ordenada IMUTAVEL (TUPLA) ##

cores = ("vermelho", "verde", "azul")
print(cores[0])  # vermelho

## Coleção não ordenada e sem duplicatas (SET) ##

numeros = {1, 2, 3, 2}
print(numeros)  # {1, 2, 3}

## Fatiamento e Loops ##

lista = [10, 20, 30, 40, 50]
print(lista[1:4])  # [20, 30, 40]

for item in lista:
    print(item)

```

--------------------------------

## ° **Dicionários**

° Dicionários (`dict`) são **coleções de pares chave:valor**. Eles funcionam como um armário onde você guarda algo e identifica cada compartimento por uma “chave”. São **não ordenados** (até o Python 3.6) e muito usados para representar objetos com propriedades.

° Dicionários são ideais quando você precisa **relacionar nomes a valores**, como IDs a nomes, produtos a preços, usuários a senhas, etc.

#### ° **Exemplo:** 

```python

##Estrutura: Chave → valor

aluno = {"nome": "Lucas", "idade": 20}
print(aluno["nome"])  # Lucas

# Adicionar
aluno["curso"] = "Python"

##Iterar:##

for chave, valor in aluno.items():
    print(chave, "=>", valor)
```

---------------------------

## ° **Input e Output**

É a **interação com o usuário**. "Input" (entrada) serve para capturar o que o usuário digita no teclado. "Output" (saída) serve para mostrar informações na tela.

#### ° **Entrada com** `input()`:

Recebe um valor digitado pelo usuário e **sempre retorna uma string** (texto). Se quiser um número, você precisa converter com `int()` ou `float()`.

`idade = int(input("Digite sua idade: "))`

#### ° **Saída com** `print()`:

Exibe uma ou mais informações no terminal. Pode usar vírgulas, f-strings, personalizar o separador (`sep`) e o final da linha (`end`).

`print(f"Você tem {idade} anos.")`

---------------------------------------

## • **Semestre 2**

° Todo conteúdo acima é referente do **primeiro semestre**.

° para o **SEGUNDO SEMESTRE** em **python** iremos abordar os seguintes conteúdos: 

| ***Matéria***               | ***Conteúdo***                                                                                                 |
| --------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Interoperabilidade** →    | JSON (Produção e aplicação) / Recursos HTTP / Integração com Oracle (Banco de Dados) / API.                    |
| **Algoritmos** →            | Algoritmos de busca / Eficiência de Algoritmos / Algoritmos de Ordenação.                                      |
| **Recursos de Linguagem** → | Uso de Bibliotecas + PIP / Orientação a objetos / Testes automatizados / Entrada e Saída de dados assíncrona.  |







»°•
