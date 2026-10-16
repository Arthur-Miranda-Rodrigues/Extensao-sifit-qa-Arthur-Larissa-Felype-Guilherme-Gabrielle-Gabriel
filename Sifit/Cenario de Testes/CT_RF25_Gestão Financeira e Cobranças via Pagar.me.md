
---

# Cenário 25: Gestão Financeira e Cobranças via Pagar.me no SIFIT

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 25: Gestão Financeira e Cobranças via Pagar.me** no sistema **SiFit**. O objetivo é validar as funcionalidades de solicitação de saque, consulta de valores em processamento, recebíveis futuros, visualização de relatórios completos de assinaturas, filtros dinâmicos no gráfico de recebimentos, criação de novas cobranças avulsas, acesso às configurações de integração, consulta ao extrato de transações, visualização de repasses e análise de chargebacks.

---

## 2. Cenários de Teste

### Caso de Teste 01: Consulta de Valores em Processamento

| ID | Descrição |
| --- | --- |
| **C25-CT01** | Validar a abertura do modal de consulta de valores **Em processamento** e visualização de prazos de liberação no Pagar.me. |

| **Pré-condições** |
| --- |
| Usuário autenticado na dashboard do módulo **Pagar.me** do sistema SiFit.|

| **Passos** |
| --- |
| **DADO** que o usuário visualiza o painel principal do Pagar.me<br> |
| **QUANDO** clicar no botão **"Ver provisões"** do card *Em processamento*<br> |
| **ENTÃO** o sistema deve exibir a modal informativa com o total em processamento e as regras de prazos de compensação por meio de pagamento (crédito, PIX, boleto). |

| **Critérios de Aceitação** |
| --- |
| * A modal de provisões deve apresentar os detalhes e orientações de liberação sem falhas na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1lu_gmDxyF_G6EVQcHAUXi1Y6jCt9Ua1U/view?usp=sharing |

---

### Caso de Teste 02: Consulta de Recebíveis Futuros

| ID | Descrição |
| --- | --- |
| **C25-CT02** | Validar a consulta de **Recebíveis Futuros** e a listagem ou mensagem de retorno na modal correspondente. |

| **Pré-condições** |
| --- |
| Usuário posicionado na dashboard do módulo **Pagar.me**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela inicial de finanças do Pagar.me<br>|
| **QUANDO** clicar no botão **"Ver recebíveis"** no card *Recebíveis futuros*<br> |
| **ENTÃO** o sistema deve abrir a modal de recebíveis futuros e exibir os registros correspondentes ou a mensagem padrão de ausência de dados no período ("Nenhum recebível futuro encontrado").|

| **Critérios de Aceitação** |
| --- |
| * A interface deve responder adequadamente ao clique e exibir o modal informando a situação dos recebíveis. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Wn4H6hjrSmfT2hfFKJMe_j61Jtvb9Cwv/view?usp=sharing |

---

### Caso de Teste 03: Solicitação de Saque de Saldo Disponível

| ID | Descrição |
| --- | --- |
| **C25-CT03** | Validar o fluxo de preenchimento e solicitação de saque de valores disponíveis na conta Pagar.me.  |

| **Pré-condições** |
| --- |
| Usuário na página de gestão **Pagar.me** do sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"Solicitar saque"**<br><br> |
| **QUANDO** preencher o campo **"Valor do saque (R$)"** com a quantia desejada (ex.: 200,00) |
| **E** clicar no botão **"Confirmar Saque"**<br><br> |
| **ENTÃO** o pedido de transferência do saldo disponível para a conta bancária cadastrada deve ser submetido com sucesso. |

| **Critérios de Aceitação** |
| --- |
| * O campo de valor monetário deve aceitar o formato adequado e permitir a conclusão da solicitação ao confirmar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Zx-x4Bc5TU_cR1qY2q7oPJqn4G8CNrzH/view?usp=sharing |

---

### Caso de Teste 04: Visualização do Relatório Completo de Assinaturas Ativas

| ID | Descrição |
| --- | --- |
| **C25-CT04** | Validar a abertura e exibição do **Relatório — Assinaturas Ativas** a partir do painel financeiro. |

| **Pré-condições** |
| --- |
| Usuário logado no módulo **Pagar.me** do SiFit. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a seção de métricas financeiras<br> |
| **QUANDO** clicar no botão **"Ver relatório completo"** no card de assinaturas |
| **ENTÃO** o modal de relatório de assinaturas ativas e inativas no período deve ser aberto corretamente na tela. |

| **Critérios de Aceitação** |
| --- |
| * O modal de relatório deve carregar as informações e estruturas de listagem de assinaturas vinculadas ao gateway. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1hnnPYremFk-SwMFqT5IGcoCY0g0txEYw/view?usp=sharing |

---

### Caso de Teste 05: Filtragem Dinâmica do Gráfico de Recebimentos por Período

| ID | Descrição |
| --- | --- |
| **C25-CT05** | Validar a alteração do período de visualização no gráfico de **Recebimentos** (alternando entre 7, 30 e 90 dias). |

| **Pré-condições** |
| --- |
| Usuário na dashboard do **Pagar.me** visualizando o gráfico de recebimentos. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no seletor de período do gráfico de recebimentos<br> |
| **QUANDO** selecionar diferentes opções de intervalo temporal (ex.: "Últimos 7 dias", "Últimos 30 dias", "Últimos 90 dias") |
| **ENTÃO** o gráfico de linhas e os indicadores financeiros correspondentes devem se atualizar dinamicamente de acordo com o período escolhido.|

