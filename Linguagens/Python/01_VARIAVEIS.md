## • **Variáveis em Python: criação e modificação**

° Uma variável é um **nome** que aponta para um valor armazenado na memória. Pensa assim: é como uma etiqueta que você cola num objeto — e você pode mover essa etiqueta para outro objeto quando quiser.

-----------------------------------------------
 • **Criando variáveis**

° Em Python, você cria uma variável simplesmente atribuindo um valor a um nome. Não precisa declarar o tipo antes (diferente de Java):

```python
idade = 20          # inteiro (int)
cidade = "São Paulo" # texto (str)
preco = 9.99         # decimal (float)
ativo = True         # booleano (bool)
```

° A **tipagem dinâmica** do *Python* faz ele descobrir o valor da variável de forma automática.

---------------------------------------------------

 • **Modificando variáveis**

Modificar é só atribuir um novo valor ao mesmo nome. A etiqueta sai do valor antigo e cola no novo:

```python
idade = 20
idade = 21         # agora aponta para 21; o 20 "some"

cidade = "São Paulo"
cidade = "Rio de Janeiro"  # nome cidade agora aponta para outro texto
```



»°•