# Find A Friend API

## Requisitos
- Node.js v.18.x instalado
- Docker instalado
- Docker compose habilitado

## Setup
- Instalar dependências:
  ```bash
  npm install # or yarn
  ```
- Subir banco de dados com o docker-compose
  ```bash
    docker compose up -d
  ```
- Gerar migrations do banco
  ```bash
    npx prisma migrate dev
  ```
- Criar um arquivo .env e preencher as variáveis de acordo com o informado em .env.example


## Inicialização
```bash
npm run dev
```
---
### Regras da aplicação

- Deve ser possível cadastrar um pet
- Deve ser possível listar todos os pets disponíveis para adoção em uma cidade
- Deve ser possível filtrar pets por suas características
- Deve ser possível visualizar detalhes de um pet para adoção
- Deve ser possível se cadastrar como uma ORG
- Deve ser possível realizar login como uma ORG

### Regras de negócio

- Para listar os pets, obrigatoriamente precisamos informar a cidade
- Uma ORG precisa ter um endereço e um número de WhatsApp
- Um pet deve estar ligado a uma ORG
- O usuário que quer adotar, entrará em contato com a ORG via WhatsApp
- Todos os filtros, além da cidade, são opcionais
- Para uma ORG acessar a aplicação como admin, ela precisa estar logada