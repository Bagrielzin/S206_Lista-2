# S206 Lista - 2
Repositório da segunda lista do laboratório de S206

#Criar uma usuario do tipo aluno:
{
  "nome": "{{$randomFullName}}",
  "email": "{{$randomEmail}}",
  "password": "{{$randomPassword}}",
  "acesso": "ALUNO",
  "ativo":1
}

#Criar um usuario do tipo aluno faltando o campo senha:
{
  "nome": "{{$randomFullName}}",
  "email": "{{$randomEmail}}",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}

#Cria um ususario faltando nome e senha:
{
  "nome": "",
  "email": "{{$randomEmail}}",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}

#Criar um usuario faltando todos os dados:
{
  "nome": "",
  "email": "",
  "password": "",
  "acesso": "ALUNO",
  "ativo":1
}

#Criar usuario com o campo nome apenas com uma letra:
{
  "nome": "l",
  "email": "{{$randomEmail}}",
  "password": "{{$randomPassword}}",
  "acesso": "ALUNO",
  "ativo":1
}

