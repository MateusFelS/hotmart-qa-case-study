# Plano de Testes

## Informações Gerais

| Item        | Valor                                      |
| ----------- | ------------------------------------------ |
| Projeto     | QA Study - Hotmart                         |
| Módulos     | Cadastro de Produto e Checkout             |
| Responsável | Mateus Felipe dos Santos                   |
| Versão      | 1.0                                        |
| Data        | 10/08/2026                                 |

---

# Objetivo

Avaliar o comportamento de funcionalidades públicas da plataforma Hotmart, com foco no cadastro e configuração de produtos e no fluxo de página do produto até o checkout, verificando validações, regras de negócio, consistência das informações, navegação e experiência do usuário.

---

# Escopo

## Funcionalidades contempladas

- Cadastro e configuração de produto
- Validação de campos obrigatórios
- Validação de limites e entradas inválidas
- Persistência dos dados durante a navegação
- Upload e validação de arquivos
- Página do produto
- Fluxo de página do produto até o checkout
- Validação dos campos do checkout
- Consistência das informações entre página do produto e checkout
- Navegação e persistência dos dados no checkout

## Fora do escopo

- Testes de segurança invasivos
- Manipulação ou exploração de transações financeiras
- Acesso a dados de terceiros
- Testes de performance e carga
- APIs e integrações internas
- Fluxos que dependam de informações ou permissões não disponíveis publicamente
- Compra de produtos de terceiros para fins de teste

---

# Estratégia de Testes

Serão utilizados os seguintes tipos de teste:

- Testes Funcionais
- Testes Exploratórios
- Testes de Validação de Campos
- Testes de Limites
- Testes de Navegação e Persistência
- Testes de Usabilidade (UX)
- Testes de Consistência

Os cenários serão priorizados considerando o impacto na experiência do usuário e a relevância dos fluxos avaliados.

Comportamentos cuja regra de negócio não esteja disponível publicamente serão registrados como observação ou sugestão de melhoria, evitando classificá-los automaticamente como defeitos.

---

# Ambiente

| Item                | Valor                                  |
| ------------------- | -------------------------------------- |
| Sistema Operacional | Windows 11                             |
| Navegador           | Brave                                  |
| Ambiente            | Ambiente público disponível ao usuário |
| Plataforma          | Hotmart                                |

---

# Critérios de Entrada

- Acesso público às funcionalidades avaliadas.
- Conexão com internet disponível.
- Dados de teste disponíveis.
- Produto público disponível para avaliação do fluxo de checkout.

---

# Critérios de Saída

O estudo será considerado concluído quando:

- Todos os casos de teste planejados forem executados.
- Os achados (bugs e melhorias) estiverem documentados e classificados.
- As evidências (prints e vídeos) estiverem organizadas.
- Os principais fluxos definidos no escopo tiverem sido avaliados.

---

# Riscos

| Risco                                                  | Impacto | Prioridade |
| ------------------------------------------------------ | ------- | ---------- |
| Dados do produto apresentarem inconsistências          | Alto    | Alta       |
| Validações permitirem dados inválidos                  | Alto    | Alta       |
| Dados preenchidos serem perdidos durante a navegação   | Alto    | Alta       |
| Informações divergentes entre produto e checkout       | Alto    | Alta       |
| Comportamentos inconsistentes entre campos             | Médio   | Média      |
| Mensagens de erro pouco claras                         | Médio   | Média      |
| Formatos ou limites de upload serem tratados incorretamente | Médio | Média |

---

# Critérios de Priorização

Os testes serão executados seguindo a ordem:

1. Cadastro e configuração do produto
2. Validação de campos e regras de negócio
3. Upload e limites de arquivos
4. Persistência e navegação
5. Página do produto e consistência das informações
6. Validação dos campos do checkout
7. Navegação e persistência no checkout
8. Usabilidade e oportunidades de melhoria

---

# Entregáveis

- Plano de Testes
- Casos de Teste
- Registro de Bugs
- Registro de Sugestões de Melhoria
- Evidências dos testes
