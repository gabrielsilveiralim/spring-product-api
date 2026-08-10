# Spring Product API

API REST simples para gerenciamento de produtos, desenvolvida com Spring Boot

O projeto foi desenvolvido para praticar operações básicas de CRUD:

* Criar produtos
* Consultar produtos
* Atualizar produtos
* Deletar produtos

Os dados são armazenados temporariamente em memória, portanto são perdidos quando a aplicação é reiniciada.

## Tecnologias
* Java
* Spring Boot
* Spring Web

## Como executar

### Pré-requisitos

* Java instalado
* Git instalado
* Maven (ou utilizar o Maven Wrapper do projeto)

### 1. Clone o repositório

```bash
git clone https://github.com/gabrielsilveiralim/spring-product-api.git
```

### 2. Entre na pasta do projeto

```bash
cd spring-product-api
```

### 3. Execute a aplicação

Com Maven:

```bash
./mvnw spring-boot:run
```

No Windows:

```bash
mvnw.cmd spring-boot:run
```

A aplicação estará disponível em:

```text
http://localhost:8080
```

## Rotas

### Criar produto

```http
POST api/produtos
```

Exemplo de requisição:

```json
{
  "name": "Notebook",
  "price": 3500.00
}
```

### Listar produtos

```http
GET api/produtos
```

### Buscar produto por ID

```http
GET api/produtos/{id}
```

Exemplo:

```http
GET s/api/produtos
```

### Atualizar produto

```http
PUT api/produtos/{id}
```

Exemplo:

```http
PUT api/produtos/1
```

```json
{
  "name": "Notebook Gamer",
  "price": 4500.00
}
```

### Deletar produto

```http
DELETE api/produtos/{id}
```

Exemplo:

```http
DELETE api/produtos/1
```

## Observação
Este projeto utiliza armazenamento temporário em memória. Ao reiniciar a aplicação, os dados criados, atualizados ou deletados durante a execução são perdidos e a aplicação volta ao estado inicial

