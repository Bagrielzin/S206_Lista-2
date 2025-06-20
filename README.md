# S206 Lista - 2
Repositório da segunda lista do laboratório de S206

<br>

# Request bases utilizados

<br>

## Obtendo token
### GET
Endpoint: https://fetin-api.confianopai.com/get-csrf-token

## Fazendo login
### POST
Endpoint: https://fetin-api.confianopai.com/login
<br>
Conteúdo do body:
```javascript
{
    "username": "matheusb@",
    "password": "123"
}
```

<br>

# Testes - Alunos

<br>

## 1 - Criar uma usuario do tipo aluno:
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "{{$randomFullName}}",
  "email": "{{$randomEmail}}",
  "password": "{{$randomPassword}}",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>

## 2 - Criar um usuario do tipo aluno faltando o campo senha (negativo):
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "{{$randomFullName}}",
  "email": "{{$randomEmail}}",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>

## 3 - Cria um ususario faltando nome e senha:
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "",
  "email": "{{$randomEmail}}",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>

## 4 - Criar um usuario faltando todos os dados:
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "",
  "email": "",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>

## 5 - Criar usuario com o campo nome apenas com uma letra:
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "l",
  "email": "{{$randomEmail}}",
  "password": "{{$randomPassword}}",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>

##  6 - Criar um usuario sem o campo email:
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Aluno/add
<br>
Conteúdo do body:
```javascript
{
  "nome": "{{$randomFullName}}",
  "email": "",
  "password": "{{$randomPassword}}",
  "acesso": "ALUNO",
  "ativo":1
}
```

<br>
<br>

# Testes - Projetos

<br>

## Teste 1 - Lista de pojetos
### GET
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/all

<br>

## Teste 2 - Busca de time pelo seu número
### GET
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/442

<br>

## Teste 3 - Buscando time com número inexistente
### GET
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/9999

<br>

## Teste 4 - Criar um novo time sem alunos
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/create
<br>
```json
"body": {
    "mode": "formdata",
    "formdata": [
        {
            "key": "titulo",
            "value": "Time sem aluno",
            "type": "text"
        },
        {
            "key": "orientador_email",
            "value": "felipeb@inatel.br",
            "type": "text"
        },
        {
            "key": "status",
            "value": "ativo",
            "type": "text"
        },
        {
            "key": "paralela",
            "value": "paralela",
            "type": "text"
        },
        {
            "key": "email_aluno1",
            "value": "",
            "type": "text"
        },
        {
            "key": "email_aluno2",
            "value": "",
            "type": "text"
        },
        {
            "key": "email_aluno3",
            "value": "",
            "type": "text"
        },
        {
            "key": "email_aluno4",
            "value": "",
            "type": "text"
        }
    ]
    },
```

<br>

## Teste 5 - Criar um time com aluno repetido
### POST
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/create
<br>
```json
"body": {
    "mode": "formdata",
    "formdata": [
        {
            "key": "titulo",
            "value": "Time com aluno repetido",
            "type": "text"
        },
        {
            "key": "orientador_email",
            "value": "felipeb@inatel.br",
            "type": "text"
        },
        {
            "key": "status",
            "value": "ativo",
            "type": "text"
        },
        {
            "key": "paralela",
            "value": "paralela",
            "type": "text"
        },
        {
            "key": "email_aluno1",
            "value": "16375171Aluno@inatel.br",
            "type": "text"
        },
        {
            "key": "email_aluno2",
            "value": "",
            "type": "text"
        },
        {
            "key": "email_aluno3",
            "value": "",
            "type": "text"
        },
        {
            "key": "email_aluno4",
            "value": "",
            "type": "text"
        }
    ]
    },
```

<br>

## Teste 6 - Atualiza status da equipe 442
### PUT
Endpoint: https://fetin-api.confianopai.com/api/v1/Time/UpdateStatus
<br>
```json
"body": {
    "mode": "formdata",
    "formdata": [
        {
            "key": "numeroGrupo",
            "value": "442",
            "type": "text"
        },
        {
            "key": "status",
            "value": "inativo",
            "type": "text"
        }
    ]
},
```

<br>

