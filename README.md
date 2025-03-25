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
## Evidências:

![image](https://github.com/user-attachments/assets/7b19a99a-f322-423a-9dd1-2001d8271f13)
![image](https://github.com/user-attachments/assets/e7f4ecb5-d5f5-443c-97c3-4893c2063fda)



### ✅ Login de usuário
- Endpoint: `POST /accountrest/api/v1/login`
- Resultado: 200 OK — Token e sessionId recebidos
## Evidências:

![image](https://github.com/user-attachments/assets/bcb28e53-f39c-45fe-9fb5-187fc3c26a2e)
![image](https://github.com/user-attachments/assets/b63c9403-8005-4ab4-bbe6-db46aeac2eef)



### ✅ Upload de imagem
- Endpoint: `POST /catalog/api/v1/product/image/{userId}/{source}/{color}`
- Headers:
  - Authorization: Bearer `<token recebido no login>`
- Resultado: 200 OK — Imagem atualizada (sem erro na API)
## Observações
- A imagem não foi refletida na interface do site mesmo com retorno `200 OK`.
## Evidências:

![image](https://github.com/user-attachments/assets/0c49e001-a9cf-4eb8-9104-8fdbfa907943)
![image](https://github.com/user-attachments/assets/8dbd4f18-4820-4df9-8298-0578177b1160)