| **Critérios de Aceitação** |
| --- |
| * A curva do gráfico e os dados consolidados devem refletir corretamente o filtro de tempo selecionado pelo usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1WKkYk4mjv23vXEq6WbPDis4rnCDhPEgv/view?usp=sharing |

---

### Caso de Teste 06: Consulta ao Extrato de Transações Recentes

| ID | Descrição |
| --- | --- |
| **C25-CT06** | Validar a consulta detalhada do **Extrato de Transações** através do atalho na listagem de transações recentes. |

| **Pré-condições** |
| --- |
| Usuário na página do módulo **Pagar.me**. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a seção de transações recentes<br> |
| **QUANDO** clicar no link/botão **"Ver todas as transações"** (ou na opção de extrato) |
| **ENTÃO** o modal de **Extrato de Transações** deve ser apresentado na tela listando os lançamentos ou informando o status do período. |

| **Critérios de Aceitação** |
| --- |
| * O extrato deve ser aberto sem falhas, exibindo o histórico de movimentações financeiras do gateway. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1GG6ugyFF6EIdLmxF4pF0e8Ph13KxxXOl/view?usp=sharing |

---

### Caso de Teste 07: Criação de Nova Cobrança Avulsa via Cartão de Crédito ou PIX

| ID | Descrição |
| --- | --- |
| **C25-CT07** | Validar o registro e geração de uma nova cobrança avulsa preenchendo descrição, valor e selecionando o método de pagamento. |

| **Pré-condições** |
| --- |
| A integração com o Pagar.me estar configurada e ativa no SiFit. |

| **Passos** |
| --- |
| **DADO** que o usuário aciona a opção **"Nova cobrança"** nos atalhos rápidos<br> |
| **QUANDO** preencher a descrição (ex.: "Mensalidade 2") e o valor (ex.: R$ 100,00) |
| **E** selecionar o método de pagamento (ex.: "Cartão de crédito") |
| **E** clicar no botão **"Criar Cobrança"**<br><br> |
| **ENTÃO** o sistema deve processar a solicitação e exibir o aviso de sucesso ("Sucesso! Cobrança criada com sucesso!") com o botão "Entendi". |

| **Critérios de Aceitação** |
| --- |
| * A nova cobrança deve ser gerada com sucesso e a confirmação visual deve ser apresentada ao operador.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11lSsrCw-dpuCS9ZJb_vWv_JudsurFfjA/view?usp=sharing |

---

### Caso de Teste 08: Acesso às Configurações de Integração com o Pagar.me

| ID | Descrição |
| --- | --- |
| **C25-CT08** | Validar o redirecionamento e a navegação para o painel de **Configurações** gerais de integração do sistema. |

| **Pré-condições** |
| --- |
| Usuário na página do módulo **Pagar.me** com permissões administrativas. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a seção de acessos rápidos do Pagar.me<br> |
| **QUANDO** clicar na opção **"Configurações"** (ou aba de Integrações) |
| **ENTÃO** o sistema deve redirecionar o usuário para a tela de **Configurações** do SiFit na aba de pagamentos/integrações correspondente. |

| **Critérios de Aceitação** |
| --- |
| * A página de configurações deve ser carregada corretamente permitindo visualizar os parâmetros de integração. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1SA0jaR3Obe1QgCLLqdrReE2bB7DRP1AZ/view?usp=sharing |

---

### Caso de Teste 09: Consulta ao Histórico de Transações e Extrato Completo

| ID | Descrição |
| --- | --- |
| **C25-CT09** | Validar a verificação de registros no extrato de transações utilizando o botão de listagem completa na tabela de repasses/transações. |

| **Pré-condições** |
| --- |
| Usuário visualizando os cards de repasses, assinaturas e transações recentes no Pagar.me. |

| **Passos** |
| --- |
| **DADO** que o usuário está na dashboard financeira do Pagar.me<br> |
| **QUANDO** clicar em **"Ver todas"** nas opções de repasses ou transações recentes |
| **ENTÃO** o sistema deve abrir o extrato detalhado correspondente para conferência dos valores. |

| **Critérios de Aceitação** |
| --- |
| * A listagem detalhada deve ser aberta na tela sem erros de carregamento. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1-9sP6NJVKWCmX7oJDpqCogIDoK-74Ea6/view?usp=sharing |

---

### Caso de Teste 10: Verificação de Repasses e Chargebacks

| ID | Descrição |
| --- | --- |
| **C25-CT10** | Validar a visualização dos indicadores de **Repasses**, **Assinaturas** e **Chargebacks** na visão geral do Pagar.me. |

| **Pré-condições** |
| --- |
| Usuário logado na dashboard financeira do módulo Pagar.me. |

| **Passos** |
| --- |
| **DADO** que o usuário rola a página principal do Pagar.me até a seção de repasses e chargebacks<br> |
| **ENTÃO** os dados consolidados das métricas devem ser exibidos de forma clara e interativa na interface. |

| **Critérios de Aceitação** |
| --- |
| * Todos os contadores e atalhos de repasses e contestações devem estar visíveis e funcionais para consulta rápida. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ZOVP961LqBrMKMTQl7lLZly6nURwID6U/view?usp=sharing |
