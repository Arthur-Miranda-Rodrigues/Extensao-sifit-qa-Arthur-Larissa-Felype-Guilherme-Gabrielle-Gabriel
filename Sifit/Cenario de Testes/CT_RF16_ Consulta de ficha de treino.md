
---

# Cenário de teste:Gerenciamento de Fichas de Treino

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo **Treinamento > Fichas de Treino** do sistema **SiFit**. O objetivo é validar o cadastro de novas fichas, a busca/seleção de alunos via modal, a adição e estruturação de rotinas de exercícios por grupo muscular, a exclusão de fichas e a filtragem por nome na listagem principal.

---

## 2. Cenários de Teste

### Cenário 01: Cadastro e Gestão de Fichas de Treino

#### Caso de Teste 01: Cadastro de Ficha de Treino com Dados Válidos

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar a criação de uma nova ficha de treino preenchendo as informações obrigatórias no formulário. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Fichas de Treino**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Fichas de Treino** |
| **E** clica no botão **+ Cadastrar Ficha** |
| **E** pesquisa e seleciona o aluno desejado (ex.: "Fulano 1") no modal de busca |
| **E** seleciona o Personal responsável (ex.: "Gabriella") |
| **E** define as datas de início e término |
| **E** preenche o campo **Objetivo** (ex.: "Crescer") |
| **QUANDO** clicar no botão **Criar Nova Ficha** |
| **ENTÃO** a ficha de treino deve ser cadastrada com sucesso |
| **E** o registro deve ser exibido na tabela principal com o status padrão (ex.: "SEM STATUS"). |

| **Critérios de Aceitação** |
| --- |
| * A nova ficha de treino deve ser listada na grade principal sem erros. |
| * Todos os dados informados (Aluno, Personal, Datas e Objetivo) devem corresponder aos selecionados no formulário. |

---

#### Caso de Teste 02: Pesquisa e Seleção de Aluno no Cadastro da Ficha

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Validar a filtragem e seleção de alunos dentro do modal de pesquisa no cadastro de ficha. |

| **Pré-condições** |
| --- |
| Modal **Cadastrar Ficha de Treino** aberto no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Pesquisar** ao lado do campo **Aluno** |
| **QUANDO** digitar um nome inexistente (ex.: "Guilherme") e clicar em **Buscar** |
| **E** limpar o campo de busca e clicar em **Buscar** novamente para listar todos os registros |
| **E** clicar em **Selecionar** no registro do aluno desejado (ex.: "Fulano 1", código 207) |
| **ENTÃO** o modal de busca deve ser fechado |
| **E** o campo **Aluno** na tela de cadastro deve ser preenchido com as informações do aluno selecionado. |

| **Critérios de Aceitação** |
| --- |
| * A busca por nome inexistente não deve retornar registros. |
| * A limpeza da busca deve reexibir a lista completa de alunos cadastrados. |
| * O clique em "Selecionar" deve vincular corretamente o aluno ao formulário principal. |

---

#### Caso de Teste 03: Adição e Gestão de Exercícios na Ficha de Treino

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar a inclusão e configuração de grupos musculares e exercícios na ficha do aluno. |

| **Pré-condições** |
| --- |
| Existir uma ficha de treino previamente cadastrada na listagem principal. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de fichas de treino |
| **E** clica na opção de gerenciar/editar os treinos do aluno |
| **QUANDO** clicar em **Adicionar grupo muscular** |
| **E** selecionar os exercícios desejados (ex.: "Abdominais", "Apostamento", "Extensão") |
| **E** definir os parâmetros de treino (séries, repetições e carga/peso) |
| **E** clicar no botão **Salvar Alterações** |
| **ENTÃO** os grupos musculares e exercícios configurados devem ser vinculados à ficha do aluno |
| **E** a estrutura do treino deve ser exibida corretamente na consulta. |

| **Critérios de Aceitação** |
| --- |
| * As séries, repetições e cargas informadas devem persistir na ficha do aluno. |
| * A listagem do treino deve atualizar refletindo os exercícios adicionados. |

---

#### Caso de Teste 04: Exclusão de Ficha de Treino

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Validar a remoção de uma ficha de treino cadastrada no sistema. |

| **Pré-condições** |
| --- |
| Existir ao menos uma ficha cadastrada na tabela principal (ex.: ficha do aluno "Adrys Lougan"). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a ficha do aluno na tabela principal |
| **QUANDO** clicar no ícone de exclusão (lixeira) na coluna de ações |
| **E** clicar em **Confirmar** dentro do modal *"Deseja deletar esta ficha?"* |
| **ENTÃO** a ficha de treino deve ser removida da listagem principal |
| **E** o contador totalizador de fichas deve ser recalculado. |

| **Critérios de Aceitação** |
| --- |
| * A ficha excluída não deve mais constar na listagem ou nas consultas do aluno. |
| * A exclusão deve ser confirmada sem erros de processamento. |

---

#### Caso de Teste 05: Consulta e Filtro por Nome do Aluno

| ID | Descrição |
| --- | --- |
| **C01-CT05** | Validar a busca por nome de aluno na tabela de listagem de fichas de treino. |

| **Pré-condições** |
| --- |
| Existirem fichas cadastradas para múltiplos alunos na base de dados. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Fichas de Treino** |
| **QUANDO** preencher o campo de busca **Nome** com o nome do aluno (ex.: "Fulano") |
| **E** clicar no botão **Buscar** |
| **ENTÃO** a tabela deve filtrar e apresentar exclusivamente as fichas de treino pertencentes ao aluno pesquisado. |

| **Critérios de Aceitação** |
| --- |
| * Apenas fichas associadas ao nome/termo buscado devem ser apresentadas na grade. |
| * O tempo de resposta do filtro deve ser imediato ao clicar em "Buscar". |

https://jam.dev/c/e3638ce6-c06f-4544-8039-cb089651238d 
