## • **Structured query language (SQL)**

» SQL é uma linguagem de programação feita para armazenar e processar informações dentro de uma data-base relacional.

 • **Linguagens do SQL:**

| Tipo                               | Função                                                          |
| ---------------------------------- | --------------------------------------------------------------- |
| DDL (Data Definition Language)     | Cria e altera estruturas -> (**CREATE, ALTER, DROP, TRUNCATE**) |
| DML (Data Manipulation Language)   | Manipula os dados -> (**INSERT, UPDATE, DELETE**)               |
| DQL (Data Query Language)          | Consulta -> (**SELECT**)                                        |
| DCL (Data Control Language)        | Permissões -> (**GRANT, REVOKE**)                               |
| TCL (Transaction Control Language) | "Checkpoints" -> (**COMMIT, ROLLBACK**)                         |

• **1FN | 2FN | 3FN** (Formas Normais)

» **1FN** -> A primeira forma normal é um conceito fundamental no processo de normalização de banco de dados, tem objetivo de evitar redundâncias e organizar os dados. A **1FN** exige:

° A tabela deve ter valores atômicos (Cada célula deve da tabela deve ter um **ÚNICO** valor ).

° Cada registro (linha) deve ser único.

° Não pode haver grupos repetitivos (as colunas não podem ter múltiplos valores).

• **EM RESUMO**: aplicar a **1FN** é criar um atributo de apoio para armazenar as informações que se repetem e podem ser expandidas (Se um atributo tem múltiplos valores, devemos separá-los em outra tabela, criando uma relação 1-N)

» **2FN** (Deve estar na 1FN) -> A segunda forma normal é verificar se os campos dependem da chave primária composta (**apenas se aplica em chaves primarias compostas**), caso um atributo não dependa da **chave primária composta** precisamos criar uma chave **primária** para o mesmo.

» **3FN** (Deve estar na 2FN) -> A terceira forma normal exige que não exista **dependência transitiva**

° **Dependência transitiva:** Ocorre quando uma coluna **não-chave** depende de outra coluna **não-chave** e essa segunda coluna depende da chave primária.

 • **Exemplos DDL (Data Definition Language)** 

```sql

-- Criar tabela

CREATE TABLE clientes (
	id INT PRIMARY KEY,
	nome VARCHAR(100) NOT NULL,
	email VARCHAR(150) UNIQUE,
	data_cadastro DATE DEFAULT CURRENT_DATE

);

-- Alterar tabela

ALTER TABLE clientes ADD telefone VARCHAR(20);

-- Modificar coluna

ALTER TABLE clientes MODIFY telefone VARCHAR(30);

-- Renomear coluna

ALTER TABLE clientes RENAME COLUMN telefone TO celular;

-- Remover coluna;

ALTER TABLE clientes DROP COLUMN celular;

-- Excluir tabela

DROP TABLE clientes;

```

 • **Exemplos DML (Data Manipulation Language)**

```sql

-- Inserir

INSERT INTO clientes (id,nome,email)
VALUES (1, 'Andre', 'andre@email.com');

-- Inserir múltiplas linhas 

INSERT INTO clientes (id, nome, email)
VALUES 
(2, 'João', 'joao@email.com'),
(3, 'Maria', 'maria@email.com');

-- Update (Sempre utilize where ou toda tabela será atualizada)

UPDATE clientes
SET email = 'novo@email.com'
WHERE id = 1;

-- Excluir (Where tem a mesma função do update)

DELETE FROM clientes
WHERE id = 3;

-- Excluir tudo sem apagar a tabela

TRUNCATE TABLE clientes;

```

 • **Exemplos DQL (Data Query Language)**

```sql

-- Select básico

SELECT nome, email
FROM clientes;

-- Selecionar tudo

SELECT * FROM clientes;
```

-------------------------------

## • **Filtros para WHERE:**

» Operadores comuns:

