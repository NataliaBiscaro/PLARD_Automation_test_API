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

### ✅ Login de usuário
- Endpoint: `POST /accountrest/api/v1/login`
- Resultado: 200 OK — Token e sessionId recebidos

### ✅ Upload de imagem
- Endpoint: `POST /catalog/api/v1/product/image/{userId}/{source}/{color}`
- Headers:
  - Authorization: Bearer `<token recebido no login>`
- Resultado: 200 OK — Imagem atualizada (sem erro na API)

## Observações
- A imagem não foi refletida na interface do site mesmo com retorno `200 OK`.

## Evidências
Ver pasta `/evidencias`.

