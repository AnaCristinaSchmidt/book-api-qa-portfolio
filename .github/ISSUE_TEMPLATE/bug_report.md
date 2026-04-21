---
name: Bug report
about: Create a report to help us improve
title: ''
labels: ''
assignees: ''

---

## 🐞 Descrição
A API permite criar uma review com valor de rating acima do permitido.

## 🔁 Passos para reproduzir
1. Enviar requisição POST /books/:bookId/reviews
2. Informar rating = 15

## ⚠️ Resultado atual
Review criada com sucesso

## ✅ Resultado esperado
A API deve retornar erro 400, informando que o valor permitido é entre 1 e 10.

## 📊 Impacto
Dados inválidos podem ser armazenados no sistema, comprometendo a integridade das avaliações.

## 🧪 Evidência (opcional)
Exemplo de payload utilizado:
```json
{
  "rating": 15,
  "text": "Teste"
}
