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
