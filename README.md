# usuarios-crud-project
Teste de Desenvolvedor Full Stack (Vue.js + Laravel) - CRUD de Usuários com Vuetify
------------------------------------------------------------------------------------------------------
1. Laravel : Certifique-se de ter o PHP instalado (versão >= 8.1) e o Composer.
2. Node.js: Certifique-se de ter o Node.js instalado (versão >= 14).
3. MySQL: Configure um banco de dados MySQL.
4. NPM/Yarn: Necessário para gerenciar pacotes no Vue.js.

## Configuração do Back-End (Laravel)

1. Clone o projeto Laravel na pasta `usuarios-crud`:
    ```bash
    cd usuarios-crud
    ```
2. Instale as dependências do Laravel:
    ```bash
    composer install
    ```
3. Copie o arquivo de exemplo `.env` e configure as credenciais do banco de dados:
    ```bash
    cp .env.example .env
    ```
   Atualize as seguintes informações no arquivo `.env`:
    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=usuarios_crud
    DB_USERNAME=seu_usuario
    DB_PASSWORD=sua_senha
    ```
4. Gere a chave da aplicação:
    ```bash
    php artisan key:generate
    ```
5. Execute as migrações para criar as tabelas no banco de dados:
    ```bash
    php artisan migrate
    ```
6. Inicie o servidor de desenvolvimento:
    ```bash
    php artisan serve
    ```

O back-end estará disponível em `http://127.0.0.1:8000`.

## Configuração do Front-End (Vue.js)

1. Clone o projeto Vue.js na pasta `usuarios-crud-frontend`:
    ```bash
    cd usuarios-crud-frontend
    ```
2. Instale as dependências do Vue.js:
    ```bash
    npm install
    ```
3. Configure a URL do back-end no arquivo `src/axios.js` (caso necessário):
    ```javascript
    axios.defaults.baseURL = 'http://127.0.0.1:8000/api';
    ```
4. Inicie o servidor de desenvolvimento do Vue.js:
    ```bash
    npm run serve
    ```

O front-end estará disponível em `http://localhost:8080`.

## Estrutura do Projeto

- **Back-end (Laravel)**:
  - `database/migrations/`: Contém as migrações para criar a tabela de usuários.
  - `app/Models/`: Contém o modelo do usuário.
  - `app/Http/Controllers/`: Contém o controlador com as rotas CRUD.

- **Front-end (Vue.js)**:
  - `src/components/`: Contém os componentes Vue para listagem e gerenciamento de usuários.




## Observações

- Certifique-se de iniciar o back-end antes do front-end.
- Caso utilize Docker, adapte os comandos para seu ambiente.




## Suporte

Nivanderson Coutinho 
E-Mail: nivanderson.coutinho@gmail.com
Contato: (92)99518-2213
