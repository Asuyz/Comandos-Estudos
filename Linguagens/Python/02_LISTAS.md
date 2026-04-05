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

° A representação do uso da listas vem de: **[]**
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

