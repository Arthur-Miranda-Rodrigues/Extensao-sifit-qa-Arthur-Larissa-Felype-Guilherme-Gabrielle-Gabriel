## Cenário 44: Gestão de Pergunta de Anamnese no Sistema SIFIT

### Caso de Teste 01: Exclusão de Pergunta da Lista

| ID | Descrição |
| --- | --- |
| **C44-CT01** | Validar a exibição do modal de confirmação de exclusão e a remoção definitiva de uma pergunta da listagem do sistema. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e posicionado na tela **Perguntas Anamnese** com registros cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a lista de perguntas de anamnese<br> |
| **QUANDO** clica no ícone de exclusão (lixeira) de uma pergunta (ex.: "Qual é o exercício?") |
| **E** visualiza o modal de confirmação "Deseja deletar esta pergunta?" e clica em **"Confirmar"**<br><br> |
| **ENTÃO** o registro deve ser removido da listagem e a contagem de perguntas atualizada na interface. |

| **Critérios de Aceitação** |
| --- |
| * A pergunta selecionada deve ser excluída permanentemente e deixar de ser exibida na tabela após a confirmação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/131widQ4Ml1kO-jQLVhkbOs4qOyy1blw3/view?usp=sharing |

---

### Caso de Teste 02: Validação de Erro ao Tentar Editar Pergunta Existente

| ID | Descrição |
| --- | --- |
| **C44-CT02** | Validar o comportamento do sistema ao tentar alterar o tipo de resposta de uma pergunta cadastrada, exibindo a mensagem de erro correspondente. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de gerenciamento de **Perguntas Anamnese** com registros existentes. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição de uma pergunta na tabela (ex.: código 4) <br> |
| **QUANDO** altera o "Tipo Resposta" (ex.: de "Sim e Não" para "Sim, Não e Não Sei") e clica em **"Salvar"**<br><br> |
| **ENTÃO** o sistema exibe o indicador de salvamento e apresenta um modal com a mensagem de erro **"Erro ao salvar pergunta"**. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve bloquear alterações não permitidas no tipo de resposta, exibindo um pop-up de alerta de erro para o operador. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1YFPpJy7qa9TTkabG3R07Z8GTdehrgKVb/view?usp=sharing |

---

### Caso de Teste 03: Cadastro de Nova Pergunta de Anamnese

| ID | Descrição |
| --- | --- |
| **C44-CT03** | Validar o fluxo de cadastro de uma nova pergunta de anamnese preenchendo o código, nome, texto da pergunta e selecionando o tipo de resposta.|

| **Pré-condições** |
| --- |
| O usuário estar posicionado na tela principal de **Perguntas Anamnese**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"Nova Pergunta"** no canto superior direito<br> |
| **QUANDO** preenche os campos de código, nome, texto da pergunta e define o tipo de resposta (ex.: "Sim e Não") |
| **E** clica no botão **"Salvar"**<br><br> |
| **ENTÃO** a nova pergunta deve ser gravada com sucesso e adicionada à listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * O novo registro deve ser persistido corretamente e refletir os dados informados nos cards de resumo e na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1QpyYGvuLut-t7-kfwXJkrM31yfr3NldF/view?usp=sharing |

---

### Caso de Teste 04: Validação de Campos Obrigatórios no Cadastro de Pergunta

| ID | Descrição |
| --- | --- |
| **C44-CT04** | O sistema deve validar o preenchimento obrigatório dos campos ao tentar salvar uma nova pergunta com dados incompletos. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Perguntas Anamnese** com o modal de nova pergunta aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário abre o modal **"Nova Pergunta"**<br><br>|
| **QUANDO** tenta prosseguir e clicar em **"Salvar"** sem preencher os campos obrigatórios (como Nome ou o enunciado da Pergunta)<br> |
| **ENTÃO** o sistema deve impedir o registro e sinalizar visualmente as pendências de preenchimento obrigatório, mas cadastra mesmo assim.|


| **Critérios de Aceitação** |
| --- |
| * O salvamento deve ser bloqueado caso os campos essenciais não estejam devidamente preenchidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ULFkiN2npCTMc3TF9CY7l_JA7ZvzFiUY/view?usp=sharing |

---

### Caso de Teste 05: Filtragem de Perguntas por Código, Nome e Status

| ID | Descrição |
| --- | --- |
| **C44-CT05** | Validar a filtragem de perguntas na listagem principal utilizando os campos de busca por código, nome e filtros de status (Ativo/Inativo). |

| **Pré-condições** |
| --- |
| O usuário estar na página principal de **Perguntas Anamnese** com múltiplos registros cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a barra de filtros no topo da tela<br> |
| **QUANDO** preenche o campo "Código" ou "Nome da pergunta" e altera o filtro de "Status" (ex.: Ativo, Inativo ou Todos) |
| **E** clica no botão **"Buscar"**<br><br> |
| **ENTÃO** a tabela deve ser atualizada dinamicamente para exibir apenas os registros que correspondem rigorosamente aos critérios de busca. |

| **Critérios de Aceitação** |
| --- |
| * Os filtros devem retornar os resultados com precisão e atualizar o contador de registros exibidos na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wVl2TUPuf7LYtu_L4KHSkWi5GsJNXRly/view?usp=sharing |
