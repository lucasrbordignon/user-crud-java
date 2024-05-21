# Documentação da API RESTful para Gerenciamento de Usuários

Esta API permite o gerenciamento de usuários.

## Endpoints Disponíveis

### 1. Obter Todos os Usuários

- **Método:** GET
- **URL:** `/api/users`
- **Descrição:** Retorna uma lista de todos os usuários cadastrados.
- **Exemplo de Resposta:**
  ```json
  [
    {
      "id": 1,
      "name": "John Doe",
      "email": "john.doe@example.com"
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "email": "jane.smith@example.com"
    }
  ]
  ```

### 2. Obter um Usuário por ID

- **Método:** GET
- **URL:** `/api/users/{id}`
- **Descrição:** Retorna um usuário específico com o ID fornecido.
- **Parâmetros de Requisição:** `{id}` (ID do usuário)
- **Exemplo de Resposta:**
  ```json
  {
    "id": 1,
    "name": "John Doe",
    "email": "john.doe@example.com"
  }
  ```

### 3. Criar um Novo Usuário

- **Método:** POST
- **URL:** `/api/users`
- **Descrição:** Cria um novo usuário com os dados fornecidos.
- **Parâmetros do Corpo da Requisição:** JSON com os campos `name` e `email`.
- **Exemplo de Corpo da Requisição:**
  ```json
  {
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com"
  }
  ```
- **Exemplo de Resposta:**
  ```json
  {
    "id": 3,
    "name": "Alice Johnson",
    "email": "alice.johnson@example.com"
  }
  ```

### 4. Atualizar um Usuário

- **Método:** PUT
- **URL:** `/api/users/{id}`
- **Descrição:** Atualiza os dados de um usuário existente com o ID fornecido.
- **Parâmetros de Requisição:** `{id}` (ID do usuário)
- **Parâmetros do Corpo da Requisição:** JSON com os campos `name` e `email`.
- **Exemplo de Corpo da Requisição:**
  ```json
  {
    "name": "Alice Johnson Updated",
    "email": "alice.johnson.updated@example.com"
  }
  ```
- **Exemplo de Resposta:** 200 OK (sem corpo)

### 5. Excluir um Usuário

- **Método:** DELETE
- **URL:** `/api/users/{id}`
- **Descrição:** Exclui um usuário com o ID fornecido.
- **Parâmetros de Requisição:** `{id}` (ID do usuário)
- **Exemplo de Resposta:** 200 OK (sem corpo)
`
