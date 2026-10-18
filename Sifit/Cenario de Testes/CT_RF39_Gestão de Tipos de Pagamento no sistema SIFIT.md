
---

## Cenário: Gestão de Tipos de Pagamento no sistema SIFIT

### Caso de Teste 01: Filtrar tipos de pagamento por Código, Nome e Tipo

| ID | Descrição |
| --- | --- |
| C12-CT01 | O sistema deve permitir a busca e filtragem precisa dos tipos de pagamento cadastrados. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e acessado a tela **Tipos de Pagamento**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Tipos de Pagamento"

 |
| **QUANDO** preenche o campo "Código" (ex: "3") ou o campo "Nome" (ex: "Cartão de Crédito")

 |
| **OU** seleciona a opção no filtro de "Tipo" (ex: "Crédito")

 |
| **ENTÃO** a tabela deve listar apenas os registros que atendam estritamente aos critérios de filtro aplicados.

 |

| **Critérios de aceitação** |
| --- |
| A busca por código, nome ou tipo deve retornar instantaneamente e atualizar o contador de registros exibidos na tabela.

 |

---

### Caso de Teste 02: Cadastrar um novo tipo de pagamento com sucesso

| ID | Descrição |
| --- | --- |
| C12-CT02 | O sistema deve permitir o cadastro de um novo tipo de pagamento definindo status, bandeira e integração. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Tipos de Pagamento**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "+ Novo" no canto superior direito

 |
| **E** preenche o "Nome" (ex: "Pix"), define o "Status" como "Ativo"

 |
| **E** seleciona a opção "Escolher Bandeira" (ex: "Sim"), "Tipo" (ex: "Débito")

 |
| **E** configura "Pagamento Pelo Sistema" (ex: "Sim")

 |
| **QUANDO** clica no botão "Salvar"

 |
| **ENTÃO** o modal fecha e o novo tipo de pagamento é exibido na tabela com os dados cadastrados.

 |

| **Critérios de aceitação** |
| --- |
| O novo registro deve ser persistido no sistema e atualizar os contadores no topo da página (Total, Inativos/Ativos, Via Gateway).

 |

---

### Caso de Teste 03: Editar e atualizar dados de um tipo de pagamento

| ID | Descrição |
| --- | --- |
| C12-CT03 | O sistema deve permitir a alteração das configurações de um tipo de pagamento cadastrado. |

| **Pré-condições** |
| --- |
| Existir tipos de pagamento listados na tabela.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de lupa/edição de um item na listagem (ex: "Dinheiro")

 |
| **E** altera o parâmetro "Pagamento Pelo Sistema" para "Sim"

 |
| **QUANDO** clica no botão "Salvar"

 |
| **ENTÃO** as modificações devem ser salvas e refletidas na coluna "VIA GATEWAY" da tabela.

 |

| **Critérios de aceitação** |
| --- |
| As propriedades modificadas devem ser persistidas com sucesso e atualizadas na listagem.

 |

---

### Caso de Teste 04: Tentar excluir tipo de pagamento vinculado e validar mensagem de erro

| ID | Descrição |
| --- | --- |
| C12-CT04 | O sistema deve bloquear a remoção de tipos de pagamento vinculados a outras operações e exibir mensagem de erro. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Tipos de Pagamento**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "X" (excluir) na linha de um tipo de pagamento

 |
| **E** confirma a intenção no modal "Deseja deletar o Tipo de Pagamento?" clicando em "Confirmar"

 |
| **QUANDO** o sistema tenta realizar a exclusão

 |
| **ENTÃO** deve ser exibido um modal de alerta com o título "Erro" e a mensagem "Erro ao deletar tipo de pagamento".

 |

| **Critérios de aceitação** |
| --- |
| O registro não deve ser excluído e o usuário deve conseguir fechar a mensagem de erro através do botão "Fechar".

 |

 https://jam.dev/c/ff1a4a81-aba2-45c2-87d4-c7b314eb1fbe
