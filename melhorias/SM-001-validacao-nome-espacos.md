# SM-001 — Validação tardia de nome composto por espaços

## Fluxo

Cadastro e configuração de produto

## Cenário

Informar somente espaços no campo "Nome".

## Comportamento atual

O sistema permite inserir somente espaços no campo "Nome" e avançar
pelas etapas do cadastro.

A validação ocorre somente na etapa final, quando o sistema apresenta
a mensagem "Nome não encontrado".

O usuário não é direcionado ao campo "Nome" para realizar a correção.

## Oportunidade de melhoria

Realizar a validação do campo "Nome" na própria etapa em que o dado é
informado, impedindo o avanço enquanto o campo contiver apenas espaços.

Também seria recomendável apresentar uma mensagem mais específica e
orientativa, por exemplo:

> "Informe um nome válido para o produto."

## Impacto

A validação tardia faz com que o usuário avance por etapas
desnecessariamente até descobrir que o nome informado não é válido.

Além disso, a mensagem "Nome não encontrado" pode dificultar a
identificação do problema, pois não indica claramente que o campo
"Nome" precisa ser corrigido.

## Prioridade sugerida

Média

## Evidência

- [Validação tardia](https://github.com/user-attachments/assets/9d9c6a4b-23d9-4339-b45c-7aca9990c7bf)
