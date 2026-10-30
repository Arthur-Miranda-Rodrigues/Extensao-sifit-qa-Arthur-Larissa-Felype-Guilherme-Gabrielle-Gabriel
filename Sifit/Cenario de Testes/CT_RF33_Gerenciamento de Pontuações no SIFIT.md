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
