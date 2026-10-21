---

## Cenário 14: Registro e Gestão de Contas a Receber

---
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

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Q5qUKG9AYxhUzBbABLlQCp1XVjo2i30C/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Nova Conta a Receber com Dados do Recebimento

| ID | Descrição |
| --- | --- |
| **C14-CT02** | Validar o cadastro de uma conta a receber pelo botão **Nova Conta**, incluindo a busca de cliente, a parametrização de cópias, o preenchimento dos dados do recebimento e a validação de campos obrigatórios. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Contas a Receber** do SIFIT; cliente cadastrado (ex.: 408 – Lila) e locais de recebimento disponíveis (Caixa Academia, Caixa Muay Thai, Teste, Teste2). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Contas a Receber**<br> |
| **QUANDO** clicar no botão **Nova Conta**<br> |
| **ENTÃO** a modal **Cadastrar Conta a Receber** deve abrir exibindo o cadastrante (ex.: 11 – Jair), a data atual (13/10/2026), o *Status* e o *Resíduo*<br> |
| **E QUANDO** clicar em **Pesquisar** na seção do cliente.|
| **ENTÃO** deve abrir a modal **Buscar Cliente** contendo o campo de pesquisa por nome, o botão **Buscar** e a listagem de Código/Nome. |
| **E QUANDO** pesquisar e selecionar o cliente desejado (ex.: 408 – Lila). |
| **E QUANDO** preencher o **Título** (ex.: "Matrícula").|
| **E** alterar o campo **Criar Cópias** de "Não" para "Sim". |
| **E** informar o **Valor a Receber** (ex.: "190,00"), a **Moeda** (BRL) e a **Data Venc.** (ex.: 13/10/2026). |
| **E** preencher os **Dados do Recebimento**: Valor Recebido (190,00), Data Recebimento (13/10/2026), Local de Recebimento (ex.: "Caixa Academia") e Observação (ex.: "Lila"), deixando temporariamente o **Tipo de Pagamento** em branco.  |
| **E** clicar em **Salvar**<br> |
| **ENTÃO** o sistema deve exibir o modal de alerta *"Atenção: Selecione o tipo de pagamento!"*<br> |
| **E QUANDO** fechar o alerta, selecionar o **Tipo de Pagamento** (ex.: "Dinheiro") e clicar novamente em **Salvar**<br> |
| **ENTÃO** a conta deve ser salva com sucesso e o usuário deve retornar à listagem principal, onde o novo registro é exibido. |

| **Critérios de Aceitação** |
| --- |
| * A modal de cadastro deve permitir localizar o cliente, preencher os dados financeiros e de recebimento e aplicar validações de campos obrigatórios (como o tipo de pagamento). |
| * O sistema deve concluir o cadastro com sucesso após o preenchimento correto e atualizar a listagem de contas a receber.|

| **Evidência** |
| --- |
|https://drive.google.com/file/d/1cvt_dqQlr9uv4gmZ93S-orkJr2gVM55m/view?usp=sharing |

---

### Caso de Teste 03: Validação de Campos Obrigatórios e Alertas de Preenchimento (Contas a Receber)

| ID | Descrição |
| --- | --- |
| **C14-CT03** | Validar as restrições e mensagens de alerta emitidas pelo sistema ao tentar salvar uma nova conta a receber com campos obrigatórios em branco (cliente, valor a receber, tipo de pagamento, local de recebimento e caixa fechado). |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Contas a Receber** e com a modal **Cadastrar Conta a Receber** aberta. |

| **Passos** |
| --- |
| **DADO** que o usuário está na modal de cadastro de conta a receber. |
| **QUANDO** clicar no botão **Salvar** sem selecionar nenhum cliente. |
| **ENTÃO** o sistema exibe o alerta: *"Atenção: Selecione o cliente!"*<br> |
| **E QUANDO** o usuário selecionar a cliente (ex.: 148 – Rharissily Gabrielle Oliveira), preencher o título mas deixar o **Valor a Receber** em branco e clicar em **Salvar**<br> |
| **ENTÃO** o sistema exibe o alerta: *"Atenção: Informe o valor a receber!"*<br> |
| **E QUANDO** preencher o valor (ex.: R$ 190,00) mas omitir o **Tipo de Pagamento** e clicar em **Salvar**<br> |
| **ENTÃO** o sistema exibe o alerta: *"Atenção: Selecione o tipo de pagamento!"*<br> |
| **E QUANDO** selecionar o tipo de pagamento (ex.: "Dinheiro") mas omitir o **Local de Recebimento** e clicar em **Salvar**<br> |
| **ENTÃO** o sistema exibe o alerta: *"Atenção: Selecione o local de recebimento!"*<br> |
| **E QUANDO** selecionar um local (ex.: "Teste") onde não há caixa aberto e clicar em **Salvar**<br> |
| **ENTÃO** o sistema exibe o aviso de caixa fechado: *"Atenção – Nenhum caixa aberto neste local. Abra um caixa e tente novamente."*, permitindo prosseguir via botão **Continuar**. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve barrar a gravação de registros incompletos, exibindo modais de aviso específicos para cada campo obrigatório omitido (cliente, valor, tipo de pagamento e local). |
| * O sistema deve tratar corretamente a restrição de caixa fechado, informando o operador antes de concluir a operação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1M2RgLTwrmKiqQNbw1egmD0JZ8SawMiER/view?usp=sharing |
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


| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nHSFb-xKV7RuW-AEwSvUukgTNWQIH728/view?usp=sharing |


