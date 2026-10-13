---

# Cenário de Teste: Registro e Gestão de Contas a Receber

---

## 1. Descrição

Este documento especifica os casos de teste referentes ao ** Cenário e Teste - Registro e Gestão de Contas a Receber** do sistema **SiFit**. O objetivo é validar os filtros da listagem (código, cliente, tipo de data, período e status), o cadastro de uma nova conta com recebimento, a atualização dos cards financeiros, os atalhos rápidos de período, a visualização e edição de uma conta já recebida (ajuste administrativo) e a exclusão de lançamentos.

---

## 2. Casos de Teste

### Caso de Teste 01: Filtros de Pesquisa por Código, Cliente, Tipo de Data, Período e Status

| ID | Descrição |
| --- | --- |
| **C14-CT01** | Validar os filtros da listagem de Contas a Receber: Código, Nome do cliente, Tipo de Data (Vencimento/Recebimento), Data Inicial/Final e Status. |

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit e posicionado na tela **Contas a Receber**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de **Contas a Receber**, com os cards financeiros (*Entradas*, *Saídas*, *Líquido*, *Previsto para o Mês*, *Recebido no Mês*, *Pendentes no Mês* e *Contas Atrasadas*) |
| **QUANDO** informar o nome de um cliente (ex.: "arthur do santos") ou o código do cliente (ex.: "398") e clicar em **Buscar** |
| **ENTÃO** a tabela deve exibir somente os lançamentos do cliente informado ou permanecer vazia quando não houver lançamentos |
| **E QUANDO** alterar o **Tipo de Data** entre *Vencimento* e *Recebimento* |
| **E** ajustar a **Data Inicial** e a **Data Final** pelo calendário (ex.: Data Inicial 13/08/2026 e Data Final 31/10/2026) |
| **E** selecionar um valor no filtro **Status** (ex.: *Todos*, *Vencido*, *Recebido* ou *Cancelado*) e clicar em **Buscar** |
| **ENTÃO** a listagem e os cards devem ser atualizados de acordo com os critérios informados. |

| **Critérios de Aceitação** |
| --- |
| * Apenas registros correspondentes ao código/nome, período, tipo de data e status informados devem ser apresentados na grid. |
| * Se nenhum lançamento for localizado, a tabela deve ficar vazia. |
| * Os cards financeiros devem ser coerentes com os registros exibidos. |

| **Resultado obtido** |
| --- |
| Os campos e o calendário aceitaram os filtros e as buscas por nome e código retornaram a grid vazia. **Inconsistência:** ao ampliar o período (Data Inicial 13/08/2026), os cards passaram a exibir *Entradas* e *Líquido* de R$ 100,00, mas a tabela continuou vazia, inclusive com os status *Recebido* e *Cancelado*. |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (cards com valor sem lançamento correspondente na grid) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Q5qUKG9AYxhUzBbABLlQCp1XVjo2i30C/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Nova Conta a Receber com Dados do Recebimento

| ID | Descrição |
| --- | --- |
| **C14-CT02** | Validar o cadastro de uma conta a receber pelo botão **Nova Conta**, com busca de cliente, criação de cópias e preenchimento dos dados do recebimento. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Contas a Receber**; cliente cadastrado (ex.: 408 – Lila) e locais de recebimento disponíveis (Caixa Academia, Caixa Muay Thai, Teste, Teste2). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Contas a Receber** |
| **QUANDO** clicar em **Nova Conta** |
| **ENTÃO** a modal **Cadastrar Conta a Receber** deve abrir com o cadastrante (ex.: 11 – Jair), a data (13/10/2026), o *Status* e o *Resíduo* |
| **E QUANDO** clicar em **Pesquisar** na seção do cliente |
| **ENTÃO** deve abrir a modal **Buscar Cliente** com o campo "Nome do cliente", o botão **Buscar** e a lista de Código/Nome, permitindo selecionar o cliente (ex.: 408 – Lila) |
| **E QUANDO** informar o **Título** (ex.: "Matrícula") |
| **E** alterar **Criar Cópias** de "Não" para "Sim" |
| **E** informar o **Valor a Receber** (ex.: "200,00"), a **Moeda** (BRL) e a **Data Venc.** (ex.: 09/10/2026) |
| **E** preencher os **Dados do Recebimento**: Valor Recebido (200,00), Data Recebimento (13/10/2026), Tipo de Pagamento (ex.: "Cheque"), Local de Recebimento (ex.: "Caixa Academia") e Observação (ex.: "Lila") |
| **E** clicar em **Salvar** |
| **ENTÃO** o sistema deve exibir o aviso *"Atenção – Nenhum caixa aberto neste local. Abra um caixa e tente novamente."* com as opções **Cancelar** e **Continuar** |
| **E QUANDO** clicar em **Continuar** |
| **ENTÃO** a conta deve ser salva e o usuário deve retornar à listagem. |

