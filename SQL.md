## • **Structured query language (SQL)**

» SQL é uma linguagem de programação feita para armazenar e processar informações dentro de uma data-base relacional.

## ° **Linguagens do SQL:**

| Tipo                               | Função                                                          |
| ---------------------------------- | --------------------------------------------------------------- |
| DDL (Data Definition Language)     | Cria e altera estruturas -> (**CREATE, ALTER, DROP, TRUNCATE**) |
| DML (Data Manipulation Language)   | Manipula os dados -> (**INSERT, UPDATE, DELETE**)               |
| DQL (Data Query Language)          | Consulta -> (**SELECT**)                                        |
| DCL (Data Control Language)        | Permissões -> (**GRANT, REVOKE**)                               |
| TCL (Transaction Control Language) | "Checkpoints" -> (**COMMIT, ROLLBACK**)                         |

## • **1FN | 2FN | 3FN** (Formas Normais)

» **1FN** -> A primeira forma normal é um conceito fundamental no processo de normalização de banco de dados, tem objetivo de evitar redundâncias e organizar os dados. A **1FN** exige:

° A tabela deve ter valores atômicos (Cada célula deve da tabela deve ter um **ÚNICO** valor ).

° Cada registro (linha) deve ser único.

° Não pode haver grupos repetitivos (as colunas não podem ter múltiplos valores).

• **EM RESUMO**: aplicar a **1FN** é criar um atributo de apoio para armazenar as informações que se repetem e podem ser expandidas (Se um atributo tem múltiplos valores, devemos separá-los em outra tabela, criando uma relação 1-N)

» **2FN** (Deve estar na 1FN) -> A segunda forma normal é verificar se os campos dependem da chave primária composta (**apenas se aplica em chaves primarias compostas**), caso um atributo não dependa da **chave primária composta** precisamos criar uma chave **primária** para o mesmo.

» **3FN** (Deve estar na 2FN) -> A terceira forma normal exige que não exista **dependência transitiva**

° **Dependência transitiva:** Ocorre quando uma coluna **não-chave** depende de outra coluna **não-chave** e essa segunda coluna depende da chave primária.

## • **Exemplos DDL (Data Definition Language)** 

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

## • **Exemplos DML (Data Manipulation Language)**

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

## • **Exemplos DQL (Data Query Language)**

```sql

-- Select básico

SELECT nome, email
FROM clientes;

-- Selecionar tudo

SELECT * FROM clientes;
```

## • **Filtros para WHERE:**

» Operadores comuns:

- `=`, `<>`
- `<`, `>`, `<=`, `>=`
- `LIKE` (texto parcial)
- `BETWEEN`
- `IN`
- `IS NULL / IS NOT NULL`

## ° **Exemplos dos filtros de WHERE:**

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

## • **Funções de agregação**

| Função     | Descrição    |
| ---------- | ------------ |
| COUNT()    | Conta linhas |
| SUM()      | Soma valores |
| AVG()      | Média        |
| MIN()      | Mínimo       |
| MAX()      | Mínimo       |
| GROUP BY() | Agrupamento  |
## • **Exemplos das funções:**

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

## • **Relacionamentos e JOINs

» Para uma manipulação correta de tabelas:

```sql

-- Inner join (retorna apenas registros que existem em ambas as tabelas)

SELECT clientes.nome, pedidos.valor
FROM clientes
INNER JOIN pedidos
    ON clientes.id = pedidos.cliente_id;

-- Left Join (traz todos os clientes, mesmo se não tiver pedidos)

SELECT clientes.nome, pedidos.valor
FROM clientes
LEFT JOIN pedidos
    ON clientes.id = pedidos.cliente_id;
    

-- Right Join | Pouco Utilizado, oposto do LEFT

-- Full Join | Traz tudo dos dois lados (dependendo do banco) 

-- Cross Join | Produto Cartesiano

```

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