
---

## Cenário: Gerenciamento de Pontuações no SIFIT

### Caso de Teste 01: Buscar pontuações por Código, Nome ou Status



| ID | Descrição |
| --- | --- |
| **PON-CT01** | O sistema deve permitir filtrar pontuações por código, nome da pontuação e status (Ativo/Inativo).

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela de "Pontuação".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Pontuação"

 |
| **QUANDO** preencher o campo "Código" (ex: "1") e clicar em "Buscar"

 |
| **ENTÃO** o sistema exibe apenas o registro do código informado

 |
| **E** ao pesquisar por "Nome da pontuação" (ex: "Teste Dezembro") e clicar em "Buscar"

 |
| **ENTÃO** o sistema filtra a tabela exibindo o registro correspondente

 |
| **E** ao alterar o filtro "Status" para "Inativo" e buscar

 |
| **ENTÃO** o sistema exibe a mensagem "Nenhuma pontuação encontrada" caso não existam itens inativos.

 |

| **Critérios de aceitação** |
| --- |
| A listagem deve responder corretamente a cada combinação de filtro aplicada.

 |

---

### Caso de Teste 02: Cadastrar nova pontuação e associar produtos de resgate



| ID | Descrição |
| --- | --- |
| **PON-CT02** | O sistema deve permitir a criação de uma nova campanha de pontuação com período e produto de resgate.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Pontuação".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica em "Nova Pontuação"

 |
| **E** preenche o "Nome" (ex: "Legpress")

 |
| **E** seleciona a "Data Inicial" e "Data Final" através do calendário

 |
| **E** define o "Tipo" (ex: "Por período") e "Status" como "Ativo"

 |
| **E** escolhe um produto em "Produtos de resgate" (ex: "Notebook Fitness")

 |
| **QUANDO** clicar em "Salvar"

 |
| **ENTÃO** a nova pontuação deve ser cadastrada com sucesso e exibida na tabela principal.

 |

| **Critérios de aceitação** |
| --- |
| O registro criado deve aparecer na lista com as datas e status configurados, e os contadores de pontuações no topo da tela devem ser incrementados.

 |

---

### Caso de Teste 03: Associar atividades a uma pontuação existente



| ID | Descrição |
| --- | --- |
| **PON-CT03** | O sistema deve permitir vincular atividades a uma campanha de pontuação.

 |

| **Pré-condições** |
| --- |
| Deve haver uma pontuação cadastrada na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Atividades da Pontuação" na coluna Ações de um registro

 |
| **E** no modal exibido, escolhe uma atividade no menu suspenso (ex: "Postar todos os treinos")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** as alterações devem ser gravadas no sistema.

 |

| **Critérios de aceitação** |
| --- |
| A atividade selecionada deve ser vinculada à pontuação com sucesso.

 |

---

### Caso de Teste 04: Visualizar Ranking de Participantes



| ID | Descrição |
| --- | --- |
| **PON-CT04** | O sistema deve permitir visualizar o ranking de participantes associados a uma pontuação.

 |

| **Pré-condições** |
| --- |
| Existir uma pontuação cadastrada na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Ranking de Participantes"

 |
| **QUANDO** o modal "Ranking de Participantes" for aberto

 |
| **ENTÃO** o sistema exibe os participantes e suas respectivas pontuações ou a mensagem "Nenhum participante encontrado" caso não haja pontuações registradas.

 |

| **Critérios de aceitação** |
| --- |
| O modal de ranking deve ser carregado exibindo a lista de participantes ou o aviso de lista vazia.

 |

---

### Caso de Teste 05: Excluir uma pontuação



| ID | Descrição |
| --- | --- |
| **PON-CT05** | O sistema deve permitir excluir uma pontuação existente após confirmação.

 |

| **Pré-condições** |
| --- |
| Deve existir ao menos uma pontuação cadastrada.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Excluir" (lixeira/X) de um registro (ex: "Legpress")

 |
| **E** o modal de confirmação "Deseja deletar a Pontuação?" é exibido

 |
| **QUANDO** clicar no botão "Confirmar"

 |
| **ENTÃO** a pontuação é removida da listagem e o contador total é atualizado.

 |

| **Critérios de aceitação** |
| --- |
| O registro excluído não deve mais constar na tabela de pontuações.

 |

---

### Caso de Teste 06: Tratar erros do servidor na edição de pontuação (Cenário de Exceção/Falha)



| ID | Descrição |
| --- | --- |
| **PON-CT06** | O sistema deve apresentar mensagem de erro amigável ao falhar ao salvar alterações de pontuação.

 |

| **Pré-condições** |
| --- |
| Ocorrer um erro interno do servidor ou falha de comunicação ao salvar alterações.

 |

| **Passos** |
| --- |
| **DADO** que o usuário edita uma pontuação existente

 |
| **E** tenta alterar o "Status" para "Inativo"

 |
| **QUANDO** clicar no botão "Salvar" e houver uma falha no backend/servidor

 |
| **ENTÃO** o sistema exibe um modal contendo a mensagem de erro (ex: "Erro no servidor - Erro interno inesperado" ou "Erro ao salvar pontuação").

 |

| **Critérios de aceitação** |
| --- |
| O modal de erro deve ser exibido informando a falha sem quebrar a interface da aplicação.

 |

https://jam.dev/c/60180959-723d-492f-9092-32c01b65c20a
