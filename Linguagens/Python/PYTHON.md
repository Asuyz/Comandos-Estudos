## • **< -PYTHON ->**

° Python é uma **linguagem de programação de alto nível**, criada por **Guido van Rossum** e lançada em 1991. Seu nome é uma homenagem ao grupo de comédia britânico **Monty Python**, e não à cobra — apesar do mascote!

° Ela foi projetada com uma filosofia clara: **código deve ser legível, simples e expressivo**. Hoje é uma das linguagens mais populares do mundo, usada em áreas como ciência de dados, automação, desenvolvimento web, inteligência artificial e muito mais.

--------------------------------------------------------------------------------
## • **Iteration (Iteração)**

° **Iteração** é o processo de **percorrer uma sequência de elementos um por um**, executando alguma ação a cada passo.

° Toda vez que passamos por cada **elemento** de uma **lista,dicionário,string ou qualquer sequência**, estamos iterando sobre ela. Um objeto que permite isso é chamado de **iterável** (_iterable_), e cada passagem individual é uma **iteração**.
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

## • **Variáveis: Criação e Modificação**

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

## • **Exemplo de If, Else e Elif:**

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

---

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

--------------------------------------

## • **Funções**

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

## • **Listas e Sequências**

° Listas são **estruturas que armazenam coleções de dados**. São usadas quando você precisa guardar vários valores em uma única variável, como uma lista de nomes, números ou itens.

|Tipo|Características|
|---|---|
|`list`|Mutável e ordenada|
|`tuple`|Imutável e ordenada|
|`set`|Mutável e **não ordenada**, sem itens repetidos|
|`str`|Também é uma sequência (de caracteres)|

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

------------------------------------------

• **Append()**

° Para adicionarmos valores em uma lista utilizamos o **append()** onde ele adiciona um **único** elemento a uma lista **existente, modificando a lista original e não retornando uma nova lista.**

```python
num = [1,2,3]
num.append("4")
```

° o método **extend** é utilizado para adicionar todos os elementos de uma **lista,tupla,String ou set no final de uma lista existente e não retorna uma nova lista similar ao append().**

```python
Carros = ["Bmw","Volvo","Fiat"]
num = [1,2,3]
Carros.extend(num)
print(Carros)
# Output -> ["Bmw,"Volvo","Fiat",1,2,3]

# Extend com Tupla

minha_lista = ['a','b']
minha_tupla('c','d')
minha_lista.extend(minha_tupla)
print(minha_lista)
# Output -> ['a','b','c','d']

# Extend com Caracteres Separados
Lista1= ['h','i']
Lista1.extend('hello')
print(Lista1)
# Output -> ['h','i','h','e','l','l','o']

```

↪ para converter cada número ou palavras em posições únicas de índice utilizamos: 

```python
entrada = input('algo')
lista = list(entrada)
```

° **List** é uma palavra **reservada** dentro do Python para esse tipo de função, onde por exemplo se o **input** foi por exemplo "algo" ele transformaria em uma lista: ['a','l','g','o'].

• **Conversão de Lista com Split

° O **split()** em listas é útil quando os caracteres são escritos de forma separada, assim ordenando eles em índices únicos para cada respectiva seperação.

------------------------------------------

• **Operador in**

° O Operador **in** em listas e também fora delas server para verificar se algo existe dentro de outro algo:

↪ **Verifica se X faz parte da Lista (Exemplo 1)**

↪ **Verifica se x é uma chave no ***Dicionário***.

-----------------------------------

• **Listas Dentro de Listas**

° Podemos criar listas dentro de listas onde devemos manipular dois **índices**:
↪ Um será referente a qual lista estamos.

↪ O outro será referente ao valor dentro da lista

```python
print(exemplo [0],[2])
```

° O índice **zero** é referente a qual lista e o índice **dois** é referente ao valor dentro da lista.

• **Funções para Listas Numéricas.

° Temos **3 funções** para valores:

↪ **max** retorna o valor **maior** da lista

↪ **min** retorna o **menor** valor da lista

↪ **sum** retorna a soma dos **valores** dentro da lista escolhida

----------------------------------

• **Soma de listas (somando os valores dentro dos índices)**

° Para a soma dos valores dentro de uma lista poder utilizar o **zip().**

```python
a = [1, 2, 3]
b = [1, 2, 3]

resultado = [x + y for x, y in zip(a, b)]
print(resultado)  # [2, 4, 6]
```

° Podemos usar também **map()** com o operador **.add**.

```python
from operator import add

resultado = list(map(add, a, b))
print(resultado)  # [2, 4, 6]
```

° O **NumPy** é ideal para listas grandes.