- `=`, `<>`
- `<`, `>`, `<=`, `>=`
- `LIKE` (texto parcial)
- `BETWEEN`
- `IN`
- `IS NULL / IS NOT NULL`

• **Exemplos dos filtros de WHERE:**

```sql

SELECT * FROM clientes WHERE nome LIKE '%a%';

SELECT * FROM pedidos 
WHERE valor BETWEEN 100 AND 500;

SELECT * FROM clientes
WHERE id IN (1, 2, 4);

-- Ordenação

SELECT * FROM clientes
ORDER BY nome ASC;

ORDER BY nome DESC;

-- Limitar Linhas 

SELECT * FROM clientes LIMIT 10;

```

---------------

## • **Funções de agregação**

| Função     | Descrição    |
| ---------- | ------------ |
| COUNT()    | Conta linhas |
| SUM()      | Soma valores |
| AVG()      | Média        |
| MIN()      | Mínimo       |
| MAX()      | Mínimo       |
| GROUP BY() | Agrupamento  |
 • **Exemplos das funções:**

```sql

SELECT COUNT(*) AS total_clientes
FROM clientes;

-- Agrupamento

SELECT cidade, COUNT(*) AS total
FROM clientes
GROUP BY cidade;

-- Filtrar 

HAVING COUNT(*) > 5;

```

------------------

## • **Relacionamentos e JOINs

» - **INNER JOIN**  
    Retorna apenas os registros que existem **em ambas as tabelas** (interseção).
    
- **FULL JOIN (FULL OUTER JOIN)**  
    Retorna **todos os registros das duas tabelas**, combinando quando há correspondência e preenchendo com `NULL` quando não há.
    
- **LEFT JOIN (LEFT OUTER JOIN)**  
    Retorna **todos os registros da tabela da esquerda**, e apenas os correspondentes da direita (ou `NULL` se não houver).
    
- **RIGHT JOIN (RIGHT OUTER JOIN)**  
    Retorna **todos os registros da tabela da direita**, e apenas os correspondentes da esquerda (ou `NULL` se não houver).
    
- **CROSS JOIN**  
    Retorna o **produto cartesiano**, ou seja, **todas as combinações possíveis entre as linhas das duas tabelas**, sem necessidade de condição (`ON`).

```sql

-- Inner join 
SELECT clientes.nome, pedidos.valor
FROM clientes
INNER JOIN pedidos
    ON clientes.id = pedidos.cliente_id;
-- Left Join 
SELECT clientes.nome, pedidos.valor
FROM clientes
LEFT JOIN pedidos
  ON clientes.id = pedidos.cliente_id;
  
-- Right Join | oposto do LEFT

-- Full Join | Traz tudo dos dois lados (dependendo do banco) 

-- Cross Join | Produto Cartesiano
--> Ex: Table1 - 3 Linhas
--> Table2 - 4 linhas, seu cross join tera 12 linhas (3x4)
--> Apenas combina tudo com tudo

```

---------------------

## • **Exemplo de subconsultas (Subqueries)**:

» No **Where**:

```sql

SELECT nome
FROM clientes
WHERE id IN (SELECT cliente_id FROM pedidos);

```

» No **Select:

```sql

SELECT 
    nome,
    (SELECT COUNT(*) FROM pedidos WHERE cliente_id = clientes.id) AS total_pedidos
FROM clientes;

```

------------------------

## • **Exemplo de TCL (Transaction Control Language)**:

» Para um controle das ações que irá realizar: 

```sql

BEGIN; -- Começo das Alterações

UPDATE contas SET saldo = saldo - 100 WHERE id = 1;
UPDATE contas SET saldo = saldo + 100 WHERE id = 2;

COMMIT;   -- aplica
-- ROLLBACK;  volta atrás (CTRL Z DO SQL)

```

•°»

--------------------------------------------------------------

## • **PL/SQL**

» PL/SQL significa Procedural Language / Structured Query Language. 

» O nome justifica-se, pois a linguagem integra construções procedurais com o acesso ao banco de dados por meio da linguagem SQL.

