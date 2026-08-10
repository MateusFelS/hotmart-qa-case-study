# Sugestões de Melhoria

## SM-001 — Validação de nome composto somente por espaços

**Fluxo:** Cadastro e configuração de produto

**Cenário:**
Ao informar somente espaços no campo "Nome", o sistema permite avançar pelas etapas do cadastro.

**Comportamento atual:**
A validação ocorre somente na etapa final, quando o sistema apresenta a mensagem:

> "Nome não encontrado"

O usuário não é direcionado ao campo que precisa ser corrigido.

**Comportamento sugerido:**
Realizar a validação do campo "Nome" na própria etapa em que o dado é informado e impedir o avanço enquanto o valor contiver apenas espaços.

Sugere-se também uma mensagem mais específica, por exemplo:

> "Informe um nome válido para o produto."

**Impacto:**
A validação antecipada reduziria retrabalho e deixaria mais claro para o usuário qual informação precisa ser corrigida.

**Prioridade sugerida:** Média
