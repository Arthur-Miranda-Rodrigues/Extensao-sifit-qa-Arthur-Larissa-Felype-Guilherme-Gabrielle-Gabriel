
---

## Cenário de teste: Gerenciamento Financeiro e Configurações no SIFIT

### Caso de Teste 01: Criar uma nova cobrança via Pagar.me com dados válidos



| ID | Descrição |
| --- | --- |
| **FIN-CT01** | O sistema deve permitir a criação de uma nova cobrança no módulo Pagar.me.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e ter acesso ao menu Financeiro > Pagar.me.

 |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu "Pagar.me" em Financeiro

 |
| **E** clica na opção "Nova cobrança" nos Acessos rápidos

 |
| **E** preenche a Descrição (ex: "Mensalidade x") e o Valor (ex: "200,00")

 |
| **E** seleciona o Método de pagamento "Cartão de crédito"

 |
| **QUANDO** clicar no botão "Criar Cobrança"

 |
| **ENTÃO** o sistema deve exibir a mensagem de sucesso "Cobrança criada com sucesso!"

 |

| **Critérios de aceitação** |
| --- |
| O modal de confirmação "Sucesso!" deve ser exibido na tela após a criação da cobrança.

 |

---

### Caso de Teste 02: Solicitação de saque de saldo



| ID | Descrição |
| --- | --- |
| **FIN-CT02** | O sistema deve permitir a abertura do modal e inserção de valor para solicitação de saque.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na página principal do Pagar.me.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está no painel do "Pagar.me"

 |
| **E** clica no botão "Solicitar saque"

 |
| **E** digita o valor desejado no campo "VALOR DO SAQUE (R$)"

 |
| **QUANDO** clicar em "Confirmar Saque"

 |
| **ENTÃO** a solicitação deve ser processada pelo sistema.

 |

| **Critérios de aceitação** |
| --- |
| O modal de saque deve aceitar os valores digitados para a transferência.

 |

---

### Caso de Teste 03: Alterar e salvar configurações gerais do sistema



| ID | Descrição |
| --- | --- |
| **CFG-CT01** | O sistema deve permitir a alteração e salvamento dos parâmetros gerais na aba Home.

 |

| **Pré-condições** |
| --- |
| O usuário deve ter privilégios de acesso às Configurações do sistema.

 |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu "Configurações"

 |
| **E** na aba "Home", altera o campo "Academia marcada como Box?" para "Sim"

 |
| **E** altera o campo "Trabalha com turmas?" para "Sim"

 |
| **E** altera o parâmetro "Controle de Presença" para "Biometria"

 |
| **QUANDO** clicar no botão "Salvar Configurações"

 |
| **ENTÃO** as preferências devem ser atualizadas no sistema.

 |

| **Critérios de aceitação** |
| --- |
| Os novos parâmetros selecionados devem ser mantidos e aplicados à conta após salvar.

 |

 https://jam.dev/c/24e36cb0-b257-48ba-ab07-77578f65ef26