```python
import numpy as np

resultado = list(np.array(a) + np.array(b))
print(resultado)  # [2, 4, 6]
```

° E por último podemos aplicar um loop manual com **range()**

```python
resultado = []
for i in range(len(a)):
    resultado.append(a[i] + b[i])
print(resultado)  # [2, 4, 6]
```

----------------------------------------------

• **Inversão de Lista**

° Para inverter uma lista (seu índice) podemos realizar da seguintes formas:

```python

Lista[::-1]
#Slicing (retorna uma nova lista)

List(reversed(lista))
#Retorna um Interador

Lista.reverse()
#Modifica a Lista original

```

° Para acessarmos os elementos pelo índice inverso utilizamos o negativo.

↪ [0,1,2] o inverso: [-3,-2,-1]

--------------------------------------

• **Conversão de lista para string (print)**

↪ Para transformarmos uma lista ([8,0,7]) em uma string (807)
podemos utilizar:

° **join()** com compressão de lista.

```python
lista = [8, 0, 7]
print("".join(str(n) for n in lista))
```

↪ O `join` sozinho não funciona com inteiros, por isso é necessário converter cada número para string antes com `str()` ou `map(str, ...)`.

° Converter para **string** e concatenar.

```python
resultado = ""
for n in lista:
    resultado += str(n)
print(resultado)  # 807

```

° Usando **join() e map()**.

```python
print("".join(map(str, lista)))
```


--------------------------------
## • **Funções**

° Funções permitem o reaproveitamento do código de forma eficiente, assim permitindo modularidade do código e a separação de tarefas do código

° **Classe vs Função** quando usar um ou outro:

↪ Usamos **função** quando: não precisamos de um objeto, não há estado (**self**) e é apenas uma ação.

↪ Usamos **classe** quando: existe um estado (**atributos**), existe um comportamento ligado ao estado e quando faz sentindo criar múltiplas instâncias desse estado.

° Para criarmos funções utilizamos o comando **def** onde a estrutura básica de uma consiste em: 

```python
def nome_function (paramentros):
	#codigo
	
	return #caso seja necessario
```



-------------------------------------

## • **Dicionários**

° Dicionários são como cofres de dados, onde utilizamos caso haja um grande fluxo de dados, onde precisamos de relacionarmos eles entre: **chave e dados (valor)**.

↪ A palavra reservada utilizada em dicionários é: **dict()**

° Um dicionário armazena elementos, esses elementos são nossos **objetos** onde cada **chave** é um **dado (valor)** exclusivo deste elemento.

↪ *cada objeto é divido entre: chave e valor igual descrito acima* 

---------------


° **Formas de Criar Dicionários:**

```python
#1. Chaves literais
pessoa = {
    "nome": "Ana",
    "idade": 30,
    "cidade": "São Paulo"
}

# 2. Construtor dict()
carro = dict(marca="Toyota", ano=2022, cor="preto")

# 3. Dict comprehension
quadrados = {x: x**2 for x in range(1, 6)}

# 4. fromkeys() — chaves com valor padrão
notas = dict.fromkeys(["mat", "port", "geo"], 0)

# 5. Dicionário vazio
vazio = {}
vazio2 = dict()
```

↪ Na número 1 (Chaves Literais) podemos utilizar valores **imutáveis** como:

| Valores Permitidos |
| ------------------ |
| str                |
| int                |
| float              |
| tuple              |

---------------------------------------

 ° **Diferença entre [] e .get()**

↪ **d["chave"]**

» Acesso direto. Se a chave não existir, lança um KeyError e o programa para imediatamente.

↪ **d.get("chave")**

» Acesso seguro. Se a chave **não existir**, retorna `None` (ou um valor padrão que você define).

» Utilizamos **d["chave"]** quando: a chave **DEVE** existir (sua ausência é um bug) e quando queremos que o erro apareça imediatamente

```python
config = {"db_url": "postgres://..."}
url = config["db_url"]     
```

» Utilizamos **d.get("chave")** quando: a chave pode ou **não existir** ou queremos um valor padrão ao invés de travar (com o erro)

```python
perfil = {"nome": "Leo"}
bio = perfil.get("bio", "Sem descrição")
```

------------------

° **Principais Métodos dos Dicionários**

» **.keys()** -> Retorna todas as chaves como uma view.

» **.update()** -> Mescla outro dicionário no atual.

» **.clear()** -> Remove todos os itens.

» **.values()** -> Retorna todos os valores como uma view.

» **.setdefault()** -> Insere uma chave como padrão se não existir.

» **len()** Número de pares chave-valor.

» **.itens()** Retorna pares (chave,valor) como tuplas.

» **.copy()** Cópia rasa do dicionário.



---------------------------


---------------------------------------

»°•
