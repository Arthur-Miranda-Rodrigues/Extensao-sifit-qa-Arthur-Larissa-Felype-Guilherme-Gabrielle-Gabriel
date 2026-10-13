Aqui está a documentação reestruturada e padronizada do **Módulo de Gestão de Turmas (RF15 - SIFIT)**, formatada em tabelas com cenários BDD/Gherkin e critérios de aceitação:

---

# Cenário de teste:Gestão de Turmas

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 15 (RF15) - Gestão de Turmas** do módulo **Treinamento > Turmas** do sistema **SiFit**. O objetivo é validar a filtragem e pesquisa de turmas por múltiplos parâmetros, a alteração de status/configurações de turmas cadastradas, a inclusão de novas turmas com seus respectivos planos e horários, e a remoção de registros inativos.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Turmas

#### Caso de Teste 01: Filtragem e Pesquisa de Turmas

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar o funcionamento dos filtros por Código, Nome da Turma e Status na listagem de turmas. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página de **Turmas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Turmas** |
| **QUANDO** preencher o campo **Código** com "1" e clicar em **Buscar** |
| **E** limpar o campo de código, preencher o campo **Nome da Turma** com "teste" e clicar em **Buscar** |
| **E** limpar o campo de nome, selecionar a opção "Inativo" no campo **Status** e clicar no botão **Buscar** |
| **ENTÃO** a tabela deve ser atualizada exibindo apenas as turmas correspondentes aos filtros aplicados em cada etapa |
| **E** apresentar a mensagem *"Nenhuma turma encontrada"* quando não houver registros que atendam aos critérios de pesquisa. |

| **Critérios de Aceitação** |
| --- |
| * Apenas as turmas equivalentes aos parâmetros pesquisados (Código, Nome ou Status) devem ser apresentadas na grade. |
| * Caso nenhum registro corresponda aos filtros aplicados, o sistema deve exibir a mensagem indicativa de tabela vazia. |

---

#### Caso de Teste 02: Edição e Atualização de Turma Existente

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Verificar a alteração de configurações e status de uma turma já cadastrada no sistema. |

| **Pré-condições** |
| --- |
| Existir a turma "Horário da" (Código 8) cadastrada na base de dados. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a turma "Horário da" (Código 8) na listagem de turmas |
| **QUANDO** clicar no ícone de edição (Lápis) |
| **E** alterar o campo **Status** para "Inativo" dentro do modal **Editar Turma** |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações da turma devem ser gravadas com sucesso |
| **E** a turma deve ter seu status atualizado para "Inativo" ao filtrar na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * As modificações de status realizadas no modal devem persistir no banco de dados. |
| * A listagem principal deve refletir a atualização do status após o salvamento. |

---

#### Caso de Teste 03: Inclusão de Nova Turma

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar o registro de uma nova turma preenchendo os campos obrigatórios, planos, personal e dias de aula. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Turmas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Turmas** |
| **E** clica no botão **Cadastrar Turma** |
| **QUANDO** preencher o campo **Nome** com "Turma dos Bodybuilders" no modal **Cadastrar Turma** |
| **E** selecionar o **Plano** "AVA", marcar **Aula Experimental** como "Sim", definir o **Tempo (meses)** como "16" e **Tem Personal** como "Sim" |
| **E** selecionar a personal "Marília Rhana Souza" e marcar os dias da semana ("Seg", "Ter", "Qua", "Qui", "Sex", "Sáb") |
| **E** clicar no botão **Salvar** |
| **ENTÃO** a nova turma deve ser registrada com sucesso |
| **E** o registro "Turma dos Bodybuilders" deve constar disponível na listagem geral de turmas. |

| **Critérios de Aceitação** |
| --- |
| * A nova turma deve ser inserida na base de dados com todas as informações e dias selecionados associados corretamente. |
| * A tabela principal deve atualizar exibindo o novo registro recém-criado. |

---

#### Caso de Teste 04: Exclusão de Turma

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Verificar a funcionalidade de remoção de uma turma inativa do sistema. |

| **Pré-condições** |
| --- |
| Existir a turma "Horário da" (Código 8) com status inativo na listagem de turmas. |

| **Passos** |
| --- |
| **DADO** que o usuário filtra pelo status "Inativo" e localiza a turma "Horário da" (Código 8) |
| **QUANDO** clicar no ícone de exclusão (Lixeira) na linha correspondente à turma |
| **E** clicar no botão **Confirmar** dentro do modal de confirmação (*"Deseja deletar esta turma?"*) |
| **ENTÃO** o sistema deve remover a turma da base de dados |
| **E** atualizar a listagem confirmando a exclusão e deixando de exibir o registro. |

| **Critérios de Aceitação** |
| --- |
| * A turma excluída deve ser removida permanentemente ou desativada conforme as regras do sistema, deixando de constar na grade. |
| * O modal de confirmação deve processar a exclusão sem retornar erros de sistema. |

https://jam.dev/c/580df45f-52e6-43c2-94f8-783cc8027bbd 

