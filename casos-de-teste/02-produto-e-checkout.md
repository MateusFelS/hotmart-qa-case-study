# Casos de Teste - Página do Produto → Checkout

## Página do Produto

| ID     | Cenário                                      | Pré-condição                    | Dados de Teste                              | Resultado Esperado                                                        | Resultado Obtido                                                                 | Status      | Prioridade |
| ------ | -------------------------------------------- | ------------------------------- | ------------------------------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ----------- | ---------- |
| CT-001 | Verificar consistência das informações entre página do produto e checkout | Produto disponível publicamente | Nome, imagem, preço, descrição, parcelamento e autor | Informações apresentadas na página do produto devem corresponder às informações apresentadas no checkout | Nome, imagem, preço, descrição, parcelamento e autor permaneceram consistentes | ✅ Passou   | Alta       |

---

## Validação dos Campos

| ID     | Cenário                                  | Pré-condição             | Dados de Teste                       | Resultado Esperado                                                        | Resultado Obtido                                                                 | Status    | Prioridade |
| ------ | ---------------------------------------- | ------------------------ | ------------------------------------ | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | --------- | ---------- |
| CT-002 | Avançar com campos obrigatórios vazios   | Usuário no checkout      | Campos obrigatórios sem preenchimento | Sistema deve impedir o avanço e informar claramente os campos obrigatórios | Sistema impediu o avanço, exibiu mensagens claras e manteve o usuário na página | ✅ Passou | Alta       |
| CT-003 | Inserir caracteres inválidos nos campos  | Usuário no checkout      | Nome, CPF/CNPJ e celular com caracteres incompatíveis | Sistema deve aplicar comportamento consistente de validação nos campos | Nome, CPF/CNPJ e celular inicialmente permitem determinados caracteres inválidos, enquanto outros campos bloqueiam a entrada durante a digitação e exibem validação instantânea | ⚠️ Observação | Média      |

---

## Navegação e Persistência

| ID     | Cenário                              | Pré-condição                 | Dados de Teste                       | Resultado Esperado                                                        | Resultado Obtido                                                                 | Status    | Prioridade |
| ------ | ------------------------------------ | ---------------------------- | ------------------------------------ | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | --------- | --------- |
| CT-004 | Recarregar a página durante o checkout | Dados parcialmente preenchidos | Informações válidas preenchidas | Sistema deve preservar os dados preenchidos ou informar claramente sua perda | Após recarregar a página, os dados preenchidos permaneceram disponíveis         | ✅ Passou | Média      |
| CT-005 | Sair do checkout e retornar posteriormente | Dados parcialmente preenchidos | Informações válidas preenchidas | Sistema deve preservar os dados preenchidos ou informar claramente sua perda | Ao sair e retornar ao checkout, os dados anteriormente preenchidos permaneceram disponíveis | ✅ Passou | Média      |
