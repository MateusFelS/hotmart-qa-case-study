# SM-002 — Padronização da validação de dados nos campos do checkout

## Fluxo

Página do Produto → Checkout

## Cenário

Inserir dados incompatíveis com o formato esperado nos campos de Nome,
CPF/CNPJ e Celular.

## Comportamento atual

Os campos apresentam comportamentos diferentes durante a inserção de
dados inválidos.

Em alguns campos, determinados caracteres incompatíveis podem ser
digitados e o sistema realiza a validação posteriormente.

Em outros campos, a entrada incompatível é bloqueada imediatamente
durante a digitação.

## Exemplo observado

- Campo Nome: permite a inserção de números e realiza a validação posteriormente.
- Campo CPF/CNPJ: permite determinados caracteres inválidos e realiza a validação posteriormente.
- Campo Celular: apresenta comportamento diferente, restringindo determinados caracteres durante a digitação.

## Oportunidade de melhoria

Avaliar a possibilidade de padronizar o comportamento de validação dos
campos do checkout, tornando mais consistente a forma como entradas
incompatíveis são tratadas durante o preenchimento.

Independentemente da abordagem escolhida (bloqueio durante a digitação
ou validação posterior), o comportamento e o feedback apresentados ao
usuário poderiam seguir um padrão consistente entre os campos.

## Impacto

A diferença de comportamento pode gerar uma experiência inconsistente
durante o preenchimento do formulário e dificultar a compreensão de
quais tipos de entrada são aceitos em cada campo.

## Prioridade sugerida

Média

## Evidências

- [Validação Inconsistente](https://github.com/user-attachments/assets/df036a49-5d25-4672-b288-2215037af29a)
