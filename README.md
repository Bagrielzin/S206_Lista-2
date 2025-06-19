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

## 2 - Criar um usuario do tipo aluno faltando o campo senha:
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

