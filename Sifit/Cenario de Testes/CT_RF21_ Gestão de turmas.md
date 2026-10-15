---

# Cenário 21: Gestão de Turmas

---

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 21: Gestão de Turmas** do módulo **Treinamento > Turmas** do sistema **SiFit**. O objetivo é validar a filtragem e pesquisa de turmas, o cadastro de novas turmas com plano, horários, personal e dias de aula, as validações de campos obrigatórios do cadastro, a edição de turmas existentes e a exclusão de turmas.

---

## 2. Cenários de Teste

### Cenário 01: Gestão de Turmas

#### Caso de Teste 01: Filtragem e Pesquisa de Turmas

| ID | Descrição |
| --- | --- |
| **C21-CT01** | Validar o funcionamento dos filtros por Nome da Turma, Código e Status, e do botão de limpar filtros, na listagem de turmas. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página de **Turmas**, com turmas cadastradas (Códigos 1, 2, 3, 4, 7 e 9) com status "Ativo". |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Turmas** com a listagem completa exibida |
| **QUANDO** preencher o campo **Nome da Turma** com "Horario da Noite" e clicar em **Buscar** |
| **E** limpar o campo de nome, preencher o campo **Código** com "1" e clicar em **Buscar** |
| **E** limpar o campo de código, selecionar a opção "Ativo" no campo **Status** e clicar em **Buscar** |
| **E** selecionar a opção "Inativo" no campo **Status** e clicar em **Buscar** |
| **E** selecionar novamente a opção "Ativo" e clicar no botão de limpar filtros (ícone de atualizar) |
| **ENTÃO** a tabela deve ser atualizada exibindo apenas as turmas correspondentes aos filtros aplicados em cada etapa |
| **E** apresentar a mensagem *"Nenhuma turma encontrada"* quando não houver registros que atendam aos critérios (Status "Inativo") |
| **E** exibir novamente todas as turmas ao limpar os filtros. |

| **Critérios de Aceitação** |
| --- |
| * Ao filtrar pelo nome "Horario da Noite", apenas a turma de Código 7 deve ser exibida. |
| * Ao filtrar pelo código "1", apenas a turma "Teste" (Código 1) deve ser exibida. |
| * Ao filtrar por Status "Ativo", todas as turmas ativas devem ser exibidas. |
| * Ao filtrar por Status "Inativo", sem turmas inativas cadastradas, o sistema deve exibir a mensagem "Nenhuma turma encontrada". |
| * O botão de limpar filtros deve restaurar os campos para o estado inicial (Status "Todos") e exibir a listagem completa. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1BnpspnJvK_bBPbJ_HAhHqp0j7jj93pYu/view?usp=sharing |

---

#### Caso de Teste 02: Cadastro de Nova Turma

| ID | Descrição |
| --- | --- |
| **C21-CT02** | Validar o cadastro de uma nova turma preenchendo nome, plano, aula experimental, tempo, horários, personal e dias da semana. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Turmas**. |
| Existir o plano "AVA" e o personal "Marcelo Longo Zandonadi" cadastrados no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Turmas** |
| **E** clica no botão **Cadastrar Turma** |
| **QUANDO** preencher o campo **Nome** com "Turma dos Marombas" no modal **Cadastrar Turma** |
| **E** selecionar o **Plano** "AVA" e marcar **Aula Experimental** como "Sim" |
| **E** preencher o campo **Tempo (meses)** com "16" |
| **E** manter a **Hora Inicial** em "09:00" e alterar a **Hora Final** para "21:00" |
| **E** marcar **Tem Personal** como "Sim" e selecionar o **Nome do Personal** "Marcelo Longo Zandonadi" |
| **E** marcar os dias da semana "Seg", "Ter", "Qua", "Qui" e "Sex" |
| **E** clicar no botão **Salvar** |
| **ENTÃO** a nova turma deve ser registrada com sucesso |
| **E** a turma "Turma dos Marombas" (Código 10) deve constar na listagem com plano "AVA", horário "09:00:00 - 21:00:00", dias "Seg, Ter, Qua, Qui, Sex" e o personal "Marcelo Longo Zandonadi" |
| **E** os indicadores de Turmas cadastradas, Turmas ativas, Com personal e Aula experimental devem ser incrementados em 1 (de 6/6/3/3 para 7/7/4/4). |

| **Critérios de Aceitação** |
| --- |
| * A nova turma deve ser inserida na base de dados com todas as informações e dias selecionados associados corretamente. |
| * A tabela principal deve exibir o novo registro recém-criado, com status "Ativo". |
| * Os cards de indicadores devem refletir o novo cadastro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/148Ky85R9QKucwU8Kt5OMLmO5gbBqS0t0/view?usp=sharing |

---

#### Caso de Teste 03: Validação de Campos Obrigatórios no Cadastro de Turma

