<img src="https://s3.us-east-2.amazonaws.com/gobarber-img/logo.svg" height = "150"/>

# APP GOBARBER

- Api criado no bootcamp Rocketseat

![Bootcamp](https://rocketseat.com.br/static/images/update/bootcamp.svg)

---

### Ferramentas utilizadas:

- Yarn
- Express
- Sequelize {sequelize, sequelize-cli, pg, pg-hstore}
- Husky
- ESLint
- Prettier
- Bcryptjs
- Date-fns
- Jsonwebtoken
- Multer
- Yup
- Nodemon
- Sucrase
- VSCode

---

### INSTALAÇÃO:

- Instale o [yarn](https://yarnpkg.com/en/docs/install#debian-stable) e o [nodeJS](https://nodejs.org/en/download/)
- Primeiramente você precisará ter o [docker](https://www.docker.com/get-started) instalado em sua máquina.
- Nesta aplicação é necessário o uso de dois bancos de dados, sendo eles o [PostgreSQL](https://www.postgresql.org/) e o [MongoDB](https://www.mongodb.com/), para rodar o container, basta executar pelo terminal:
- Para o container do PostgreSQL: `sudo docker run --name postgresbarber -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres`.
- Para o container do MongoDB: `sudo docker run --name mongobarber -p 27017:27017 -d -t mongo`.
- Criar uma database no PostgreSQL com o nome "gobarber". Obs: Recomendo o uso do [postbird](https://electronjs.org/apps/postbird) para fazer a criação do banco e visualização dos dados.
- Já para o MongoDB, o banco é criado automaticamente pela aplicação com o nome de gobarber, porém recomendo o uso do [MongoDB Compass](https://www.mongodb.com/products/compass) para visualização dos dados no banco
- No projeto usar `yarn install` para instalar todas as dependências.
- Além disso, `yarn sequelize db:migrate` , para estruturar a base de dados.
- Após, executar `yarn dev` para levantar a aplicação.

---

### Rotas das API:

- Segue abaixo a lista de rotas disponíveis pela api GOBARBER

#### Sessions: `BASE_URL/sessions`

- **(POST)** _Create_ -> Esta rota é usada para fazer a autenticação com a API e dela será retornada uma token bearer, que sera usada nas rotas que possuirem **@token_auth**.

#### Users: `BASE_URL/users`

- **(POST)** _Create_ -> Esta rota rota é usada para realizar o cadastramento de usuários

- **(PUT)** _Update_ @token_auth -> Esta rota pode ser usada para editar informações básicas do usuário, como também para alterar a senha e linkar uma foto de avatar (desde que a foto de avatar já tenha sido criada no servidor).

#### Schedule: `BASE_URL/schedule`

- **(GET)** _List_ @token_auth -> Esta rota é usada para retornar os agendamentos do provider logado

#### Appointments: `BASE_URL/appointments`

- **(POST)** _Create_ @token_auth -> Esta rota é usada para cadastramento de agendamentos

- **(GET)** _List_ @token_auth -> Esta rota é usada para listar os agendamentos

#### Provider: `BASE_URL/provider`

- **(GET)** _List_ @token_auth -> Esta rota é usada para listar todos os usuários que são prestadores de serviço

#### Files: `BASE_URL/files`

- **(POST)** _Create_ @token_auth -> Esta rota é usada para servir de upload de avatar do usuário, que posteriormente pode ser linkada na edição do usuário com o ID deste.

---