| **Critérios de Aceitação** |
| --- |
| * A modal deve permitir localizar e selecionar o cliente, informar os dados da conta e do recebimento e salvar. |
| * O aviso de caixa não aberto deve ser exibido e, ao continuar, o cadastro deve ser concluído. |

| **Resultado obtido** |
| --- |
| A busca de cliente, o preenchimento dos campos e o aviso de caixa foram exibidos conforme o esperado; ao continuar, o cadastro foi concluído e o registro apareceu na listagem (CT03). |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/12cE6Q-cCyWn9kCH2nGjJuolwO1dmZQIF/view?usp=sharing |

---

### Caso de Teste 03: Conferência do Lançamento e dos Cards Financeiros Após o Cadastro

| ID | Descrição |
| --- | --- |
| **C14-CT03** | Verificar se a conta cadastrada aparece na listagem com status "RECEBIDO" e se os cards financeiros refletem o valor lançado. |

| **Pré-condições** |
| --- |
| Conta cadastrada no CT02 (cliente Lila, título "Matrícula", R$ 200,00). |

| **Passos** |
| --- |
| **DADO** que o usuário retornou à listagem de **Contas a Receber** com o período de 01/10/2026 a 31/10/2026 e status *Todos* |
| **QUANDO** consultar a grid e os cards financeiros |
| **ENTÃO** a tabela deve exibir o lançamento (código 1589, cliente Lila, título Matrícula, valor a receber R$ 200,00, valor recebido R$ 200,00, status **RECEBIDO**) com as ações de visualizar e excluir |
| **E** os cards *Entradas*, *Líquido*, *Previsto para o Mês* e *Recebido no Mês* devem apresentar R$ 200,00 (100,00% recebido). |

| **Critérios de Aceitação** |
| --- |
| * O lançamento deve ser listado com os valores e o status informados no cadastro. |
| * Os cards devem somar o valor da nova conta. |

| **Resultado obtido** |
| --- |
| Lançamento 1589 exibido com R$ 200,00 e status RECEBIDO; cards atualizados para R$ 200,00. Apenas **um** lançamento foi listado mesmo com "Criar Cópias" = "Sim". |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (confirmar o comportamento esperado de "Criar Cópias") |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1veOnehEG9kRDaH-yZH8ojd6Fiydy6a7C/view?usp=sharing |

---

### Caso de Teste 04: Atalhos Rápidos de Período (Ontem e Este mês)

| ID | Descrição |
| --- | --- |
| **C14-CT04** | Validar os botões de atalho de período (*Hoje*, *Ontem*, *Últimos 7 dias* e *Este mês*) na atualização das datas, da grid e dos cards. |

| **Pré-condições** |
| --- |
| Existir ao menos uma conta lançada no mês corrente (ex.: 1589 – Lila). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de **Contas a Receber** |
| **QUANDO** clicar no atalho **Ontem** |
| **ENTÃO** os campos **Data Inicial** e **Data Final** devem ser preenchidos com 12/10/2026, a grid deve ficar vazia e os cards *Entradas* e *Líquido* devem exibir R$ 0,00 |
| **E QUANDO** clicar no atalho **Este mês** |
| **ENTÃO** as datas devem ser ajustadas para 01/10/2026 a 31/10/2026, o lançamento 1589 deve ser listado e os cards *Entradas* e *Líquido* devem exibir R$ 200,00. |

| **Critérios de Aceitação** |
| --- |
| * O atalho selecionado deve ficar destacado e preencher automaticamente o período. |
| * A grid e os cards devem refletir o período escolhido. |

