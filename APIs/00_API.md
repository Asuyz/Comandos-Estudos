• **O que é uma API**

° API's são aplicações que permitem a integração de dados, serviços ou recursos de outras aplicações ao invés do desenvolvimento do zero da mesma.

° Também oferecem uma maneira simples e segura de disponibilizar os dados es as funções do aplicativo para o time de desenvolvimento, incluindo o compartilhamento ou comercialização de dados e funções com parceiros e terceiros.

------------------------------------------

• **Como funcionam as API's (fluxo básico)**

° As API's funcionam como uma especie de "garçom", a aplicação envia a solicitação e o servidor oferece a resposta. Então a API é a ponte que estabelece a conexão entre eles.

° A transferência de dados pode e vai varias de acordo com o serviço da web utilizado, toda essa troca de informações (solicitações e respostas) são responsáveis pelas API's.

° Toda requisição de API precisa de um URI (Uniform Resource Identifier) que representa o destino do recurso. Esse URI pode ser uma URL completa ou apenas um caminho, dependendo do contexto.

```
URI completa (URL): https://api.exemplo.com/produtos/5 
Apenas o caminho: /produtos/5
```

° **URI vs URL:** toda URL é uma URI, mas nem toda URI é uma URL. A URL inclui o protocolo e o domínio (`https://...`). A URI pode ser só o caminho (`/produtos/5`).

-------------------------------------------

• **Representação de um fluxo completo de uma API (abordado acima)**

```
Cliente faz:  GET /produtos/5

  │
  ▼
[1] Autenticação   → Token JWT válido? ✓
  │
  ▼
[2] Roteamento     → GET /produtos/{id} → ProductController
  │
  ▼
[3] Lógica         → Busca produto id=5 no banco
  │
  ▼
[4] Serialização   → Converte objeto Produto → JSON
  │
  ▼
[5] Status HTTP    → 200 OK + body JSON

  │
  ▼
Cliente recebe:
{
  "id": 5,
  "nome": "Teclado Mecânico",
  "preco": 349.90
}


```

• **Camadas internas da API**

° ***1. Autenticação***

° Verifica **quem está fazendo a requisição** antes de qualquer coisa.

» Mecanismos comuns:

- **API Key** — uma chave secreta enviada no header
- **JWT (JSON Web Token)** — token com informações do usuário, assinado
- **OAuth 2.0** — fluxo de autorização (ex: "Entrar com Google")

° ***2. Roteamento***

° Direciona a requisição para o **recurso correto** com base na URL e no método HTTP.

```
GET    /produtos      → lista produtos
POST   /pedidos       → cria um pedido
PUT    /usuarios/42   → atualiza usuário de id 42
DELETE /carrinho/7    → remove item do carrinho
```

° **Exemplos de roteamento em Frameworks:**

» *Spring Boot (java)*

```java

@GetMapping("/produtos")
public List<Produto> listarProdutos() { ... }

```

» *FastAPI (python)*

```python

@app.get("/produtos")
def listar_produtos():
    ...

```

° ***3. Lógica de negócio***

° Onde a API **processa, valida e toma decisões** sobre os dados recebidos.

```
"O estoque tem esse produto?"
"O usuário tem saldo suficiente?"
"Esse e-mail já está cadastrado?"
```

° ***4. Serialização***

° Converte os dados internos (objetos, classes) para um **formato de transporte** que o cliente entende.

```
Objeto Python/Java  →  JSON (Formato usado)  →  Cliente

```


° ***5. Status HTTP***

° A API sempre devolve um **código de status** junto com a resposta, indicando o resultado da operação.

| **Código** | **Significado**       | **Quando usar**                       |
| ---------- | --------------------- | ------------------------------------- |
| `200`      | OK                    | Requisição bem-sucedida               |
| `201`      | Created               | Recurso criado com sucesso            |
| `400`      | Bad Request           | Dados inválidos enviados pelo cliente |
| `401`      | Unauthorized          | Não autenticado                       |
| `403`      | Forbidden             | Autenticado, mas sem permissão        |
| `404`      | Not Found             | Recurso não encontrado                |
| `500`      | Internal Server Error | Erro inesperado no servidor           |

---------------------------------------------------

• **Visualização e Testes de API's

° Para visualizar, testar e depurar APIs sem precisar escrever código, utilizamos ferramentas client como **Insomnia** e **Postman**.

° Elas permitem:

- Enviar requisições HTTP (GET, POST, PUT, DELETE) manualmente.
- Inspecionar a resposta completa — status code, headers e body.
- Salvar e organizar coleções de requisições para reutilizar.
- Simular diferentes cenários (token inválido, payload errado, etc.)

-----------------------------------------


