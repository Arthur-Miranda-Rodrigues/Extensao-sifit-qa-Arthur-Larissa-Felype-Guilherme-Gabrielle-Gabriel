# Cenário 23 : Gestão de Box (Turmas e Modalidades)

### Caso de Teste 01: Cadastro de Nova Modalidade de Treino

| ID | Descrição |
| --- | --- |
| **C23-CT01** | Validar o cadastro de uma nova modalidade preenchendo o nome correspondente no painel de Modalidades. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit na página **Box - Turmas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na seção de **Modalidades**<br><br> |
| **QUANDO** preencher o campo **Nome da modalidade** com "Modalidade Maromba" |
| **E** clicar no botão de salvar/adicionar **+ Modalidade**<br><br>  |
| **ENTÃO** a modalidade deve ser cadastrada com sucesso |
| **E** ser exibida corretamente na listagem da tabela superior. |

| **Critérios de Aceitação** |
| --- |
| * A modalidade deve ser gravada na base de dados com o nome estipulado. |
| * A tabela de modalidades deve ser atualizada exibindo o novo registro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11hAqVHfYQxMMLIDmC0GskR63QWAigEl1/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Turma Recorrente com Horários e Vagas Definidos

| ID | Descrição |
| --- | --- |
| **C23-CT02** | Validar o cadastro de uma nova turma recorrente vinculada a uma modalidade com configuração de horário e vagas. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit na página **Box - Turmas** e modalidade existente cadastrada. |

| **Passos** |
| --- |
| **DADO** que o usuário está na seção de **Turmas recorrentes**<br><br> |
| **QUANDO** preencher o campo **Nome da turma** com "Turma Maromba 2" |
| **E** selecionar a **Modalidade** correspondente (ex: "Modalidade Maromba") |
| **E** definir o horário de início ("09:00") e término ("16:00") |
| **E** configurar a quantidade de **Vagas** para "16" |
| **E** clicar no botão de salvar/adicionar **+ Turma**<br><br> |
| **ENTÃO** a turma deve ser cadastrada com sucesso |
| **E** ser exibida corretamente na listagem da tabela inferior.|

| **Critérios de Aceitação** |
| --- |
| * A turma recorrente deve ser gravada na base de dados com o intervalo de horário e número de vagas estipulados. |
| * A tabela de turmas recorrentes deve ser atualizada exibindo o novo registro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Uw6czej6aLWaabbPSV5fov7Nbt24yPdf/view?usp=sharing |

---

### Caso de Teste 03: Edição de Modalidade (Alteração de Nome e Status)

| ID | Descrição |
| --- | --- |
| **C23-CT03** | Validar a edição do nome e do status de uma modalidade existente. |

| **Pré-condições** |
| --- |
| Existir uma modalidade cadastrada no painel de *Modalidades*. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição de uma modalidade existente |
| **QUANDO** alterar o nome da modalidade no campo correspondente (ex: ajustar para "Léo Valeska"). |
| **E** alterar o seletor de status (ex: alternar para "Ativo"). |
| **E** confirmar/salvar as alterações no botão **Modalidade**<br><br> |
| **ENTÃO** os dados da modalidade devem ser atualizados no sistema |
| **E** a tabela de modalidades deve refletir as modificações imediatamente. |

| **Critérios de Aceitação** |
| --- |
| * As alterações de nome e status da modalidade devem persistir corretamente no banco de dados.|
| * A listagem de modalidades deve recarregar atualizada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/17WI-vKXPTS43Ig9aDG4lOTUOnfmNO6Jt/view?usp=sharing |

---

Aqui está o Caso de Teste 04 ajustado com base nas ações realizadas no vídeo:

---

### Caso de Teste 04: Edição de Turma Recorrente

| ID | Descrição |
| --- | --- |
| **C23-CT04** | Validar a edição dos dados de uma turma recorrente existente (nome, modalidade vinculada, horários, vagas, dias da semana e status). |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit na página **Box - Turmas** e existência de uma turma recorrente cadastrada. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição (lápis) de uma turma recorrente existente |
| **QUANDO** alterar o **Nome da turma** para "Leonardo Valeska 2" |
| **E** selecionar a **Modalidade** correspondente (ex: "Leo valeska") |
| **E** manter/ajustar o horário de início ("09:30") e término ("12:30") |
| **E** marcar os dias da semana desejados (ex: Dom, Seg, Ter, Qua, Qui, Sex, Sab) |
| **E** definir a quantidade de **Vagas** (ex: "20") e o status (ex: "Inativo") |
| **E** clicar no botão **+ Turma** para salvar as alterações |
| **ENTÃO** as alterações da turma recorrente devem ser salvas com sucesso |
| **E** a tabela de turmas recorrentes deve exibir os dados atualizados. |

| **Critérios de Aceitação** |
| --- |
| * As informações editadas da turma recorrente devem persistir corretamente no banco de dados. |
| * A listagem na grade principal de turmas recorrentes deve ser atualizada imediatamente com os novos valores. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1LORLB3QegZ1je0MStozRoRM9Jzz_BKVB/view?usp=sharing |

---

### Caso de Teste 05: Exclusão de Modalidade de Treino

| ID | Descrição |
| --- | --- |
| **C23-CT05** | Validar a funcionalidade de exclusão de uma modalidade cadastrada na tabela de modalidades. |

| **Pré-condições** |
| --- |
| Existir pelo menos uma modalidade cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a modalidade desejada na tabela superior |
| **QUANDO** clicar no ícone de exclusão (botão de lixeira na coluna de Ações) correspondente |
| **ENTÃO** o registro da modalidade deve ser removido da base de dados do sistema |
| **E** a tabela de modalidades deve ser atualizada, deixando de exibir o item excluído. |

| **Critérios de Aceitação** |
| --- |
| * A modalidade selecionada deve ser excluída com sucesso ao acionar o botão de exclusão. |
| * O sistema não deve apresentar travamentos ou erros de integridade ao remover o registro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Lgg4hLQyXctUGZZhh8h3jG_JFZyPfzNf/view?usp=sharing |

---

#### Caso de Teste 06: Exclusão de Turma Recorrente

| ID | Descrição |
| --- | --- |
| **C23-CT06** | Testar a remoção de uma turma recorrente cadastrada na listagem de turmas do Box. |

| **Pré-condições** |
| --- |
| Existir uma turma recorrente cadastrada na tabela inferior do painel. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza as turmas recorrentes cadastradas. |
| **QUANDO** clicar no botão de exclusão (ícone de lixeira) na linha referente à turma alvo. |
| **ENTÃO** a turma recorrente deve ser permanentemente excluída do sistema. |
| **E** a listagem de turmas deve ser atualizada refletindo a remoção do registro. |

| **Critérios de Aceitação** |
| --- |
| * A turma recorrente deve ser apagada corretamente da tabela e da base de dados. |
| * A interface deve responder de forma fluida à ação de exclusão. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1hTepbhZ3kiV38R75GvsPAPJr0OrMy0YK/view?usp=sharing |