| ID | Descrição |
| --- | --- |
| **C21-CT03** | Verificar as mensagens de validação exibidas ao tentar salvar uma turma sem preencher os campos obrigatórios (nome, plano, dia da semana e personal). |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Turmas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Turmas** |
| **E** clica no botão **Cadastrar Turma** |
| **QUANDO** clicar em **Salvar** com o campo **Nome** vazio |
| **E** preencher o campo **Nome** com "Turma dos durões", manter o **Plano** em "Selecione" e clicar em **Salvar** |
| **E** selecionar o **Plano** "Plano Diário", não marcar nenhum dia da semana e clicar em **Salvar** |
| **E** preencher o **Tempo (meses)** com "123", marcar os dias "Ter", "Qua", "Qui", "Sex" e "Sáb", marcar **Aula Experimental** como "Sim" e **Tem Personal** como "Sim" |
| **E** clicar em **Salvar** sem selecionar o **Nome do Personal** |
| **E** clicar em **Entendi** no aviso e em **Cancelar** no modal |
| **ENTÃO** o sistema deve exibir, a cada tentativa, um modal de **Aviso** com as mensagens *"Informe o nome da turma."*, *"Selecione um plano."*, *"Selecione ao menos um dia da semana."* e *"Selecione o personal."*, respectivamente |
| **E** nenhuma turma deve ser cadastrada. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve impedir o salvamento enquanto o nome, o plano, ao menos um dia da semana e (quando "Tem Personal" for "Sim") o personal não forem informados. |
| * Cada validação deve exibir a mensagem de aviso correspondente ao campo pendente. |
| * Após cancelar, o total de turmas cadastradas deve permanecer inalterado (7). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/14OC4o1CnzRuvTymcx1-7U_wcWbduwBb1/view?usp=sharing |

---

#### Caso de Teste 04: Edição e Atualização de Turma Existente

| ID | Descrição |
| --- | --- |
| **C21-CT04** | Verificar a alteração do nome e das configurações de personal de uma turma já cadastrada no sistema. |

| **Pré-condições** |
| --- |
| Existir a turma "Teste" (Código 1) cadastrada, com plano "AVA", personal "Mátila Rhana Souza" e dias "Ter, Qui". |
| Existir o personal "Marcelo Longo Zandonadi" cadastrado no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a turma "Teste" (Código 1) na listagem de turmas |
| **QUANDO** clicar no ícone de edição (Lápis) |
| **E** alterar o campo **Nome** para "Teste2" no modal **Editar Turma** |
| **E** alterar o campo **Tem Personal** para "Não" e clicar em **Salvar** |
| **E** fechar o aviso de erro, alterar novamente o campo **Tem Personal** para "Sim" e selecionar o **Nome do Personal** "Marcelo Longo Zandonadi" |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações da turma devem ser gravadas com sucesso |
| **E** a listagem deve exibir a turma de Código 1 com o nome "Teste2" e o personal "Marcelo Longo Zandonadi". |

| **Critérios de Aceitação** |
| --- |
| * As modificações realizadas no modal devem persistir no banco de dados. |
| * A listagem principal deve refletir o novo nome e o novo personal após o salvamento. |
| * O sistema não deve exibir erro ao salvar uma edição válida. |

| **Observações** |
| --- |
| * Ao abrir o modal **Editar Turma**, o campo **Status** é exibido vazio, sem refletir o status atual ("Ativo") da turma. |
| * Ao salvar com **Tem Personal** = "Não", o sistema exibiu o modal de **Erro** com a mensagem *"Erro ao salvar turma."*. |
| * Após o salvamento bem-sucedido, o modal exibiu momentaneamente a tela **Cadastrar Turma** vazia antes de retornar à listagem. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing |

---

#### Caso de Teste 05: Exclusão de Turma

| ID | Descrição |
| --- | --- |
| **C21-CT05** | Verificar a funcionalidade de remoção de uma turma do sistema. |

| **Pré-condições** |
| --- |
| Existir a turma "Teste" (Código 2) cadastrada na listagem de turmas (7 turmas cadastradas). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a turma "Teste" (Código 2) na listagem de turmas |
| **QUANDO** clicar no ícone de exclusão (Lixeira) na linha correspondente à turma |
| **E** clicar no botão **Confirmar** dentro do modal de confirmação (*"Deseja deletar esta turma?"*) |
| **ENTÃO** o sistema deve remover a turma da base de dados |
| **E** a listagem deve deixar de exibir a turma "Teste" (Código 2) |
| **E** os indicadores devem ser atualizados (Turmas cadastradas e Turmas ativas de 7 para 6, Com personal de 4 para 3 e Aula experimental de 4 para 3). |

| **Critérios de Aceitação** |
| --- |
| * A turma excluída deve ser removida da base de dados, deixando de constar na grade. |
| * O modal de confirmação deve processar a exclusão sem retornar erros de sistema. |
| * Os cards de indicadores devem refletir a exclusão. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1kPl1cUPSCTGhuo1NTWCUMiJJsEbBjN_w/view?usp=sharing |
