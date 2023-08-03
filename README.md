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

Exemplo de resposta:
```
[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 65,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    },
    {
        "id": 4,
        "title": "Naruto",
        "year": 2019,
        "price": 150
    },
    {
        "id": 2525
    }
]
```
#### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição
Motivos: Token inválido, Token expirado

Exemplo de resposta:
```
{
    "err": "Token inválido!"
}
```
