# Api de Games
Esta api foi utilizada para estudo de api com Node utilizando JWT.
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK| 200
Caso esta resposta aconteça você irá receber a listagem de todos os games.

Exemplo de resposta:
```
[
    {
        "id": 10,
        "title": "Counter Strike",
        "price": 60,
        "year": 2018
    },
    {
        "id": 20,
        "title": "Dragon Ball",
        "price": 200,
        "year": 2020
    },
    {
        "id": 30,
        "title": "God of WAR",
        "price": 120,
        "year": 2017
    }
]
```
##### Falha na Autenticação| 401
Caso esta resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido ou Token expirado.

Exemplo de resposta:
```
{
    "err": "Token Inválido"
}
```

### POST /auth
Esse endpoint é responsável por fazer o processo de login.
#### Parametros
email: E-mail do usuário cadastrado no sistema.

password: Senha do usuário cadastrado no sistema.

Exemplo:
```
 {    
   "email":"teste@gmail.com",
   "password": 123
 }
 ```
#### Respostas
##### OK| 200
Caso esta resposta aconteça você irá receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:
```
{token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpfgfgfgZCI6MSwiZWhjhjh1haWwiOiJyaHVhbmNvc3RghghghhbnpvQGdtYWlsLmNvbSIsImlhdCI6MTYwOTg5ODM2NSwiZXhwIjoxNjEwMDcxMTY1fQ.LkQSH72EpmNJR7inOFNqbswoIpPWVkkN3ntTTs42BC8"}
```
##### Falha na Autenticação| 401
Caso esta resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: e-mail ou senha incorretos.

Exemplo de resposta:
```
{erro:"Credenciais Inválidas"}
```
