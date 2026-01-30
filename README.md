# Sobre o Projeto

O projeto **DSList - Lista de Games** foi desenvolvido com o objetivo de aprimorar habilidades técnicas e consolidar conhecimentos em desenvolvimento backend e APIs REST.

A aplicação permite que o usuário consulte e organize listas de jogos, estruturadas nas categorias **Aventura e RPG** e **Jogos de Plataforma**, armazenadas em um banco de dados relacional. Para o mapeamento das entidades, é utilizada a **JPA (Java Persistence API)**, que relaciona as classes do sistema com as tabelas do banco de dados.

O banco de dados PostgreSQL é executado em um container Docker por meio do Docker Compose, e os dados são inicializados automaticamente utilizando o arquivo `import.sql`, responsável por popular o sistema com listas e jogos previamente cadastrados.

A API REST disponibiliza endpoints para consulta das informações organizadas por categorias.

## Modelo de Domínio DSList
![Modelo de Domínio DSList](images/dslist-model.png)

## Tecnologias

### Backend
- Java
- Spring Boot

### Banco de Dados
- PostgreSQL
- SQL

### Ferramentas
- Docker Compose
- Postman

## Endpoints

### Games
- **GET** `/games` — Retorna todos os jogos
- **GET** `/games/{id}` — Retorna um jogo específico

### Lists
- **GET** `/lists` — Retorna todas as listas
- **GET** `/lists/{id}/games` — Retorna todos os jogos de uma lista
- **PUT** `/lists/{id}/replacement` — Altera a posição de um jogo na lista

## Prints da aplicação

### Games / Postman
![Games postman](images/games-postman.png)

### Lista 2 / PostgreSQL
![Lista 2](images/list2-postgres.png)

### Posição dos games nas listas / PostgreSQL
![Posição dos games na lista](images/position-games-lists-postgres.png)

### Alterar a posição de um game na lista / Postman
![Alterar posição](images/replacement-postman.png)

## Docker

O banco de dados PostgreSQL é executado via Docker Compose, utilizando o arquivo:

[docker-compose.yml](Aula3/docker-compose.yml)

### Execução do projeto

1. Faça o clone do repositório:
```bash
git clone https://github.com/kauegadelha/dslist.git
```
2. Abra o projeto em sua IDE (IntelliJ, VS Code, Eclipse, etc).

3. Execute a aplicação Spring Boot.

4. No terminal PowerShell como adminstrador, navegue até a pasta:
```bash
cd Aula3
```
5. Execute o Docker Compose:
```bash
docker-compose up -d
```
6. Acesse o PgAdmin no navegador:
```bash
http://localhost:5050
```
7. Credenciais:
- Email: me@example.com
- Senha: 1234567
