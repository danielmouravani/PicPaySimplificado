# Authentication API

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

Este projeto é uma API construída usando **Java, Java Spring, H2 como banco de dados.**

Os testes unitários foram desenvolvidos com o objetivo de demonstrar como escrever testes unitários para aplicações Java Spring usando JUnit, Mockito e AssertJ.

## Índice

- [Installation](#Instalação)
- [Configuration](#Configuração)
- [Usage](#Uso)
- [API Endpoints](#api-endpoints)
- [Database](#database)

  ## Instalação

  1. Clone the repository:

```bash
git clone 
```

2. Instale dependências com Maven

## Uso

1. Inicie o aplicativo com Maven
2. A API estará acessível em http://localhost:8080

## API Endpoints
A API fornece os seguintes endpoints:


**GET USERS**
```markdown
GET /users - Retrieve a list of all users.
```
```json
[
    {
        "id": 1,
        "firstName": "Pedro",
        "lastName": "Silva",
        "document": "123456787",
        "email": "pedro@example.com",
        "password": "senha",
        "balance": 20.00,
        "userType": "MERCHANT"
    },
{
        "id": 4,
        "firstName": "Luckas",
        "lastName": "Silva",
        "document": "123456783",
        "email": "luckas@example.com",
        "password": "senha",
        "balance": 0.00,
        "userType": "COMMON"
    }
]
```

**POST USERS**
```markdown
POST /users - Cadastre um novo usuário no aplicativo

```
```json
{
    "firstName": "Lucas",
    "lastName": "Silva",
    "password": "senha",
    "document": "123456783",
    "email": "lucas@example.com",
    "userType": "COMMON",
    "balance": 10
}
```

**POST TRANSACTIONS**
```markdown
POST /transactions - Cadastrar uma nova transação entre usuários (COMMON para COMMON ou COMMON para MERCHANT)
```

```json

{
  "senderId": 4,
  "receiverId": 1,
  "value": 10
}
```

## Database
O projeto utiliza [H2 Database](https://www.h2database.com/html/tutorial.html) como banco de dados.
