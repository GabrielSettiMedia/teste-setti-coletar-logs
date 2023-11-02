# Teste Técnico - Desenvolvimento Back-End em JavaScript

## Descrição

Este teste técnico tem como objetivo avaliar suas habilidades em desenvolvimento back-end em JavaScript. Você será responsável por criar um pequeno serviço que recebe eventos da plataforma via uma rota /webhook, armazena esses eventos em um banco de dados SQLite e fornece uma rota /logs para recuperar esses eventos, permitindo filtrar por tipo e data.

## Instruções

1. Crie um servidor Node.js utilizando o framework Express para gerenciar as rotas.

2. Implemente uma rota `/webhook` que aceite eventos JSON no seguinte formato:

```json
{
  "type": "click",
  "date_time": "2023-11-02T08:57:07-05:00",
  "campaign": {
    "id": "1",
    "status": "1",
    "name": "[EMP] Email 02 - ES",
    "type": "single",
    "recipients": "1",
    "message": {
      "id": "1",
      "subject": "TITLE"
    }
  }
}
```

3. Salve os campos type, date_time e campaign.name no banco de dados SQLite como se fosse um registro de log.

4. Implemente uma rota `/logs` que permita a recuperação dos registros de log armazenados no banco de dados. Essa rota deve suportar o seguinte parâmetro de consulta:

- type (filtro opcional): Recupere registros com um tipo específico.

5. Implemente a autenticação por meio de um token de autenticação no cabeçalho da solicitação para a rota `/logs`. O token deve ser verificado antes que o usuário possa acessar os registros.

6. Use um ORM (Object-Relational Mapping) para interagir com o banco de dados SQLite. Recomendamos o uso de um ORM como o Sequelize ou algum equivalente.

7. Forneça uma documentação clara no código sobre como configurar e executar o projeto.

8. Certifique-se de que seu código seja organizado, comentado e siga as melhores práticas de desenvolvimento.

## Critérios de Avaliação

- Precisão na implementação das rotas `/webhook` e `/logs`.
- Uso adequado de Express para criar o servidor.
- Correta implementação de um banco de dados SQLite e uso de um ORM.
- Implementação de autenticação por token.
- Boas práticas de codificação, organização e documentação.