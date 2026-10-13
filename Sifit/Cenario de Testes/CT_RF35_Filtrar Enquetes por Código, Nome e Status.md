
---

## Cenários de Teste: Módulo de Enquetes

### Caso de Teste 01: Filtrar Enquetes por Código, Nome e Status

| ID | Descrição |
| --- | --- |
| **ENQ-CT01** | O sistema deve permitir a filtragem da lista de enquetes através dos campos Código, Nome e Status (Ativo/Inativo/Todos).

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela "Enquetes".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de Enquetes

 |
| **QUANDO** preencher o campo "Código" com "4" e clicar em "Buscar"

 |
| **ENTÃO** apenas os registros correspondentes ao código pesquisado devem ser exibidos na tabela

 |
| **E** ao preencher o campo "Nome" com "tase" e clicar em "Buscar"

 |
| **ENTÃO** a tabela deve filtrar e listar apenas as enquetes que contenham "tase" no nome

 |
| **E** ao selecionar o filtro "Status" como "Inativo" e clicar em "Buscar"

 |
| **ENTÃO** a mensagem "Nenhuma enquete encontrada" deve ser apresentada caso não existam registros com esse status.

 |

| **Critérios de Aceitação** |
| --- |
| Os filtros devem retornar exatamente os registros condizentes com os parâmetros informados, exibindo a contagem correta de registros encontrados.

 |

---

### Caso de Teste 02: Validar Mensagem de Erro ao Criar Nova Enquete

| ID | Descrição |
| --- | --- |
| **ENQ-CT02** | O sistema deve exibir um modal de erro ao tentar salvar uma nova enquete que não atenda às regras de negócio/persistência.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de "Enquetes".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "+ Nova Enquete"

 |
| **E** preenche o campo "Nome" com "Tass"

 |
| **E** preenche o campo "Pergunta" com "O que é tass"

 |
| **E** informa uma ou mais opções nos campos de "Respostas" (ex: "Tass é um exercício", "Tass é uma pessoa")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** o sistema deve exibir um modal de feedback com a mensagem de erro: "Erro ao salvar enquete".

 |

| **Critérios de Aceitação** |
| --- |
| Caso ocorra uma falha no processamento do cadastro, um alerta amigável de erro deve ser exibido ao usuário com a opção de fechar.

 |

---

### Caso de Teste 03: Editar Status/Dados de Enquete Existente

| ID | Descrição |
| --- | --- |
| **ENQ-CT03** | O sistema deve tratar tentativas de alteração em enquetes existentes e exibir o feedback adequado.

 |

| **Pré-condições** |
| --- |
| Deve existir ao menos uma enquete cadastrada na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Detalhes/Editar" (lupa) de um registro (ex: Código 2)

 |
| **E** altera o parâmetro "Status" de "Ativo" para "Inativo" no modal

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** se aoperação não for concluída, o sistema deve exibir o modal de alerta com a mensagem "Erro ao salvar enquete".

 |

| **Critérios de Aceitação** |
| --- |
| O modal de edição deve carregar os dados cadastrados e, em caso de erro no salvamento, impedir a alteração inconsistente mantendo o estado anterior.

 |

---

### Caso de Teste 04: Excluir Enquete com Confirmação e Tratamento de Exceção

| ID | Descrição |
| --- | --- |
| **ENQ-CT04** | O sistema deve solicitar confirmação antes da exclusão e reportar falhas caso o registro não possa ser removido.

 |

| **Pré-condições** |
| --- |
| Deve haver registros de enquete visíveis na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (X) de uma enquete

 |
| **E** o modal de confirmação "Deseja deletar a Enquete?" é exibido na tela

 |
| **QUANDO** clicar no botão "Confirmar"

 |
| **ENTÃO** se houver erro ao deletar, o modal com a mensagem "Erro ao deletar Enquete" deve ser apresentado.

 |

| **Critérios de Aceitação** |
| --- |
| A exclusão só deve ser acionada após confirmação explícita no modal, apresentando mensagem descritiva de erro em caso de falha na requisição.

 |
