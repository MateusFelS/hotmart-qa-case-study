# SM-001 — Validação tardia de nome composto por espaços

## Fluxo

Cadastro e configuração de produto

## Cenário

Informar somente espaços no campo "Nome".

## Comportamento atual

O sistema permite avançar pelas etapas e apresenta
"Nome não encontrado" somente na etapa final.

## Oportunidade de melhoria

Realizar a validação na própria etapa do campo e apresentar
uma mensagem orientativa ao usuário.

## Impacto

O usuário precisa avançar pelo fluxo até descobrir que o
nome informado não é válido.

## Prioridade sugerida

Média

## Evidência

- [Validação tardia](https://github.com/user-attachments/assets/9d9c6a4b-23d9-4339-b45c-7aca9990c7bf)