| **Resultado obtido** |
| --- |
| Os atalhos "Ontem" e "Este mês" preencheram as datas corretamente e atualizaram a grid e os cards *Entradas* e *Líquido*. |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1y0NIE8Sh4_cgP8MyDhPZ2v2SJO0V9sp2/view?usp=sharing |

---

### Caso de Teste 05: Visualização e Edição de Conta Já Recebida (Ajuste Administrativo)

| ID | Descrição |
| --- | --- |
| **RFC14-CT05** | Validar a visualização dos detalhes de uma conta recebida e a edição dos valores com o aviso de **Ajuste Administrativo**. |

| **Pré-condições** |
| --- |
| Existir conta com status **RECEBIDO** (ex.: 1589 – Lila, R$ 200,00). |

| **Passos** |
| --- |
| **DADO** que o usuário clicou no ícone de visualizar da conta recebida |
| **QUANDO** a modal **Visualizar Conta** for exibida |
| **ENTÃO** devem constar *Informações Gerais*, *Dados da Conta*, *Dados do Recebimento* e *Observação*, além do botão **Editar** |
| **E QUANDO** clicar em **Editar** |
| **ENTÃO** o sistema deve exibir o aviso *"Ajuste Administrativo – Você está editando uma conta já recebida. Esta ação será registrada como ajuste administrativo."* com **Cancelar** e **Continuar** |
| **E QUANDO** clicar em **Continuar** e alterar o **Valor a Receber** e o **Valor Recebido** de R$ 200,00 para R$ 190,00 |
| **E** clicar em **Salvar** |
| **ENTÃO** o botão deve exibir "Salvando...", a modal deve ser fechada e a listagem deve apresentar o lançamento com o novo valor e os cards *Entradas* e *Líquido* atualizados. |

| **Critérios de Aceitação** |
| --- |
| * A edição de conta recebida deve exigir a confirmação do ajuste administrativo. |
| * Os novos valores devem ser persistidos e refletidos na listagem e nos cards. |

| **Resultado obtido** |
| --- |
| Aviso de ajuste administrativo exibido e valores salvos: grid com R$ 190,00 e cards *Entradas*/*Líquido* em R$ 190,00. **Inconsistências:** os cards *Previsto para o Mês* e *Recebido no Mês* permaneceram em R$ 200,00; na visualização, o Tipo de Pagamento aparece como "Dinheiro" e o Vencimento como 13/10/2026, diferentes do informado no cadastro (Cheque e 09/10/2026), e o Local de Recebimento aparece como "entrada" na visualização e "Caixa Academia" na edição. |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (cards de previsto/recebido não recalculados e divergência de dados entre cadastro e visualização) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11hHSbnN18f9I9riwdkuww1Mwt237prY7/view?usp=sharing |

---

### Caso de Teste 06: Exclusão de Conta a Receber

| ID | Descrição |
| --- | --- |
| **C14-CT06** | Validar a remoção de um lançamento na listagem de Contas a Receber mediante confirmação. |

| **Pré-condições** |
| --- |
| Existir ao menos um registro cadastrado na listagem (ex.: 1589 – Lila, R$ 190,00). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de **Contas a Receber** |
| **QUANDO** clicar no ícone de **Lixeira** na coluna de ações do registro |
| **ENTÃO** o sistema deve exibir a modal *"Deseja deletar esta conta?"* com **Cancelar** e **Confirmar** |
| **E QUANDO** clicar em **Confirmar** |
| **ENTÃO** a conta deve ser excluída e removida da grade de exibição |
| **E** os valores dos cards financeiros devem ser recalculados. |

| **Critérios de Aceitação** |
| --- |
| * A exclusão só deve ocorrer após a confirmação. |
| * Após excluir, a conta não deve mais constar na grid e os cards devem ser recalculados. |

| **Resultado obtido** |
| --- |
| Modal de confirmação exibida e a conta removida da grid. **Falha:** os cards não foram recalculados após a exclusão (*Entradas* e *Líquido* em R$ 190,00; *Previsto* e *Recebido no Mês* em R$ 200,00), embora a grid esteja vazia. |

| **Status** |
| --- |
| FALHOU (cards financeiros não recalculados após a exclusão) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nHSFb-xKV7RuW-AEwSvUukgTNWQIH728/view?usp=sharing |


