## Cenário 33: Gerenciamento de Pontuações no SIFIT

### Caso de Teste 01: Buscar pontuações por Código, Nome ou Status

| ID | Descrição |
| --- | --- |
| **C33-CT01** | O sistema deve permitir filtrar as pontuações cadastradas por código, nome da pontuação e status (Ativo/Inativo). |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela "Pontuação", com as pontuações "Desafio de Outubro" (código 1) e "Teste Dezembro" (código 2) cadastradas e ativas. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Pontuação" |
| **QUANDO** preencher o campo "Nome da pontuação" com "Desafio de Outubro" e clicar em "Buscar" |
| **ENTÃO** o sistema deve exibir apenas o registro correspondente (1 registro) |
| **E** ao limpar o nome, preencher o campo "Código" com "2" e clicar em "Buscar" |
| **ENTÃO** o sistema deve exibir apenas a pontuação "Teste Dezembro" (1 registro) |
| **E** ao limpar os filtros e selecionar o Status "Ativo" e clicar em "Buscar" |
| **ENTÃO** o sistema deve exibir as 2 pontuações ativas |
| **E** ao alterar o Status para "Inativo" e clicar em "Buscar" |
| **ENTÃO** o sistema deve exibir a mensagem "Nenhuma pontuação encontrada". |

| **Critérios de Aceitação** |
| --- |
| A listagem deve responder corretamente a cada combinação de filtro aplicada. |
| O rodapé da tabela deve refletir a quantidade de registros exibidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1h72VYND6GtgKN6SsflaxDkAFUCClSlJo/view?usp=sharing |

---

### Caso de Teste 02: Cadastrar nova pontuação com período e produtos de resgate

| ID | Descrição |
| --- | --- |
| **C33-CT02** | O sistema deve permitir a criação de uma nova pontuação (campanha) com período, tipo, status e produtos de resgate. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Pontuação" e existirem produtos cadastrados (ex.: "Notebook" e "Notebook Gamer"). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Pontuação" |
| **E** preenche o campo "Nome" com "Desafio de Halloween" |
| **E** seleciona a "Data Inicial" (17/10/2026) e a "Data Final" (31/10/2026) pelo calendário |
| **E** define o "Tipo" como "Período" e o "Status" como "Ativo" |
| **E** seleciona os produtos "Notebook Gamer" e "Notebook" em "Produtos de resgate", clicando em "Adicionar" a cada seleção |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** a nova pontuação deve ser cadastrada com sucesso |
| **E** exibida na tabela principal. |

| **Critérios de Aceitação** |
| --- |
| O registro criado deve aparecer na lista com o tipo, o período e o status configurados. |
| Os indicadores do topo da tela devem ser atualizados (ex.: "Total" de 2 para 3, "Ativas" de 2 para 3 e "Por período" de 1 para 2). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1XpsSsidfNsf1uwcyAaQRcg4sYgwHSxM6/view?usp=sharing |

---

### Caso de Teste 03: Tratar erro ao salvar a edição de uma pontuação

| ID | Descrição |
| --- | --- |
| **C33-CT03** | O sistema deve apresentar uma mensagem de erro ao falhar ao salvar as alterações de uma pontuação existente, sem quebrar a interface. |

| **Pré-condições** |
| --- |
| Existir a pontuação "Desafio de Outubro" (código 1, tipo "Mensal", status "Ativo") cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de visualizar/editar (lupa) da pontuação "Desafio de Outubro" |
| **E** altera o "Status" para "Inativo" no modal "Pontuação" |
| **E** seleciona um produto em "Produtos de resgate" |
| **QUANDO** clicar no botão "Salvar" e ocorrer uma falha ao gravar |
| **ENTÃO** o sistema deve exibir o modal de erro com a mensagem "Erro ao salvar pontuação" |
| **E** ao clicar em "Fechar", o usuário deve retornar à listagem com os dados originais mantidos. |

| **Critérios de Aceitação** |
| --- |
| O modal de erro deve informar a falha sem quebrar a interface da aplicação. |
| A pontuação não deve ser alterada na listagem após o erro (permanece com status "Ativo"). |

| **Observação (comportamento verificado na gravação)** |
| --- |
| A alteração de status para "Inativo" não foi concluída: o sistema exibiu o modal **"Erro – Erro ao salvar pontuação"** e a pontuação continuou "Ativa" na listagem. Verificar se a falha se deve a um defeito na edição de uma alteração válida. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/17rlYxRcvmZSKIoensH0pldTBkU3NX06o/view?usp=sharing |

---

### Caso de Teste 04: Associar atividades a uma pontuação

| ID | Descrição |
| --- | --- |
| **C33-CT04** | O sistema deve permitir vincular atividades a uma pontuação por meio do modal "Atividades da Pontuação". |

| **Pré-condições** |
| --- |
| Deve haver uma pontuação cadastrada na listagem e atividades cadastradas no menu "Atividades". |

| **Passos** |
| --- |
| **DADO** que o usuário abre o modal "Atividades da Pontuação" pela coluna "Ações" de uma pontuação |
| **E** seleciona a atividade "Correr no quarteirão" no campo "Atividade" e clica em "Adicionar" |
| **E** seleciona a atividade "Treino de perna" e clica em "Adicionar" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** as atividades devem ser gravadas e vinculadas à pontuação |
| **E** o modal deve ser fechado, retornando à listagem de pontuações. |

