## • **PYTHON**

° Python é uma **linguagem de programação de alto nível**, criada por **Guido van Rossum** e lançada em 1991. Seu nome é uma homenagem ao grupo de comédia britânico **Monty Python**, e não à cobra — apesar do mascote!

° Ela foi projetada com uma filosofia clara: **código deve ser legível, simples e expressivo**. Hoje é uma das linguagens mais populares do mundo, usada em áreas como ciência de dados, automação, desenvolvimento web, inteligência artificial e muito mais.

--------------------------------------------------------------------------------
## • **Iteration (Iteração)**

° **Iteração** é o processo de **percorrer uma sequência de elementos um por um**, executando alguma ação a cada passo.

° Toda vez que passamos por cada **elemento** de uma **lista,dicionário,string ou qualquer sequência**, estamos iterando sobre ela. Um objeto que permite isso é chamado de **iterável** (_iterable_), e cada passagem individual é uma **iteração**.

-----------------------------------------------
## • **Variáveis e Tipos de Dados**

» Variáveis são palavras (caixas) onde guardamos dados para utilizar no código, em Python a tipagem do dado é feita de forma **automática** pelo Python (tipagem dinâmica), mas para um código limpo e legível é importante saber seus tipos. 

| Tipo       | Descrição e Exemplo                              |
| ---------- | ------------------------------------------------ |
| `str`      | Texto — `'Ana'`, `"Python"`, `'Olá mundo'`       |
| `int`      | Números inteiros — `10`, `-3`, `0`, `1000`       |
| `float`    | Números decimais — `3.14`, `-0.5`, `1.68`        |
| `bool`     | Verdadeiro ou falso — `True`, `False`            |
| `list`     | Lista de valores — `[1, 2, 3]`, `['a', 'b']`     |
| `dict`     | Par chave-valor — `{'nome': 'Ana', 'idade': 25}` |
| `tuple`    | Lista imutável — `(1, 2, 3)`                     |
| `NoneType` | Ausência de valor — `None`                       |

----------------------------

## • **Input e Output (Entrada e Saída de Dados)**

» É a **interação com o usuário**. "Input" (entrada) serve para capturar o que o usuário digita no teclado. "Output" (saída) serve para mostrar informações na tela.

#### ° **Entrada com** `input()`:

Recebe um valor digitado pelo usuário e **sempre retorna uma string** (texto). Se quiser um número, você precisa converter com `int()` ou `float()`.

`idade = int(input("Digite sua idade: "))`

#### ° **Saída com** `print()`:

Exibe uma ou mais informações no terminal. Pode usar vírgulas, f-strings, personalizar o separador (`sep`) e o final da linha (`end`).

`print(f"Você tem {idade} anos.")`

```python

nome = input("Digite seu nome: ")
#Entrada de dados

print("Olá,", nome)
#Saida de dados

```

--------------------------------------

## • **Execução Condicional: `if`, `else`**

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

» **If, elif e else** são estruturas condicionais. Estruturas condicionais são seções onde definem condições para a execução de determinados blocos de comandos (ao invés de executa-los todos de uma o programa para e decide qual caminho seguir baseada na condição do momento).

» Basicamente se **X** condição for satisfeita, execute **esse** bloco de comandos, **senão** execute outro bloco de comandos.

» O **elif** é uma estrutura intermediária dentro da seção if-else no python e deve vir como um complemento a ambos. Quando você já tem um IF e um ELSE, mas precisa de uma condição para especificar outra regra, pode usar o elif.

 • **Exemplo de If, Else e Elif:**

```python

print ("Selecione o seu operador: +,-,/,*") #calculadora que seleciona os operadores .

operador =input()

print ("Digite um número a sua escolha:")

num1 = float(input())

print ("Digite outro número:")

num2 = float(input())

if operador == "+":     #if, elif e else sempre estão são atreladas em condições

    num1 + num2

    print (num1 + num2)

elif operador == "-":

    num1 - num2

    print (num1 - num2)

elif operador == "/":

    num1 / num2

    print (num1 / num2)

elif operador == "*":

    num1 * num2

    print (num1 * num2)

else:

    print ("Operador Inválido (Selecione entre: +, -, * ou ;).")

```

---

 • **Resumo Rápido em Tabela**:

| Conceito            | Função usada / Exemplo       |
| ------------------- | ---------------------------- |
| Entrada de dados    | `input()`                    |
| Saída de dados      | `print()`                    |
| Criar variáveis     | `nome = "Maria"`             |
| Modificar variáveis | `idade = idade + 1`          |
| Condicional simples | `if condição: ... else: ...` |

----------------------------------------------------------------------------------------------

## • **Como importar em forma eficiente:**

° Quando você usa `from ... import ...`, está dizendo ao Python: **"busque dentro de um arquivo específico uma função que quero usar aqui"**.

 • **Exemplo de Import:**

```python

#Para importar objetos em python:

from nome_do_objeto import nome_da_func

#como consumir esse import (exemplo)

from contador import contar_palavras

frase = input("Digite uma frase").strip()
..
	..
resultado = contar_palavas(frase)

##estamos colocando os valores na variavel frase e associando eles a funcao contar_palavras

```

» **Explicando o exemplo:

° Vai até o arquivo `contador.py` e importa a função `contar_palavras`

° Pede uma frase ao usuário, remove espaços extras das bordas com `.strip()` e guarda na variável `frase`

```
arquivo contador.py          seu script principal
┌──────────────────┐         ┌────────────────────────┐
│ def contar_      │  import │frase = input(...)      │
│   palavras(text):│ ──────► │  resultado =           │
│   return ...     │         │  contar_palavras(frase)│
└──────────────────┘         └────────────────────────┘
```




»°•
