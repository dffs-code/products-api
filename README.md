# API REST de Produtos

## Descrição:

API REST para gerenciamento de produtos, utilizando Java, Spring Boot, JPA e PostgreSQL.

## Tecnologias Utilizadas

- Spring Boot: Framework para criação de aplicações Java baseadas em Spring.
- PostgreSQL: Banco de dados relacional para armazenamento dos dados.
- Maven: Ferramenta de automação de compilação e gerenciamento de dependências.
- Spring Data JPA: Facilita a implementação da camada de persistência.
- Spring Web: Para construir aplicativos web com Spring MVC e RESTful.

## Funcionalidades

- Cadastro, leitura, atualização e exclusão de produtos.
- Endpoint para listar todos os produtos.
- Endpoint para buscar um produto por ID.

## Instalação:

1. Clone o projeto para o seu computador.
2. Instale o Maven.
3. Configure o banco de dados PostgreSQL.
4. Altere as propriedades de conexão no arquivo `application.properties`.
5. Execute o comando `mvn clean install`.
6. Inicie a aplicação com o comando `mvn spring-boot:run`.

## Uso da API:

- A API está disponível na seguinte URL:
  http://localhost:8080/products
- A API utiliza o formato JSON para comunicação.

**POST /products**
  - **Descrição**: Este endpoint permite adicionar um novo produto ao sistema.
  - **Campos necessários no corpo da solicitação**:
    - `name` (string): O nome do produto.
    - `value` (number): O preço do produto.

**GET /products**
  - **Descrição**: Este endpoint retorna uma lista de todos os produtos cadastrados no sistema.

**GET /products/{id}**
  - **Descrição**: Este endpoint retorna um produto específico com base no ID fornecido.
  - **Parâmetros de consulta**:
    - `id` (UUID): O ID único do produto que deseja-se buscar.

**PUT /products/{id}**
  - **Descrição**: Este endpoint permite atualizar os detalhes de um produto existente com base no ID fornecido.
  - **Parâmetros de consulta**:
    - `id` (UUID): O ID único do produto que deseja-se atualizar.
  - **Campos necessários no corpo da solicitação**:
    - `name` (string): O novo nome do produto (opcional).
    - `value` (number): O novo preço do produto (opcional).

**DELETE /products/{id}**
  - **Descrição**: Este endpoint permite excluir um produto existente com base no ID fornecido.
  - **Parâmetros de consulta**:
    - `id` (UUID): O ID único do produto que deseja-se excluir.

