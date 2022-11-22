# NG-Cash 

Aplicação voltada para criação de novos usuários na plataforna, com página de login inclusa, cujo foco em fazer e registrar transações entre usuários no banco de dados.

# Rodando no Docker

## Clone esse repositório
```bash
  git clone git@github.com:Alan-Junqueira/ng-cash.git
```

## Clone projeto frontend
- Dentro da pasta que fizer o clone deste arquivo, clonar o frontend e o backend em suas respectivas pastas.

Clone o frontend

```bash
 git clone git@github.com:Alan-Junqueira/ng-cash-frontend.git
```

Clone o backend

```bash
 git clone git@github.com:Alan-Junqueira/ng-cash-backend.git
```

### Com todos os projetos clonados e na sua máquina, é necessário fazer alguns pequenos ajustes.

- No arquivo Dockerfile do projeto do frontend e do projeto do backend, o WORKDIR deve ser alterado de acordo com sua maquina.

- No meu frontend por ex, está assim o Dockerfile: WORKDIR /home/alan/development/ng-cash/frontend

- No seu caso, deve modificar para especificar o local que esta na sua maquina.

- Com tudo configurado, na pasta que esta o docker-compose.yml, execute os seguintes comandos na sequencia.

```bash
docker-compose build
```

```bash
docker-compose up ou docker-compose up -d
```


Pronto, containers rodando, basta acessar a aplicação e ver funcionando.

# Rodando Localmente

- Versão node utilizada: node`18.12.0`
## Rodando localmente frontend

Clone o projeto

```bash
  git clone git@github.com:Alan-Junqueira/ng-cash-frontend.git
```

Entre no diretório do projeto

```bash
  cd ng-cash-frontend
```

Instale as dependências

```bash
  npm install
```

Inicie o servidor

```bash
  npm run dev
```

## Rodando localmente backend

### Variáveis de Ambiente

Para rodar esse projeto, você vai precisar adicionar as seguintes variáveis de ambiente no seu .env

`DATABASE_URL`

`JWT_SECRET_KEY`

Mude o arquivo `example.env`, para `.env`, e modifique de acordo com os dados do seu banco PostgreSQL.

Clone o projeto

```bash
  git clone git@github.com:Alan-Junqueira/ng-cash-backend.git
```

Entre no diretório do projeto

```bash
  cd ng-cash-backend
```

Instale as dependências

```bash
  npm install
```

Inicie o servidor, crie o banco de dados e execute as migrations

```bash
  npm run dev
```

Caso já tenha executado `npm run dev`

```bash
  npm start
```


# Funcionalidades

## Frontend

- Página de cadastro.
- Página de login.
- Página de transferências.
- Filtro de transferências por data, cash-in e cash-out.

## Backend

### Rotas de usuários (users)
- Rota que pega todos os usuários.
- Rota que pega usuário por id.
- Rota que edita usuário por id.
- Rota que deleta usuário por id.
- Rota que cria novo usuáio.
- Rota que faz login de usuário.
- Rota que pega o usuário pelo token passado.

### Rotas da conta (account)
- Rota que pega todas as contas cadastradas.
- Rota que cria uma nova conta.
- Rota que pega o saldo atual da conta.
- Rota que pega a conta pelo id do usuário.
- Rota que edita a conta pelo id do usuário.
- Rota que deleta a conta pelo id do usuário.

### Rotas das transações (transactions)
- Rota que salva uma transação no banco de dados.
- Rota que pega as transações de um usuário por id.
