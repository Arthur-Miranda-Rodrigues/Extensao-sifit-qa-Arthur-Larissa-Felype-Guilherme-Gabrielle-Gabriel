


Aqui está a documentação reestruturada e padronizada do **Módulo de Gestão de Box (Turmas e Modalidades - RF17 - SIFIT)**, formatada no padrão em tabelas com cenários BDD/Gherkin e critérios de aceitação:

---

# Cenário de teste: Gestão de Box (Turmas e Modalidades)

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 17 (RF17) - Gestão de Box** do módulo **Treinamento > Box - Turmas** do sistema **SiFit**. O objetivo é validar o cadastramento de modalidades de treino, a criação e edição de turmas recorrentes (horários, vagas e dias da semana), o gerenciamento de status de modalidades e a exclusão de turmas.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Box (Turmas e Modalidades)

#### Caso de Teste 01: Cadastramento de Nova Modalidade

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar o cadastro de uma nova modalidade de treino no Box. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado no menu **Box - Turmas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Box - Turmas** |
| **QUANDO** preencher o campo **Nome da modalidade** com "Leo" no painel de *Modalidades* |
| **E** preencher o campo **Descrição** com "Leo" |
| **E** clicar no botão **+ Modalidade** |
| **ENTÃO** a nova modalidade deve ser cadastrada com sucesso |
| **E** ser exibida na tabela de modalidades com o status "Ativo". |

| **Critérios de Aceitação** |
| --- |
| * A modalidade cadastrada deve ser gravada na base de dados e vinculada à listagem de modalidades do Box. |
| * O status padrão da nova modalidade deve ser exibido como "Ativo". |

---

#### Caso de Teste 02: Cadastramento de Nova Turma Recorrente

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Verificar o cadastro de uma turma recorrente vinculada a uma modalidade existente. |

| **Pré-condições** |
| --- |
| Existir a modalidade "Leo" cadastrada no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Box - Turmas** |
| **QUANDO** preencher o **Nome da turma** com "Leo" no painel *Turmas recorrentes* |
| **E** selecionar a **Modalidade** "Leo" |
| **E** marcar os dias da semana desejados (ex: Seg, Qua, Qui, Sex) |
| **E** definir a quantidade de **Vagas** como "20" |
| **E** configurar o horário (Início: "20:09" / Fim: "20:30") |
| **E** clicar no botão **+ Turma** |
| **ENTÃO** a turma recorrente deve ser criada com sucesso |
| **E** ser exibida na tabela inferior com as informações de horário, dias da semana e quantidade de vagas ativas. |

| **Critérios de Aceitação** |
| --- |
| * A turma recorrente deve ser inserida na base de dados com todos os dias, horários e vagas configurados. |
| * A listagem principal deve atualizar exibindo o novo registro de turma. |

---

#### Caso de Teste 03: Edição de Modalidade (Status e Nome)

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Testar a alteração do nome/descrição e do status de uma modalidade existente. |

| **Pré-condições** |
| --- |
| Existir a modalidade "Leo" cadastrada no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a modalidade "Leo" no painel de *Modalidades* |
| **QUANDO** alterar o nome/descrição para "Leo valesk" |
| **E** alterar o seletor de status para "Inativo" e retornar para "Ativo" / salvar alterações |
| **ENTÃO** os dados e o status da modalidade devem ser atualizados |
| **E** a tabela deve refletir as novas informações de nome e status. |

| **Critérios de Aceitação** |
| --- |
| * As modificações de texto e status devem ser atualizadas na base de dados. |
| * A tabela de modalidades deve recarregar exibindo os dados atualizados. |

---

#### Caso de Teste 04: Edição de Horário e Atualização de Turma

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Validar a atualização dos parâmetros de horário e vagas de uma turma recorrente cadastrada. |

| **Pré-condições** |
| --- |
| Existir uma turma recorrente cadastrada na listagem de turmas. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a turma cadastrada na listagem |
| **QUANDO** alterar os horários de início e fim nos campos correspondentes (ex: definindo de "09:30" até "12:30") |
| **E** clicar no botão **+ Turma** ou ícone de edição/salvar |
| **ENTÃO** o intervalo de horário da turma deve ser atualizado |
| **E** a tabela deve exibir a nova faixa de horário configurada. |

| **Critérios de Aceitação** |
| --- |
| * As alterações nos campos de horário devem persistir corretamente no banco de dados. |
| * A grade de exibição de turmas deve refletir o novo intervalo de tempo. |

---

#### Caso de Teste 05: Exclusão de Turma

| ID | Descrição |
| --- | --- |
| **C01-CT05** | Validar a funcionalidade de remoção de uma turma recorrente cadastrada no sistema. |

| **Pré-condições** |
| --- |
| Existir uma turma recorrente cadastrada na listagem do Box. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a turma na listagem de turmas recorrentes |
| **QUANDO** clicar no botão de exclusão (lixeira) correspondente à turma |
| **E** confirmar a ação no modal de confirmação, se exibido |
| **ENTÃO** a turma deve ser removida da base de dados |
| **E** a listagem deve ser atualizada deixando de exibir a turma excluída. |

| **Critérios de Aceitação** |
| --- |
| * A turma selecionada deve ser removida permanentemente do sistema. |
| * O botão de exclusão deve disparar a rotina de deleção sem falhas de execução ou travamentos na interface. |

https://jam.dev/c/f3126bb6-21e6-4af8-ad30-bea4effe0d7a
