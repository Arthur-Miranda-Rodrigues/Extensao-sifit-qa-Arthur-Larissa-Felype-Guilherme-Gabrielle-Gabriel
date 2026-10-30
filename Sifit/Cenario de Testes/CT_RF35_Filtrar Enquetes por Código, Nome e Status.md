## Cenário 35: Módulo de Enquetes

### Caso de Teste 01: Filtrar enquetes por Código, Nome e Status

| ID | Descrição |
| --- | --- |
| **C35-CT01** | O sistema deve permitir a filtragem da lista de enquetes pelos campos Código, Nome e Status (Todos/Ativo/Inativo). |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela "Enquetes", com enquetes cadastradas (ex.: "tasa", códigos 1 a 3, sendo a de código 2 inativa). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Enquetes" |
| **QUANDO** preencher o campo "Nome" com "tasa" e clicar em "Buscar" |
| **ENTÃO** a tabela deve listar apenas as enquetes cujo nome corresponde a "tasa" (3 registros) |
| **E** ao limpar o nome, preencher o campo "Código" com "7" e clicar em "Buscar" |
| **ENTÃO** a tabela deve listar apenas os registros correspondentes ao código pesquisado |
| **E** ao limpar o código, selecionar o "Status" como "Ativo" e clicar em "Buscar" |
| **ENTÃO** a tabela deve listar apenas as enquetes ativas |
| **E** ao alterar o "Status" para "Inativo" e clicar em "Buscar" |
| **ENTÃO** a tabela deve listar apenas a enquete inativa (1 registro) |
| **E** ao selecionar "Todos" e clicar em "Buscar", a listagem completa deve ser exibida novamente. |

| **Critérios de Aceitação** |
| --- |
| Os filtros devem retornar exatamente os registros condizentes com os parâmetros informados, exibindo a contagem correta de registros encontrados. |
| Quando não houver registros para o filtro aplicado, deve ser exibida a mensagem "Nenhuma enquete encontrada". |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KvdZ5lvSkokgo4KIiFTT5mwUE2z2g9dD/view?usp=sharing |

---

### Caso de Teste 04: Tratar erro ao excluir uma enquete com confirmação

| ID | Descrição |
| --- | --- |
| **C35-CT04** | O sistema deve solicitar confirmação antes da exclusão e reportar a falha caso o registro não possa ser removido. |

| **Pré-condições** |
| --- |
| Deve haver enquetes visíveis na listagem (ex.: código 1, "tasa"). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (X) da enquete de código 1 |
| **E** o modal de confirmação "Deseja deletar a Enquete?" é exibido com as opções "Cancelar" e "Confirmar" |
| **QUANDO** clicar no botão "Confirmar" |
| **ENTÃO** o sistema deve exibir o modal "Erro" com a mensagem "Erro ao deletar Enquete" |
| **E** ao clicar em "Fechar", a listagem deve permanecer inalterada. |

| **Critérios de Aceitação** |
| --- |
| A exclusão só deve ser acionada após confirmação explícita no modal. |
| Em caso de falha na requisição, deve ser apresentada mensagem descritiva de erro, e o registro deve permanecer na listagem (indicadores inalterados). |

| **Observação (comportamento verificado na gravação)** |
| --- |
| A enquete não foi excluída: após confirmar, o sistema exibiu o modal **"Erro – Erro ao deletar Enquete"**, e o total de enquetes permaneceu em 26. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1T5NkHzsYMznhO__HtoEpzEC5YpYpzEyW/view?usp=sharing |
