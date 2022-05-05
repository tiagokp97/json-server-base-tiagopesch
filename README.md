### URL base da API:

https://json-server-tiagokp97.herokuapp.com/

# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

Exemplo de usuário cadastrado

"users": [
{
"email": "email@mail.com",
"password": "Sua senha",
"name": "nome",
"age": 20,
"id": 1
}
]

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

Retorno esperado:

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InRpYWdvQGdtYWlsLmNvbSIsImlhdCI6MTY1MTc3NDU2NSwiZXhwIjoxNjUxNzc4MTY1LCJzdWIiOiIyIn0.GmxI8ZI3cPnCsdQ8zNaKFcpCU6TRGid8f00P4l7Pc0I",
"user": {
"email": "email@mail.com",
"id": 1
}

# Postar produtos

O usuário deve estar logado e também deverá ser passado o token/bearer no corpo da requisição.

{
"type": "products",
"name": "nome do produto",
"userId": Numero do id do usuário (type number)

}
