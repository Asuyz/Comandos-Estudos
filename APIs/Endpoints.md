• **O que é um EndPoint**

° Os endpoints das API's são locais onde a API recebe as chamadas (solicitações)

° Os endpoints funcionam como localizadores que apontam onde o recurso que precisa ser utilizado pela API está localizado na aplicação.

° Os endpoints seguros e formatados são **essenciais** para o funcionamento correto das API's

-----------

• **Como funcionam os endpoints**

° Os endpoints de API's geralmente são descritos na documentação da aplicação, onde está informado de quais maneiras a API aceitara as informações (solicitações) e como devem ser formadas.

° Os formatos usados pelas API's são por exemplo: 

| Formato            | Descrição                                                                 |
|--------------------|--------------------------------------------------------------------------|
| JSON               | O mais comum para troca de dados entre APIs                              |
| XML                | Usado principalmente em sistemas legados, bancos e emissão de notas      |
| Form URL-encoded   | Utilizado em formulários web simples                                     |
| Multipart          | Específico para upload de arquivos                                       |
| Protobuf           | Formato binário eficiente, usado no gRPC                                 |
| SSE / NDJSON       | Usado por LLMs para streaming de dados (texto token por token)           |

-----------------------------

• **Contextos breves para entendimento:**

° No contexto de **API REST** os endpoints são acessado utilizando solicitações **HTTP** (**POST, GET, PUT, PATCH E DELETE**). Cada método citado indica como a ação que o cliente deseja realizar.

° Em **GraphQL** os endpoints são colocados em um único endpoint (**POST/graphql**) e quem define o que buscar é o cliente, não o servidor, sendo possivel realizar como por exemplo: **Query, Mutation e Subscription**. 

° **gRPC** abandona o conceito de endpoint e trabalha definindo serviços com métodos em um arquivo .proto, onde o framework gera o código automaticamente.

° E em **WebSocket** é uma comunicação bidirecional em tempo real, onde a cada segundo a conexão fica ativa mandando eventos quanto eles acontecem.

------------------------------------------------------------

