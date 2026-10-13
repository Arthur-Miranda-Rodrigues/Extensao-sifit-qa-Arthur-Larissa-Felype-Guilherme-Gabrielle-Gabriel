

## Cenário de teste: Gestão Financeira e Cobranças via Pagar.me no SIFIT

### Caso de Teste 01: Solicitar saque de saldo disponível

| ID | Descrição |
| --- | --- |
| C07-CT01 | O sistema deve validar e permitir a solicitação de saque do saldo disponível na conta Pagar.me. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela do módulo **Pagar.me** (Financeiro). |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu "Pagar.me" |
| **E** clica no botão "Solicitar saque" |
| **QUANDO** preenche o campo "Valor do Saque (R$)" com um valor numérico (ex.: 200,00) |
| **E** clica no botão "Confirmar Saque" |
| **ENTÃO** a solicitação de saque deve ser enviada para processamento |

| **Critérios de aceitação** |
| --- |
| O campo de valor deve aceitar a formatação de moeda em reais e habilitar a confirmação de transferência para a conta bancária vinculada. |

---

### Caso de Teste 02: Criar nova cobrança avulsa via cartão de crédito ou PIX

| ID | Descrição |
| --- | --- |
| C07-CT02 | O sistema deve permitir a geração de uma nova cobrança definindo descrição, valor e método de pagamento. |

| **Pré-condições** |
| --- |
| A integração com o gateway de pagamento (Pagar.me) deve estar ativa no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o atalho "Nova cobrança" na tela principal do Pagar.me |
| **E** preenche o campo "Descrição" (ex.: "Mensalidade x") |
| **E** insere o "Valor (R$)" (ex.: 200,00) |
| **E** seleciona o "Método" de pagamento (ex.: "Cartão de crédito") |
| **QUANDO** clica no botão "Criar Cobrança" |
| **ENTÃO** o sistema exibe a mensagem de sucesso "Cobrança criada com sucesso!" com o botão "Entendi" |

| **Critérios de aceitação** |
| --- |
| A modal de confirmação "Sucesso!" deve ser apresentada confirmando a criação do link/cobrança. |

---

### Caso de Teste 03: Filtrar gráfico de recebimentos por período

| ID | Descrição |
| --- | --- |
| C07-CT03 | O sistema deve atualizar o gráfico de recebimentos conforme a janela temporal selecionada. |

| **Pré-condições** |
| --- |
| Existir histórico de transações registradas no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na dashboard do módulo "Pagar.me" |
| **QUANDO** altera o seletor de período do gráfico "Recebimentos" de "Últimos 30 dias" para "Últimos 7 dias" (ou "Últimos 90 dias") |
| **ENTÃO** o gráfico de linhas e os valores totais exibidos devem se reajustar ao período escolhido |

| **Critérios de aceitação** |
| --- |
| As opções de filtro disponíveis ("Últimos 7 dias", "Últimos 30 dias", "Últimos 60 dias", "Últimos 90 dias") devem alterar dinamicamente a curva do gráfico de recebimentos. |

https://jam.dev/c/24e36cb0-b257-48ba-ab07-77578f65ef26
