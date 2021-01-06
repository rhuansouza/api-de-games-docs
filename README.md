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
##### Falha na Autenticação| 401
Caso esta resposta aconteça isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido ou Token expirado.
