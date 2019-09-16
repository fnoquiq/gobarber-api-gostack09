<img src="https://s3.us-east-2.amazonaws.com/gobarber-img/logo.svg" height = "150"/>

# APP GOBARBER

- Api criado no bootcamp Rocketseat

![Bootcamp](https://rocketseat.com.br/static/images/update/bootcamp.svg)

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
  
 ### INSTALAÇÃO:
 
  - Instale o [yarn](https://yarnpkg.com/en/docs/install#debian-stable) e o [nodeJS](https://nodejs.org/en/download/)
  - Primeiramente você precisará ter o [docker](https://www.docker.com/get-started) instalado em sua máquina.
  - Fazer a instalação do DB, pelo terminal usando `sudo docker run --name database -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres`.
  - Criar uma database com o nome "gobarber". Obs: Recomendo o uso do [postbird](https://electronjs.org/apps/postbird) para fazer a criação do banco
  - No projeto usar `yarn install` para instalar todas as dependências do projeto.
  - Além disso, `yarn sequelize db:migrate` , para criar a base de dados.
  - Após, executar `yarn dev` para iniciar a aplicação.
