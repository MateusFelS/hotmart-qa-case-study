# Casos de Teste - Cadastro e Configuração de Produto

## Validação do Nome do Produto

| ID     | Cenário                                      | Pré-condição                    | Dados de Teste                                  | Resultado Esperado                                                        | Resultado Obtido                                                                 | Status              | Prioridade |
| ------ | -------------------------------------------- | ------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------- | ---------- |
| CT-001 | Cadastrar produto sem informar o nome        | Usuário na etapa de cadastro    | Nome: vazio                                      | Sistema deve impedir o avanço e informar que o campo é obrigatório       | Sistema impediu o avanço e exibiu mensagem de validação                         | ✅ Passou            | Alta       |
| CT-002 | Cadastrar produto com nome de um caractere   | Usuário na etapa de cadastro    | Nome: `a`                                        | Sistema deve aceitar o nome caso esteja dentro da regra de tamanho válida | Nome com um caractere foi aceito                                                 | ⚠️ Não classificável | Média      |
| CT-003 | Cadastrar produto com nome de 255 caracteres | Usuário na etapa de cadastro    | Nome com 255 caracteres                          | Sistema deve aceitar o nome caso 255 seja o limite máximo permitido       | Nome com 255 caracteres foi aceito                                               | ✅ Passou            | Média      |
| CT-004 | Cadastrar produto com nome acima de 255 caracteres | Usuário na etapa de cadastro | Nome com 256 caracteres                          | Sistema deve impedir o cadastro ou limitar a entrada ao máximo permitido | Sistema bloqueou a entrada acima de 255 caracteres                              | ✅ Passou            | Média      |
| CT-005 | Cadastrar produto com espaços no início e fim | Usuário na etapa de cadastro  | Nome: `   a   b   `                              | Sistema deve tratar os espaços conforme a regra definida para o campo     | Sistema aceitou o valor com espaços no início, entre os caracteres e no final    | ⚠️ Não classificável | Média      |
| CT-006 | Cadastrar produto contendo somente espaços | Usuário na etapa de cadastro | Nome: `     ` | Sistema deve identificar que o campo não contém um nome válido e informar o problema na própria etapa do campo | Sistema permitiu avançar nas etapas e somente no último passo exibiu a mensagem "Nome não encontrado" | ⚠️ Sugestão de melhoria | Média |
| CT-007 | Inserir quebra de linha no nome               | Usuário na etapa de cadastro   | Nome contendo quebra de linha                   | Sistema deve impedir caracteres de quebra de linha no campo               | Sistema não permitiu a inserção de quebra de linha                              | ✅ Passou            | Média      |
| CT-008 | Cadastrar produto com caracteres especiais    | Usuário na etapa de cadastro   | Nome: `@#$`                                     | Sistema deve aceitar ou rejeitar conforme as regras de caracteres do campo | Sistema permitiu o cadastro com os caracteres informados                        | ⚠️ Não classificável | Média      |
| CT-009 | Cadastrar produto utilizando emojis            | Usuário na etapa de cadastro   | Nome: `😀😁`                                    | Sistema deve aceitar ou rejeitar emojis conforme a regra definida         | Sistema permitiu o cadastro com emojis                                           | ⚠️ Não classificável | Baixa      |
| CT-010 | Cadastrar produto contendo marcação HTML       | Usuário na etapa de cadastro   | Nome: `<b>teste</b>`                            | Sistema deve tratar a entrada conforme a regra de caracteres do campo     | Sistema permitiu o cadastro e exibiu literalmente `<b>teste</b>`                | ⚠️ Não classificável | Média      |

---

## Validação de Campos Obrigatórios

| ID     | Cenário                                  | Pré-condição                 | Dados de Teste                    | Resultado Esperado                                                  | Resultado Obtido                                                     | Status      | Prioridade |
| ------ | ---------------------------------------- | ---------------------------- | ---------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------- | ----------- | ---------- |
| CT-011 | Tentar avançar com campos obrigatórios vazios | Usuário na etapa de cadastro | Campos obrigatórios sem preenchimento | Sistema deve impedir o avanço e informar quais campos são obrigatórios | Sistema impediu o avanço e exibiu mensagens de erro claras          | ✅ Passou   | Alta       |

---

## Navegação e Persistência dos Dados

| ID     | Cenário                                      | Pré-condição                          | Dados de Teste                                  | Resultado Esperado                                                   | Resultado Obtido                                                   | Status      | Prioridade |
| ------ | -------------------------------------------- | ------------------------------------- | ------------------------------------------------ | -------------------------------------------------------------------- | ------------------------------------------------------------------ | ----------- | ---------- |
| CT-012 | Avançar e retornar entre as etapas            | Dados preenchidos na etapa de cadastro | Informações válidas preenchidas                  | Sistema deve permitir retornar à etapa anterior mantendo os dados   | Sistema retornou à etapa anterior mantendo os dados preenchidos    | ✅ Passou   | Alta       |
| CT-013 | Recarregar a página durante o cadastro        | Dados preenchidos na etapa de cadastro | Informações válidas preenchidas                  | Sistema deve preservar os dados ou informar claramente a perda deles | Após recarregar, os dados permaneceram preenchidos                 | ✅ Passou   | Alta       |

---

## Upload de Arquivo

| ID     | Cenário                                  | Pré-condição                    | Dados de Teste                          | Resultado Esperado                                                        | Resultado Obtido                                                                 | Status                       | Prioridade |
| ------ | ---------------------------------------- | ------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------------- | ---------- |
| CT-014 | Realizar upload de arquivo válido         | Usuário na etapa de upload     | Arquivo JPG/PNG dentro do limite          | Sistema deve aceitar o arquivo e permitir continuar                      | Arquivo válido foi aceito corretamente                                          | ✅ Passou                   | Alta       |
| CT-015 | Realizar upload de formato não documentado | Usuário na etapa de upload     | Arquivo `.jfif`                           | Sistema deve aceitar somente os formatos oficialmente suportados          | Sistema aceitou o arquivo `.jfif`, embora a descrição apresente JPG e PNG       | ⚠️ Necessita investigação   | Média      |
| CT-016 | Realizar upload de arquivo acima do limite | Usuário na etapa de upload     | Arquivo acima do limite permitido          | Sistema deve bloquear o arquivo e informar o motivo                      | Sistema bloqueou o arquivo e exibiu mensagem de erro clara                      | ✅ Passou                   | Alta       |
