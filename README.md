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
- Fazer a instalação do DB, pelo terminal usando `sudo docker run --name database -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres`.
- Criar uma database com o nome "gobarber". Obs: Recomendo o uso do [postbird](https://electronjs.org/apps/postbird) para fazer a criação do banco
- No projeto usar `yarn install` para instalar todas as dependências do projeto.
- Além disso, `yarn sequelize db:migrate` , para criar a base de dados.
- Após, executar `yarn dev` para iniciar a aplicação.

---

### Rotas das API:

- Segue abaixo a lista de rotas disponíveis pela api GOBARBER

#### Sessions: ```BASE_URL/sessions```

  - **(POST)** *Create* -> Esta rota é usada para fazer a autenticação com a API e dela será retornada uma token bearer, que sera usada nas rotas que possuirem **@token_auth**.

#### Users: ```BASE_URL/users```

  - **(POST)** *Create* -> Esta rota rota é usada para realizar o cadastramento de usuários
  
  - **(PUT)** *Update* @token_auth -> Esta rota pode ser usada para editar informações básicas do usuário, como também para alterar a senha e linkar uma foto de avatar (desde que a foto de avatar já tenha sido criada no servidor).

#### Schedule: ```BASE_URL/schedule```

  - **(GET)** *List* @token_auth -> Esta rota é usada para retornar os agendamentos do provider logado

#### Appointments: ```BASE_URL/appointments```

  - **(POST)** *Create* @token_auth -> Esta rota é usada para cadastramento de agendamentos
  
  - **(GET)** *List* @token_auth -> Esta rota é usada para listar os agendamentos

#### Provider: ```BASE_URL/provider```

  - **(GET)** *List* @token_auth -> Esta rota é usada para listar todos os usuários que são prestadores de serviço

#### Files: ```BASE_URL/files```

  - **(POST)** *Create* @token_auth -> Esta rota é usada para servir de upload de avatar do usuário, que posteriormente pode ser linkada na edição do usuário com o ID deste.
  
---
