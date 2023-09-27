# Aplicativo para Hostifrutis

#### Nesse projeto irei criar inicialmente o back-end do aplicativo, a api terá como principal ferramenta o Adonis JS, nele que irei criar a API, já o Front End será criado totalmente no Flutter, onde iremos dar o deploy do app para o Google Play.

# Inicio (Criando o projeto)
    Inicialmente temos que criar o projeto no Adonis JS ( A ordem de criação do Back end para o Front End ou do Front End para o back End é preferencial, vai do desenvolvedor escolher qual etapa irá concluir primeiro, no meu caso, prefiro criar o back End primeiro )

### (Etapa 1) Configurando o Adonis e criando o projeto:
    . node -v 
    . yarn create adonis-ts-app hello-world
    . node ace serve --watch
### Explicando a Etapa 1:
    * O comando (node -v) é utilizado para vizualizar a versão do Node Js Instalado no computador do desenvolvedor, é recomendado que seja utilizado a versão mais recente.

    * O comando (yarn create adonis-ts-app hello-world) é utilizado para criar o projeto do Adonis JS onde ele irá fornecer os principais plugins e ferramentas para criar o projeto, no meu caso eu criei o projeto com o Yarn, mas você pode escolher entre NPM, YARN ou PNPM, assim, você irá prosseguir e criar o projeto de acordo com o que pretende criar. Você encontrará as seguintes oções; API, WEB e Slim como estou criando uma API então escolhi a opção "API".

    * O comando (node ace serve --watch) é utilizado depois de criar a aplicação com o comando anterior, ele serve para criar o ambiente de desenvolvimento com o servidor, onde o comando também irá sempre está se atualizando automaticamente.

### (Etapa 2) Conectando ao banco de dados
    . npm i @adonisjs/lucid
    . node ace configure @adonisjs/lucid
        . Opção MySql/MariaDB
        . Aguarda a instalação
        . Opção para mostrar as instruções no terminal (Opcional)
    . Após concluir a etapa anterior, vamos deixar o arquivo (env) configrado de acordo com o nosso Banco de Dados
        DB_CONNECTION=mysql
        MYSQL_HOST=localhost
        MYSQL_PORT=3306 -> Porta de conexão do Banco de Dados
        MYSQL_USER=Administrador -> Nome do Usuário administrador do MySQL
        MYSQL_PASSWORD=Senha123 -> Senha do Banco de Dados
        MYSQL_DB_NAME=db_app -> Nome do Banco de Dados Criado

### (Etapa 3) Configurando o MySQL Workbench
    O MySQL iremos configurar de forma bem simples, só iremos criar o bancode dados mesmo e o LUCID (Adonis JS) fará o resto:

    . Connection name: Nome do Banco de Dados
    . Hostname: 127.0.0.1
    . username: administrador (Preferêncial)
    . Password: 123456 (preferêncial)

    . Charset Location: utf8mb4 / utf8mb4_unicode_ci

    . Apply
    . Finish

    Para testarmos iremoscolocar o comando no terminal do VS Code "node ace migration:run" para gerar as tabelas padrões do Adonis JS.