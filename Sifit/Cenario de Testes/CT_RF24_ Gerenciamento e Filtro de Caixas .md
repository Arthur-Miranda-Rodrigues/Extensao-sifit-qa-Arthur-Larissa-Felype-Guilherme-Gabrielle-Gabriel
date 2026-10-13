
## Cenário de teste: Gerenciamento e Filtro de Caixas no Módulo Financeiro

### Caso de Teste 01: Abrir um novo caixa com dados válidos

| ID | Descrição |
| --- | --- |
| C06-CT01 | O sistema deve permitir a abertura de um novo caixa selecionando um local válido. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e com permissões para gerenciar caixas. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela "Caixas" |
| **E** clica no botão "Abrir Caixa" |
| **E** seleciona um "Local de Contas" válido (ex.: "Caixa Muay Thai") |
| **QUANDO** clicar em "Salvar" |
| **ENTÃO** o novo caixa deve ser aberto com status "ABERTO" e listado na tabela |

| **Critérios de aceitação** |
| --- |
| O caixa cadastrado deve exibir o status "ABERTO" em destaque verde na listagem. |

---

### Caso de Teste 02: Filtrar caixas por status "Aberto" e "Fechado"

| ID | Descrição |
| --- | --- |
| C06-CT02 | O sistema deve filtrar e exibir apenas os caixas correspondentes ao status selecionado. |

| **Pré-condições** |
| --- |
| Devem existir caixas cadastrados com status "ABERTO" e "FECHADO" no período selecionado. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela "Caixas" |
| **E** seleciona a opção "Aberto" (ou "Fechado") no campo de filtro "Status" |
| **QUANDO** clicar no botão "Buscar" |
| **ENTÃO** a tabela deve atualizar exibindo apenas os caixas correspondentes ao status selecionado |

| **Critérios de aceitação** |
| --- |
| A lista deve filtrar corretamente os registros de acordo com o status selecionado ou retornar a mensagem "Nenhum caixa encontrado" caso não haja registros. |

---

### Caso de Teste 03: Registrar conferência em um caixa com preenchimento obrigatório de motivo

| ID | Descrição |
| --- | --- |
| C06-CT03 | O sistema deve exigir a inclusão de um motivo ao registrar a conferência física do caixa. |

| **Pré-condições** |
| --- |
| Existir pelo menos um caixa listado para edição/fechamento. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição/visualização de um caixa |
| **E** clica em "Informar valor contado" (ou "Nova Conferência") |
| **E** insere o "Valor contado fisicamente" |
| **E** tenta clicar em "Registrar Conferência" sem preencher o campo "Motivo" |
| **QUANDO** o alerta "Informe o motivo da conferência" for exibido, o usuário clica em "Entendi", preenche o campo "Motivo" e clica novamente em "Registrar Conferência" |
| **ENTÃO** o sistema exibe a mensagem de confirmação "Conferência registrada com sucesso" |

| **Critérios de aceitação** |
| --- |
| A conferência só deve ser concluída se o campo "Motivo" estiver devidamente preenchido. |

https://jam.dev/c/504c40b9-a1f4-4b1a-87b9-ac134afdf171
