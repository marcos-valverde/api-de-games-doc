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

### POST /auth 
Esse endpoint é responsável por fazer o processo de login
#### Parametros
email: E-mail do usuário cadastrado no sistema
password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail

Exemplo:
```
{
    "email": "marcos@gmail.com",
    "password": "m4rc0s"
}
```
#### Respostas
OK! 200
Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar os endpoints protegidos da API.

Exemplo de resposta:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJtYXJjb3NAZ21haWwuY29tIiwiaWF0IjoxNjkxMTE2NzYyLCJleHAiOjE2OTEyODk1NjJ9.u84g9ADktJaoMuXNYPnyhCidK8J1zJxlTXWiV05hmhc"
}
```
#### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição
Motivos: E-mail ou senha inválida

Exemplo de resposta:
```
{
    "err": "Credências invalida"
}
