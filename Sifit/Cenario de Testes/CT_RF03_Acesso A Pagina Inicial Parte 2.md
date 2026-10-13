
---

# Cenário 3: Página Inicial (Parte 2)

### Caso de Teste 01: Visualização do Detalhamento Financeiro (Mensalidades Pendentes / Em Aberto)

| ID | Descrição |
| --- | --- |
| **C03-CT01** | Verificar se o modal/painel de "Mensalidades pendentes / Financeiro em Aberto" abre corretamente ao clicar em "Ver detalhes" e se os filtros por período de vencimento funcionam adequadamente.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado no sistema SIFIT e na Página Inicial.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial

 |
| **E** visualiza o card/seção de "Mensalidades pendentes"

 |
| **QUANDO** clicar no link "Ver detalhes"

 |
| **E** alternar entre as abas de filtro do modal (ex.: *Todos*, *Vence hoje*, *Até 7 dias*, *8 a 15 dias*, *16 a 30 dias*, *> 30 dias*)

 |
| **ENTÃO** o sistema deve carregar e filtrar as mensalidades em aberto de acordo com a aba selecionada sem apresentar erros.

 |

| **Critérios de aceitação** |
| --- |
| O modal de "Financeiro em Aberto" deve abrir com as métricas consolidadas e atualizar a listagem de registros ao alternar entre os filtros de período.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wiOUZ76pRiST_obtsVMrF0Jdc8-PK7p9/view?usp=sharing |

---

### Caso de Teste 02: Consulta de Desistências no Período e Pesquisa de Alunos

| ID | Descrição |
| --- | --- |
| **C03-CT02** | Validar a exibição do modal de "Desistências no Período" ao clicar no card correspondente e testar a busca por nome ou código.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está no Dashboard principal

 |
| **QUANDO** clicar sobre o card de métrica "Desistências no Período"

 |
| **E** utilizar o campo de pesquisa "Buscar por nome ou código..." digitando um termo de busca

 |
| **ENTÃO** o modal deve exibir a contagem total e filtrar os registros do período conforme o termo inserido no campo de busca.

 |

| **Critérios de aceitação** |
| --- |
| O modal "Desistências no Período" deve abrir corretamente e o campo de busca deve filtrar em tempo real a tabela de desistências.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1dQK6_uOb5jDR4ysA8sum-bfzlHiZd2gz/view?usp=sharing |

---

### Caso de Teste 03: Consulta e Filtragem de Matrículas no Período

| ID | Descrição |
| --- | --- |
| **C03-CT03** | Validar a abertura e o funcionamento da pesquisa no modal "Matrículas no Período" a partir do card do Dashboard.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial

 |
| **QUANDO** clicar no card de indicador "Matrículas no Período"

 |
| **E** digitar o nome ou código de um aluno no campo de busca do modal

 |
| **ENTÃO** o sistema deve atualizar a listagem de matrículas de acordo com o filtro aplicado.

 |

| **Critérios de aceitação** |
| --- |
| A listagem de matrículas do período deve ser exibida no modal e responder corretamente ao filtro digitado.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1PDujs2EBZTBo_S1REIBVpLMEAJJQBpqJ/view?usp=sharing |

---

### Caso de Teste 04: Visualização e Filtro da Listagem de Personais

| ID | Descrição |
| --- | --- |
| **C03-CT04** | Verificar se a modalidade/card de "Personais" abre a lista de profissionais cadastrados e permite a busca individualizada.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está no Dashboard

 |
| **QUANDO** clicar no card de indicador "Personais"

 |
| **E** utilizar o campo de pesquisa para buscar um profissional pelo nome

 |
| **ENTÃO** o modal "Personais" deve exibir a lista de personal trainers cadastrados (com informações de dias sem visita e última visita) e filtrar os resultados com precisão.

 |

| **Critérios de aceitação** |
| --- |
| O modal de Personais deve apresentar o total de profissionais cadastrados/ativos e permitir a busca por texto.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1-Qy_GsKdOtQ08zvxEGySzJaqNPfXkhTb/view?usp=sharing |

---

---

### Caso de Teste 05: Detalhes da Agenda de Hoje, Filtros e Ações Rápidas em Aulas

| ID | Descrição |
| --- | --- |
| **C03-CT05** | Validar a expansão do modal "Agenda de hoje" ao clicar em "Ver agenda", a busca por aulas, a seleção de unidades e a alteração dinâmica de detalhes ao selecionar aulas como *Turma dos Bodybuilders*, *Teste* e *Horario da manhã*, disponibilizando os botões de ações rápidas.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado no sistema SIFIT, posicionado na Página Inicial visualizando o painel "Agenda de hoje".

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial

 |
| **E** clica no link "Ver agenda" no canto superior do painel "Agenda de hoje"

 |
| **QUANDO** o modal "Agenda de hoje" for aberto

 |
| **E** o utilizador utilizar o campo "Buscar aula..." digitando um termo de pesquisa (ex.: "S") e em seguida limpando o campo

 |
| **E** navegar pelas opções na coluna "AULAS DO DIA", selecionando sucessivamente as turmas *Turma dos Bodybuilders*, *Teste* e *Horario da manhã*<br> |
| **E** interagir com o filtro de unidade ("Todas as unidades" / "Unidade não informada")

 |
| **ENTÃO** o modal deve filtrar/atualizar a lista de aulas em tempo real e o painel de "Detalhes da aula" deve atualizar as informações de horário, duração, professor, lista de alunos agendados e exibir as ações rápidas (*Lista de alunos*, *Fazer check-in*, *Enviar lembrete*, *Cancelar aula*).

 |

| **Critérios de aceitação** |
| --- |
| A consulta e busca de aulas no modal devem responder corretamente, atualizando dinamicamente os detalhes e ações rápidas da aula selecionada na coluna lateral.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18-fZsccI5UdnPHCNRzEgoWxFiRhV6Vtm/view?usp=sharing |
