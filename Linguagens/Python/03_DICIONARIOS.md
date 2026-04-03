## • **Dicionários**

° Dicionários são como cofres de dados, onde utilizamos caso haja um grande fluxo de dados, onde precisamos de relacionarmos eles entre: **chave e dados (valor)**.

↪ A palavra reservada utilizada em dicionários é: **dict()**

° Um dicionário armazena elementos, esses elementos são nossos **objetos** onde cada **chave** é um **dado (valor)** exclusivo deste elemento.

↪ *cada objeto é divido entre: chave e valor igual descrito acima* 

---------------

• **Principais Métodos dos Dicionários**

| Método / Função   | Descrição                                   |
| ----------------- | ------------------------------------------- |
| **.keys()**       | Retorna todas as chaves como uma view       |
| **.update()**     | Mescla outro dicionário no atual            |
| **.clear()**      | Remove todos os itens                       |
| **.values()**     | Retorna todos os valores como uma view      |
| **.setdefault()** | Insere uma chave como padrão se não existir |
| **len()**         | Número de pares chave-valor                 |
| **.items()**      | Retorna pares (chave, valor) como tuplas    |
| **.copy()**       | Cópia rasa do dicionário                    |

--------------------------

• **Formas de Criar Dicionários:**

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

 • **Diferença entre d[] e .get()**

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