| **Critérios de Aceitação** |
| --- |
| As atividades adicionadas devem aparecer na lista do modal (com opção de remoção) antes de salvar. |
| As atividades selecionadas devem ficar vinculadas à pontuação após salvar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ZJQsQNJRwXjUlXjtbgjS6C97VKSCUyVi/view?usp=sharing |

---

### Caso de Teste 05: Visualizar o Ranking de Participantes

| ID | Descrição |
| --- | --- |
| **C33-CT05** | O sistema deve permitir visualizar o ranking de participantes associados a uma pontuação. |

| **Pré-condições** |
| --- |
| Existir uma pontuação cadastrada na listagem (ex.: "Desafio de Outubro"). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Pontuação" |
| **QUANDO** clicar no ícone "Ranking de Participantes" (ícone de pessoas) na coluna "Ações" da pontuação |
| **ENTÃO** o modal "Ranking de Participantes" deve ser aberto |
| **E** exibir as colunas de posição, nome e pontos dos participantes, ou a mensagem "Nenhum participante encontrado" caso não existam pontuações registradas |
| **E** ao clicar em "Fechar", o modal deve ser encerrado. |

| **Critérios de Aceitação** |
| --- |
| O modal de ranking deve ser carregado exibindo a lista de participantes ou o aviso de lista vazia. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1G45l4kbEHZ30sPfTT4WRmEt2Z_EhraBb/view?usp=sharing |

---

### Caso de Teste 06: Tratar erro do servidor ao acionar uma ação da pontuação

| ID | Descrição |
| --- | --- |
| **C33-CT06** | O sistema deve apresentar mensagem de erro ao falhar o processamento de uma ação da coluna "Ações", sem quebrar a interface. |

| **Pré-condições** |
| --- |
| Existir a pontuação "Desafio de Outubro" (código 1) cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Pontuação" |
| **QUANDO** clicar no quarto ícone (lista de verificação) da coluna "Ações" da pontuação "Desafio de Outubro" |
| **E** ocorrer uma falha no servidor |
| **ENTÃO** o sistema deve exibir o modal de erro com a mensagem "Erro no servidor – Erro interno inesperado" |
| **E** ao clicar em "Fechar", o usuário deve retornar à listagem sem alterações. |

| **Critérios de Aceitação** |
| --- |
| O modal de erro deve ser exibido informando a falha sem quebrar a interface da aplicação. |
| A listagem e os indicadores do topo devem permanecer inalterados após fechar o modal. |

| **Observação (comportamento verificado na gravação)** |
| --- |
| Ao acionar a ação, o sistema exibiu o modal **"Erro no servidor – Erro interno inesperado"**, e a ação não foi concluída. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Ne4ay4CW_VtSYdFDLJzXFM_QZNMIB3yc/view?usp=sharing |

---

### Caso de Teste 07: Excluir uma pontuação

| ID | Descrição |
| --- | --- |
| **C33-CT07** | O sistema deve permitir excluir uma pontuação existente após confirmação do usuário. |

| **Pré-condições** |
| --- |
| Deve existir ao menos uma pontuação cadastrada (ex.: "Desafio de Outubro", código 1). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (X) da pontuação "Desafio de Outubro" |
| **E** o modal de confirmação "Deseja deletar a Pontuação?" é exibido com as opções "Cancelar" e "Confirmar" |
| **QUANDO** clicar no botão "Confirmar" |
| **ENTÃO** a pontuação deve ser removida da listagem |
| **E** os indicadores do topo devem ser atualizados. |

| **Critérios de Aceitação** |
| --- |
| O registro excluído não deve mais constar na tabela de pontuações. |
| Os indicadores devem refletir a exclusão (ex.: "Total" de 3 para 2, "Ativas" de 3 para 2 e "Mensais" de 1 para 0). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11wYcBAlwqeVBF8mQJtAO4-2l98QuOfLk/view?usp=sharing |

### Caso de Teste 08: Validar o nome obrigatório ao cadastrar uma pontuação

| ID | Descrição |
| --- | --- |
| **C33-CT08** | O sistema deve impedir o cadastro de uma pontuação sem nome e exibir um aviso solicitando o preenchimento do campo. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Pontuação" e existirem produtos cadastrados (ex.: "Notebook Gamer"). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Pontuação" |
| **E** deixa o campo "Nome" em branco |
| **E** seleciona o produto "Notebook Gamer" em "Produtos de resgate" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o sistema deve exibir o modal "Aviso" com a mensagem "Informe o nome da pontuação" |
| **E** a pontuação não deve ser cadastrada |
| **E** ao clicar em "Entendi", o usuário deve retornar ao formulário com os dados mantidos para corrigir o preenchimento. |

| **Critérios de Aceitação** |
| --- |
| O cadastro só deve ser concluído com o campo "Nome" preenchido. |
| Os indicadores do topo da tela não devem ser alterados enquanto o cadastro não for concluído. |

| **Observação (comportamento verificado na gravação)** |
| --- |
| Após o aviso, ao preencher apenas o Nome ("sdfasdf"), com Tipo "Mensal" e Status "Ativo", sem informar Data Inicial e Data Final, o sistema **cadastrou** a pontuação, que foi listada com o período "0000-00-00 — 0000-00-00". Verificar se as datas deveriam ser obrigatórias. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ZherjpC1oDDIsjo2h2qQNwKXn08A0_39/view?usp=sharing |

