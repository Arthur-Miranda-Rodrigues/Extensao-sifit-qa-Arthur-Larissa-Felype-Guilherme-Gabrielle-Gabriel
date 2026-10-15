
---

# Cenário 20: Gestão de Grupos

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 20: Gestão de Grupos** do módulo **Treinamento > Grupos** do sistema **SiFit**. O objetivo é validar a filtragem e pesquisa por múltiplos parâmetros, o cadastro de novos grupos, a edição e atualização de registros (incluindo a validação do comportamento de status), e o tratamento de integridade referencial em tentativas de exclusão de registros vinculados.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Grupos

#### Caso de Teste 01: Filtragem e Pesquisa de Grupos

| ID | Descrição |
| --- | --- |
| **C20-CT01** | Validar o funcionamento dos filtros por Código, Nome, Status e Tipo de Caixa na listagem de grupos. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Grupos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Grupos**<br> |
| **QUANDO** preencher o campo **Código** com "1" e realizar a busca. |
| **E** limpar o campo **Código**, preencher o campo **Nome do grupo** com "Treino" e filtrar pelo nome completo "Treino Personal". |
| **E** selecionar a opção "Inativo" no campo **Status** e clicar no botão de pesquisa. |
| **E** selecionar o tipo de caixa "Externo" no campo **Tipo Caixa** e clicar no botão de pesquisa. |
| **ENTÃO** a tabela deve ser atualizada exibindo apenas os registros correspondentes aos filtros aplicados em cada etapa. |
| **E** apresentar a mensagem *"Nenhum grupo encontrado"* quando não houver correspondências na consulta. |

| **Critérios de Aceitação** |
| --- |
| * Apenas os registros equivalentes aos critérios pesquisados (Código, Nome, Status ou Tipo de Caixa) devem ser exibidos na grade. |
| * Caso nenhum registro atenda aos parâmetros filtrados, a mensagem informativa de tabela vazia deve ser exibida. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tRwtlNGAqZKTUXOjOs6_zM0hjk1GhFte/view?usp=sharing |

---

#### Caso de Teste 02: Inclusão de Novo Grupo

| ID | Descrição |
| --- | --- |
| **C20-CT02** | Validar o registro de um novo grupo preenchendo os campos obrigatórios e definindo o status como inativo. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Grupos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Grupos**<br> |
| **E** clica no botão de cadastro (**+**).|
| **QUANDO** preencher o campo **Nome** com "Grupo dos Marombas" no modal **Novo Grupo**<br> |
| **E** manter o campo **Status** como "Ativo" (ou definir conforme fluxo) e configurar o tipo de caixa como "Externo". |
| **E** preencher a **Descrição** e clicar no botão **Salvar Grupo**<br> |
| **ENTÃO** o novo grupo deve ser cadastrado com sucesso. |
| **E** o registro deve ser adicionado e exibido na tabela principal. |

| **Critérios de Aceitação** |
| --- |
| * O novo grupo cadastrado deve ser inserido na base de dados e vinculado às suas respectivas propriedades. |
| * O registro recém-criado deve constar na listagem principal. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1PxwoOnZ6m7QmSlsoLDT9gSBwMAorI6B3/view?usp=sharing |

---

#### Caso de Teste 03: Inclusão de Grupo com Preenchimento Obrigatório e Validação

| ID | Descrição |
| --- | --- |
| **C20-CT03** | Validar a obrigatoriedade de preenchimento dos campos essenciais ao tentar salvar um novo grupo sem as informações necessárias. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Grupos** e com o modal **Novo Grupo** aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário abre o modal **Novo Grupo**<br> |
| **QUANDO** tenta clicar diretamente no botão **Salvar Grupo** sem preencher o nome. |
| **ENTÃO** o sistema deve exibir mensagens de validação solicitando o preenchimento do campo obrigatório (*"Preencha este campo"*). |
| **QUANDO** o usuário preenche o campo **Nome** (ex.: "Leon"), define o **Tipo Caixa** como "Interno" e clica em **Salvar Grupo**<br> |
| **ENTÃO** o grupo é cadastrado e listado com sucesso na tabela principal. |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir o salvamento de registros sem o preenchimento dos campos obrigatórios. |
| * Mensagens visuais de alerta devem orientar corretamente o usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1xRh8XshoGdSRG9vHYGiDHH3gYKQISRGL/view?usp=sharing |

---

#### Caso de Teste 04: Edição e Atualização de Grupo Existente

| ID | Descrição |
| --- | --- |
| **C20-CT04** | Verificar a alteração das configurações de código, descrição, tipo de caixa e status em grupos cadastrados. |

| **Pré-condições** |
| --- |
| Existirem grupos previamente cadastrados na base de dados.  |

| **Passos** |
| --- |
| **DADO** que o usuário localiza um grupo na listagem principal e clica no ícone de edição (lápis). |
| **QUANDO** altera o código, a descrição, o tipo de caixa e tenta modificar o **Status** de "Ativo" para "Inativo" no modal de edição. |
| **E** clica no botão **Salvar Grupo**<br> |
| **ENTÃO** os dados alterados deveriam ser gravados na base de dados e refletidos na listagem, mas os **Status** se mantem "Ativo". |

| **Critérios de Aceitação** |
| --- |
| * As modificações salvas no modal devem persistir no banco de dados e atualizar a grade principal. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Yi157R7voRJfQg9BsBddk1HcqLlnF-y4/view?usp=sharing |

---

#### Caso de Teste 05: Tentativa de Exclusão de Grupo Vinculado 

| ID | Descrição |
| --- | --- |
| **C20-CT05** | Verificar a validação de integridade referencial do sistema ao tentar excluir um grupo que possui vínculos ativos. |

| **Pré-condições** |
| --- |
| Existir um grupo cadastrado no sistema que possua dependências ou vínculos ativos. |

| **Passos** |
| --- |
| **DADO** que o usuário identifica o grupo vinculado na tabela principal. |
| **QUANDO** clicar no ícone de remoção (lixeira) na linha do registro. |
| **E** clicar no botão **Confirmar** dentro do modal de confirmação (*"Deseja deletar o Grupo?"*). |
| **ENTÃO** o sistema deve impedir a remoção do registro. |
| **E** exibir uma mensagem de erro indicando a impossibilidade de exclusão (*"Erro / Erro ao deletar Grupo"*). |

| **Critérios de Aceitação** |
| --- |
| * Registros com relacionamentos ou vínculos ativos na base de dados não podem ser excluídos. |
| * Uma mensagem de alerta amigável deve ser apresentada ao usuário, preservando os dados cadastrados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1XOjyUzN0LwOnJBfguLCeHFa7eEQv6MIl/view?usp=sharing |