» Sua característica principal é a sua estrutura em bloco com: **Declare** (Opcional), **Begin**, **Exception** (Opcional) e **End**.

```plsql
/*
DECLARE
/* Declaração de variáveis de memória – opcional

BEGIN
/* Instruções de funcionamento – processamento, ifs

EXCEPTION
/* Tratamento de exceções
opcional

END
/* Finalização do bloco
```

• **Recursos de Linguagem**

| Categoria 1            | Categoria 2   | Categoria 3 |
| ---------------------- | ------------- | ----------- |
| Tratamento de erros    | Cursores      | Pacotes     |
| Tipos e variáveis      | Procedimentos | Coleções    |
| Estrutura de decisão   | Funções       |             |
| Estrutura de repetição | Gatilhos      |             |
» - **Categoria 1 (estrutura básica do código)**  
    Reúne elementos essenciais para construir qualquer programa:
    
    - Tipos e variáveis → armazenar dados
        
    - Estruturas de decisão → tomar decisões (`IF`, `CASE`)
        
    - Estruturas de repetição → criar loops (`FOR`, `WHILE`)
        
    - Tratamento de erros → lidar com exceções
        
- **Categoria 2 (lógica e modularização)**  
    Foca em como organizar e executar operações:
    
    - Procedimentos e funções → reutilizar código
        
    - Cursores → manipular resultados de consultas
        
    - Gatilhos (triggers) → automatizar ações no banco
        
- **Categoria 3 (organização avançada e estrutura de dados)**  
    Voltada para arquitetura e estruturas mais complexas:
    
    - Pacotes → agrupar e organizar código
        
    - Coleções → trabalhar com conjuntos de dados em memória

-----------------------------------------------
## • **Bloco Anônimo**

» Um **bloco anônimo** é um código PL/SQL que:

- **não tem nome**
    
- **não fica salvo no banco**
    
- é executado **na hora e descartado depois**

• **Exemplo simples**

```plsql
BEGIN
   DBMS_OUTPUT.PUT_LINE('Olá, mundo!');
END;
/

```

» ` DBMS_OUTPUT.PUT_LINE()` é o **print** da linguagem.

• **Exemplo com variável**

```plsql
DECLARE
   v_nome VARCHAR2(50) := 'André';
BEGIN
   DBMS_OUTPUT.PUT_LINE('Nome: ' || v_nome);
END;
/

```

» O **operador** || (**Double Pipe**) utilizado no exemplo acima é a concatenação de strings ou texto + **variáveis**

-----------------------------------------------

## • **Sintaxe de variáveis**

» As **variáveis** sempre estarão na seção de **DECLARE** em PL/SQL.

» Sua sintaxe **PADRÃO:**

```plsql
nome_variavel TIPO [:= valor_inicial];
```

» - `:=` → atribuição

------------------------------------------

## • **Sintaxe usada em PL/SQL**

» Exemplos de lógica dentro do **PL/SQL** e como são escritas na linguagem abordada.

» Diferente do **SQL** em **PL/SQL** precisamos de **INTO** ao invés de **FROM** no **SELECT**.

```plsql
SELECT nome INTO v_nome FROM clientes WHERE id = 1;
```


• **Estrutura de Decisão**

```plsql
IF condição THEN
   ...
ELSIF condição THEN
   ...
ELSE
   ...
END IF;
```

• **Loops**

» **FOR**

```plsql
FOR i IN 1..10 LOOP
   ...
END LOOP;
```

» **WHILE**

```plsql
WHILE condição LOOP
   ...
END LOOP;
```

» **LOOP SIMPLES**

```plsql
LOOP
   EXIT WHEN condição;
END LOOP;
```

• **Exceções**

```plsql
EXCEPTION
   WHEN ZERO_DIVIDE THEN ...
   WHEN NO_DATA_FOUND THEN ...
   WHEN OTHERS THEN ...
```

» **OTHERS pega qualquer outro erro da exceção**.
