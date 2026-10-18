# Cenário 35: Módulo de Enquetes

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário Módulo de Enquetes** do menu **Enquetes** do sistema **SIFIT**. O objetivo é validar a filtragem da listagem por Código, Nome e Status, e o tratamento das mensagens de erro exibidas ao cadastrar, editar e excluir enquetes quando a operação não é concluída pelo servidor, conferindo também que a listagem e os indicadores do topo (Enquetes, Ativas, Inativas e Respostas) permanecem consistentes.

---

## 2. Casos de Teste

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

### Caso de Teste 02: Tratar erro ao cadastrar uma nova enquete

| ID | Descrição |
| --- | --- |
| **C35-CT02** | O sistema deve exibir um modal de erro quando o cadastro de uma nova enquete não puder ser concluído. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Enquetes". |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Enquete" |
| **E** preenche o campo "Nome" com "Músculo" |
| **E** preenche o campo "Pergunta" com "Qual é a proteína mais indicada?" |
| **E** informa as opções de resposta, adicionando campos pelo botão "+" (ex.: "Whey", "Carne bovina", "Carne suína" e "Carne de frango") |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o sistema deve exibir o modal "Erro" com a mensagem "Erro ao salvar enquete" |
| **E** ao clicar em "Fechar", o modal de erro deve ser encerrado. |

| **Critérios de Aceitação** |
| --- |
| Caso ocorra uma falha no processamento do cadastro, um alerta de erro deve ser exibido ao usuário com a opção de fechar, sem quebrar a interface. |
| A enquete não deve ser incluída na listagem quando o cadastro falhar. |

| **Observação (comportamento verificado na gravação)** |
| --- |
| O cadastro com todos os campos preenchidos (Nome, Pergunta e 4 respostas) não foi concluído: o sistema exibiu o modal **"Erro – Erro ao salvar enquete"**. Verificar se a falha decorre de um defeito no cadastro de enquetes. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1RbssKnL6GfKSsI4xUpaL4lWxSkU8wSD8/view?usp=sharing |

---

### Caso de Teste 03: Tratar erro ao editar uma enquete existente

| ID | Descrição |
| --- | --- |
| **C35-CT03** | O sistema deve tratar a falha ao salvar alterações em uma enquete existente e exibir o feedback adequado. |

| **Pré-condições** |
| --- |
| Deve existir ao menos uma enquete cadastrada na listagem (ex.: código 1, "tasa", sem pergunta cadastrada). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de visualizar/editar (lupa) da enquete de código 1 |
| **E** preenche o campo "Pergunta" (ex.: "teste") e adiciona respostas no modal "Enquete" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o sistema deve exibir o modal "Erro" com a mensagem "Erro ao salvar enquete" |
| **E** ao clicar em "Fechar" e em "Cancelar", o usuário deve retornar à listagem sem alterações. |

| **Critérios de Aceitação** |
| --- |
| O modal de edição deve carregar os dados cadastrados da enquete. |
| Em caso de erro no salvamento, a alteração não deve ser aplicada e a enquete deve manter o estado anterior na listagem ("Sem pergunta cadastrada"). |

| **Observação (comportamento verificado na gravação)** |
| --- |
| A edição não foi concluída: o sistema exibiu o modal **"Erro – Erro ao salvar enquete"** nas tentativas de salvar, e a enquete permaneceu sem pergunta cadastrada na listagem. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/15PBazaM8Wsb8qpbfW-f0oBQXLwXogc9p/view?usp=sharing |

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
