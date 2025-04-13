# E-commerce DevOps

Este repositório contém a configuração DevOps para o sistema de e-commerce, permitindo a execução de todos os componentes em containers Docker.

## Arquitetura

O sistema é composto por três componentes principais:

1. **Frontend** - Interface de usuário em React para o e-commerce
2. **API Backend** - API REST em Python/FastAPI para gerenciar operações de e-commerce
3. **FakeStore API** - Serviço externo para obtenção de dados de produtos

![Arquitetura](arquitetura.png)

## Requisitos

- Docker
- Docker Compose

## Instruções de Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/cscheidegger/e-commerce-devops.git
   cd e-commerce-devops
   ```

2. Crie um arquivo `.env` baseado no `.env.example`:
   ```bash
   cp .env.example .env
   ```

3. Execute o sistema completo:
   ```bash
   make up
   ```

4. Acesse a aplicação:
   - Frontend: http://localhost:5173
   - API: http://localhost:8000
   - API Docs (Swagger): http://localhost:8000/docs

5. Para parar todos os serviços:
   ```bash
   make down
   ```

## Componentes

### Frontend (ecommerce-front)

O frontend é uma aplicação React que fornece uma interface de usuário para interagir com a loja online. Ela se comunica com o backend via API REST.

- Repositório: [https://github.com/cscheidegger/ecommerce-front](https://github.com/cscheidegger/ecommerce-front)

### API Backend (ecommerce-api)

O backend é uma API REST desenvolvida em Python com FastAPI que gerencia todas as operações do e-commerce e se comunica com o serviço externo FakeStore API para obter dados de produtos.

- Repositório: [https://github.com/cscheidegger/ecommerce-api](https://github.com/cscheidegger/ecommerce-api)

### API Externa (FakeStore API)

O sistema utiliza a FakeStore API como serviço externo para obter dados de produtos.

- URL: [https://fakestoreapi.com](https://fakestoreapi.com)
- Documentação: [https://fakestoreapi.com/docs](https://fakestoreapi.com/docs)
- Endpoints utilizados:
  - `GET /products` - Lista todos os produtos
  - `GET /products/{id}` - Obtém detalhes de um produto específico
  - `GET /products/categories` - Lista todas as categorias de produtos
  - `GET /products/category/{category}` - Lista produtos por categoria

## Comandos Disponíveis

Utilize o Makefile para operações comuns:

- `make up` - Inicia todos os serviços
- `make down` - Para todos os serviços
- `make logs` - Visualiza logs
- `make ps` - Lista serviços em execução
- `make build` - Reconstrói os containers
- `make rebuild` - Reconstrói os containers do zero

## Banco de Dados

O sistema utiliza PostgreSQL para persistência de dados. O banco é inicializado automaticamente ao iniciar os serviços.

## Troubleshooting

Se encontrar problemas ao executar o sistema:

1. Verifique se as portas 5173, 8000 e 5432 estão disponíveis
2. Verifique os logs com `make logs`
3. Tente reconstruir os containers com `make rebuild`
