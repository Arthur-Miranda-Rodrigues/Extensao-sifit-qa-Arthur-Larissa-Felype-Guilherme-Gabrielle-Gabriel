
---

## Cenário de teste: Cadastro, Edição e Erro de Alteração em Pergunta de Anamnese

### Caso de Teste 01: Cadastrar pergunta e validar erro ao alterar tipo de resposta.

| ID | Descrição |
| --- | --- |
| C01-CT01 | O sistema deve permitir o cadastro de uma nova pergunta, mas deve exibir uma mensagem de erro ao tentar salvar uma alteração do tipo de resposta não permitida. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SIFIT e na tela de Perguntas Anamnese. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de "Perguntas Anamnese"

 |
| **E** clica no botão "Nova Pergunta"

 |
| **E** preenche o Nome com "Qual é o nome da academia" e Pergunta com "Qual é o nome da academia"

 |
| **E** define o Número como "5" e clica em "Salvar" |
| **QUANDO** o usuário tenta editar a pergunta recém-criada e altera o Tipo Resposta para "Se Sim, qual?" |
| **E** clica no botão "Salvar" |
| **ENTÃO** o sistema deve exibir a mensagem de erro "Erro ao salvar pergunta" |

| **Critérios de aceitação** |
| --- |
| O registro inicial é salvo com sucesso, porém a tentativa de alteração do Tipo Resposta é bloqueada exibindo um modal de erro. |

---

### Caso de Teste 02: Exclusão de pergunta da lista.

| ID | Descrição |
| --- | --- |
| C02-CT01 | O sistema deve permitir a exclusão de uma pergunta existente mediante confirmação. |

| **Pré-condições** |
| --- |
| Deve haver pelo menos uma pergunta cadastrada na listagem de Perguntas Anamnese.

 |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a lista de Perguntas Anamnese |
| **E** clica no ícone de exclusão (lixeira) de uma pergunta (ex: "Qual é o exercício?") |
| **QUANDO** o modal de confirmação "Deseja deletar esta pergunta?" for exibido |
| **E** o usuário clicar em "Confirmar" |
| **ENTÃO** o registro deve ser removido da listagem e a contagem de perguntas atualizada |

| **Critérios de aceitação** |
| --- |
| A pergunta selecionada é excluída permanentemente e deixa de ser exibida na tabela. |

---

## Cenário 02: Consulta, Filtros e Duplicidade na Anamnese

### Caso de Teste 01: Filtrar perguntas por Código e por Nome.

| ID | Descrição |
| --- | --- |
| C02-CT02 | O sistema deve filtrar corretamente as perguntas exibidas conforme os critérios de busca inseridos nos campos Código ou Nome. |

| **Pré-condições** |
| --- |
| Existem perguntas cadastradas na listagem (ex: códigos "3", "4" ou "5"). |

| **Passos** |
| --- |
| **DADO** que o usuário informa um código no campo de busca "Código" (ex: "3") e clica em "Buscar" |
| **QUANDO** o sistema processar a busca |
| **ENTÃO** deve exibir a mensagem "Nenhuma pergunta encontrada." caso o código não corresponda a nenhum registro |
| **E** ao buscar por um código/nome existente e clicar em "Buscar", deve filtrar e exibir apenas os registros correspondentes na tabela |

| **Critérios de aceitação** |
| --- |
| A listagem deve refletir precisamente o filtro aplicado e atualizar o total de registros encontrados. |

https://jam.dev/c/51a1cf79-bb03-45b5-8ee5-c79b9a4c2491
