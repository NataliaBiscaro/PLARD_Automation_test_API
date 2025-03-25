# Relatório de Testes - API Advantage Online Shopping

## Objetivo
Validar o funcionamento dos endpoints da API pública, incluindo:
- Consulta de produtos por ID
- Autenticação de usuários ADMIN
- Upload de imagem de produto

## Cenários Testados

### ✅ Registro de usuário ADMIN
- Endpoint: `POST /accountrest/api/v1/register`
- Resultado: 200 OK — Usuário criado com sucesso

![image](https://github.com/user-attachments/assets/7b19a99a-f322-423a-9dd1-2001d8271f13)


### ✅ Login de usuário
- Endpoint: `POST /accountrest/api/v1/login`
- Resultado: 200 OK — Token e sessionId recebidos

![image](https://github.com/user-attachments/assets/bcb28e53-f39c-45fe-9fb5-187fc3c26a2e)


### ✅ Upload de imagem
- Endpoint: `POST /catalog/api/v1/product/image/{userId}/{source}/{color}`
- Headers:
  - Authorization: Bearer `<token recebido no login>`
- Resultado: 200 OK — Imagem atualizada (sem erro na API)

![image](https://github.com/user-attachments/assets/0c49e001-a9cf-4eb8-9104-8fdbfa907943)

## Observações
- A imagem não foi refletida na interface do site mesmo com retorno `200 OK`.

## Evidências
Ver pasta `/evidencias`.

