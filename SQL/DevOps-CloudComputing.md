PL/SQL

**Procedural Language/Structured Query Language**.

É uma linguagem criada pela Oracle Corporation que estende o **SQL** tradicional, adicionando recursos de programação procedural.

Em outras palavras:

- **SQL** → consulta e manipula dados.
    
- **PL/SQL** → permite criar _lógica de programação_ dentro do banco de dados.

Todo código PL/SQL segue esta estrutura:

```SQL
DECLARE
   -- variáveis (opcional)
BEGIN
   -- código executável
   dbms.output.put_line --> é o print do PL/SQL 
EXCEPTION
   -- tratamento de erros (opcional)
END;
```

PL/SQL é muito usado em bancos Oracle para:

- Criar **procedures**
    
- Criar **functions**
    
- Criar **triggers**
    
- Automatizar regras de negócio
    
- Validar dados
    
- Tratar exceções (erros)
    
- Criar pacotes (packages)


Bloco Anonimo é um objeto de banco de dados com regra de negócios (programação) que existe só em tempo de execução.

Estrutura de um bloco Anonimo:

```SQL

DECLARE
   -- declaração de variáveis (opcional)
BEGIN
   -- código executável
EXCEPTION
   -- tratamento de erros (opcional)
END;
/

--> O `/` no final serve para executar o bloco em ferramentas como SQL*Plus ou SQL Developer.


```

Exemplo de PL/SQL | da estrutura: 

```SQL
SET SERVEROUT ON

DECLARE

v_Real NUMBER := 200;

BEGIN

    dbms_output.put_line(v_Real || 'em dol fica:' || round((v_Real/5.13),2));

END;
```

- Para as Variáveis em PL/SQL (convenção)

| Prefixo | Significado     |
| ------- | --------------- |
| `v_`    | variável        |
| `p_`    | parâmetro       |
| `c_`    | constante       |
| `g_`    | variável global |
| `l_`    | variável local  |

Sinais para operações matematicas:
- +
- -
- /
- *

SET SERVEROUTPUT ON - Serve para informar que estou trabalhando, mostrar todos os valores

Utilizamos os tipo de dados padrão:
- VARCHAR
- VARCHAR2
- CHAR
- NUMBER
- DATE
- NUMERIC
- DATETIMEOFFSET (trabalho com dados globais)
- BLOB (Imagens/Arquivos que foram convertidos em binário)
- CLOB











