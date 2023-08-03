# API de Games
Esta API é utilizada para tal e tal....
## Endpoints
### GET /games 
Esse endpoint é responsável por retornar a listagem de todos os games cadastrado no Banco de Dados
#### Parametros
Nenhum
#### Respostas
OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games
#### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição
Motivos: Token inválido, Token expirado
