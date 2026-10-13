Aqui está a documentação reestruturada e padronizada do **Módulo de Gestão de Grupos (RF13 - SIFIT)**, formatada estritamente em tabelas com cenários BDD/Gherkin e critérios de aceitação:

---

# Cenário de teste:Gestão de Grupos

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 13 (RF13) - Gestão de Grupos** do módulo **Treinamento > Grupos** do sistema **SiFit**. O objetivo é validar a filtragem e pesquisa por múltiplos parâmetros, a edição de registros existentes, o cadastro de novos grupos com status inativo e o tratamento de integridade referencial em tentativas de exclusão de registros vinculados.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Grupos

#### Caso de Teste 01: Filtragem e Pesquisa de Grupos

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar o funcionamento dos filtros por Código, Nome, Status e Tipo de Caixa na listagem de grupos. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Grupos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Grupos** |
| **QUANDO** preencher o campo **Código** com "1" e realizar a busca |
| **E** limpar o campo **Código**, preencher o campo **Nome do grupo** com "Treino" e filtrar pelo nome completo "Treino Personal" |
| **E** selecionar a opção "Inativo" no campo **Status** e clicar no botão de pesquisa |
| **E** selecionar o tipo de caixa "Externo" no campo **Tipo Caixa** e clicar no botão de pesquisa |
| **ENTÃO** a tabela deve ser atualizada exibindo apenas os registros correspondentes aos filtros aplicados em cada etapa |
| **E** apresentar a mensagem *"Nenhum grupo encontrado"* quando não houver correspondências na consulta. |

| **Critérios de Aceitação** |
| --- |
| * Apenas os registros equivalentes aos critérios pesquisados (Código, Nome, Status ou Tipo de Caixa) devem ser exibidos na grade. |
| * Caso nenhum registro atenda aos parâmetros filtrados, a mensagem informativa de tabela vazia deve ser exibida. |

---

#### Caso de Teste 02: Edição e Atualização de Grupo Existente

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Verificar a alteração das configurações de status e tipo de caixa em grupos cadastrados. |

| **Pré-condições** |
| --- |
| Existirem grupos previamente cadastrados na base de dados (ex.: "Teste", Código 3 e "Teste Novo", Código 5). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o grupo "Teste" (Código 3) na listagem principal |
| **QUANDO** clicar no ícone de edição (lápis) |
| **E** alterar o **Status** para "Inativo" e o **Tipo Caixa** para "Interno" no modal **Editar Grupo** |
| **E** clicar no botão **Salvar Grupo** |
| **E** repetir a operação para o grupo "Teste Novo" (Código 5), alterando o **Status** para "Inativo" e clicando em **Salvar Grupo** |
| **ENTÃO** as alterações do formulário devem ser gravadas na base de dados |
| **E** os novos dados editados devem ser refletidos e atualizados na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * Todas as modificações salvas no modal (Status e Tipo Caixa) devem persistir no banco de dados. |
| * A grade da listagem principal deve atualizar imediatamente mostrando os novos valores dos registros editados. |

---

#### Caso de Teste 03: Inclusão de Novo Grupo com Status Inativo

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar o registro de um novo grupo preenchendo os campos obrigatórios e definindo o status como inativo. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página de **Grupos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Grupos** |
| **E** clica no botão de cadastro (**+**) |
| **QUANDO** preencher o campo **Nome** com "Teste 2" no modal **Novo Grupo** |
| **E** alterar o campo **Status** para "Inativo" |
| **E** preencher o campo **Descrição** com "teste 2" |
| **E** clicar no botão **Salvar Grupo** |
| **ENTÃO** o novo grupo deve ser cadastrado com sucesso |
| **E** o registro "Teste 2" deve ser adicionado e exibido na tabela principal. |

| **Critérios de Aceitação** |
| --- |
| * O novo grupo cadastrado deve ser inserido na base de dados e vinculado às suas respectivas propriedades. |
| * O registro recém-criado deve constar na listagem principal mantendo o status "Inativo". |

---

#### Caso de Teste 04: Tentativa de Exclusão de Grupo Vinculado

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Verificar a validação de integridade referencial do sistema ao tentar excluir um grupo que possui vínculos ativos. |

| **Pré-condições** |
| --- |
| Existir um grupo cadastrado no sistema que possua dependências ou vínculos ativos. |

| **Passos** |
| --- |
| **DADO** que o usuário identifica o grupo vinculado na tabela principal |
| **QUANDO** clicar no ícone de remoção (lixeira) na linha do registro |
| **E** clicar no botão **Confirmar** dentro do modal de confirmação (*"Deseja deletar o Grupo?"*) |
| **ENTÃO** o sistema deve impedir a remoção do registro |
| **E** exibir uma mensagem de erro indicando a impossibilidade de exclusão (ex.: *"Erro ao deletar Grupo"*). |

| **Critérios de Aceitação** |
| --- |
| * Registros com relacionamentos ou vínculos ativos na base de dados não podem ser excluídos. |
| * Uma mensagem de alerta amigável deve ser apresentada ao usuário, preservando os dados cadastrados. |

https://jam.dev/c/f449384d-fb57-4e6e-8acf-71fcfbb6a69d
