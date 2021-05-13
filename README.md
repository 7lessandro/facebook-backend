# Comandos Gerais AdonisCLI v5

## Iniciar Projeto Adonis

```
npm init adonis-ts-app@latest hello-world
```

## Selecionar Tipo de Projeto

```
API Server -> Model & Controller
Web Application -> MVC (Model, View & Controller)
```

## Criar Controller

```
node ace make:controller {{name} -r
```

## Criar Model

```
node ace make:model {{name}}
```

## Instalar ORM Lucid

```
npm i @adonisjs/lucid
```

## Selecionar o Banco de Dados

```
node ace configure @adonisjs/lucid
```

## Criar Migration

```
node ace make:migration {{name}}
```

## Gerar/Desfazer Migration

```
node ace migration:run
node ace migration:rollback
```

## Atualizar Tabela c/ Migration

```
node ace make:migration deletar_adicionar_coluna_nome --table={{nome da tabela que vai atualizar}}
```

## Listar Rotas Criadas

```
node ace list:routes
```

## Instalar Autenticação 
```
npm i @adonisjs/auth
node ace invoke @adonisjs/auth
```

## Criar e Rodar Seeder 

```
node ace make:seeder {{ name }}
node ace db:seed
``` 

## Criar Middleware

```
node ace make:middleware {{ name }}
``` 

## Criar Validação

```
node ace make:validator {{ name }}
``` 


# Comandos Docker

Install [Docker Compose](https://docs.docker.com/compose/install/).

```bash
# Create container with MySQL
$ docker-compose up -d

# Create database structure
$ node ace migration:run

# install dependencies
$ npm install

# server with changes watcher
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start
```

# Anotações

```bash
- Relacionamento: Importar o Decorator, e a declaração da interface do type (belongsTo - BelongsTo) e depois alterar as informações na sequência -> Migration, Model & Controller.

- O método auth.authenticate faz com que você pegue todas informações da sessão do usuário logado.

- É possível utilizar um Decorator computed() para retirar apenas algumas informações de dentro do model.
```
