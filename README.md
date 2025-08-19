## Descrição

Criação de uma aplicação web simples para gerenciamento de usuários, desenvolvida com Flask e estruturada como uma API Restful.
A API conta com as quatro operações básicas do CRUD (Create, Read, Update, Delete) permitindo criar, consultar, atualizar e excluir usuários.
Os dados são armazenados temporariamente em uma lista, simulando um banco de dados simples.


## Requisitos Funcionais

### POST /users (Create)
- Cria um novo usuário.
- Requisição: JSON com `nome` (string) e `email` (string).
- A aplicação gera um ID único para o usuário.
- Resposta: JSON do usuário criado e status **201 Created**.

### GET /users (Read All)
- Retorna todos os usuários cadastrados.
- Resposta: lista JSON de usuários (ou `[]` se vazio) e status **200 OK**.

### GET /users/<int:user_id> (Read Single)
- Retorna um usuário pelo ID.
- Se encontrado: JSON do usuário e status **200 OK**.
- Se não encontrado: JSON de erro e status **404 Not Found**.

### PUT /users/<int:user_id> (Update)
- Atualiza os dados de um usuário existente.
- Requisição: JSON com `nome` e/ou `email`.
- Se encontrado: JSON atualizado e status **200 OK**.
- Se não encontrado: JSON de erro e status **404 Not Found**.

### DELETE /users/<int:user_id> (Delete)
- Remove um usuário pelo ID.
- Se encontrado: JSON de sucesso (ex: `{"message": "Usuário excluído com sucesso"}`) e status **200 OK**.
- Se não encontrado: JSON de erro e status **404 Not Found**.
