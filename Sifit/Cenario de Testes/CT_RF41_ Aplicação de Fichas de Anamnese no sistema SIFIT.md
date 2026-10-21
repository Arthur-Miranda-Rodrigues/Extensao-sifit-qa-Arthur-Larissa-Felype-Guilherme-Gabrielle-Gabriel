## Cenário 41: Aplicação de Fichas de Anamnese no sistema SIFIT

### Caso de Teste 01: Buscar Aluno e Selecionar Modelo de Anamnese

| ID | Descrição |
| --- | --- |
| **C41-CT01** | Validar a busca por um aluno no modal de aplicação, o tratamento de registros não encontrados e a seleção subsequente de um modelo de anamnese. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela **Fichas de Anamnese** do sistema SiFit. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"Nova Anamnese"** no canto superior direito<br> |
| **QUANDO** digita o nome de um aluno e clica no ícone de busca |
| **ENTÃO** o sistema exibe o resultado ou a mensagem de que nenhum aluno foi encontrado caso não localize. |
| **DADO** que o usuário localiza e seleciona o aluno correto avançando para a etapa seguinte<br> |
| **QUANDO** escolhe um modelo de anamnese disponível na lista e clica em **"Iniciar"**<br><br> |
| **ENTÃO** o sistema direciona para a etapa de preenchimento das perguntas da ficha de anamnese. |
| **E** o ao clicar em **Finalizar Anamnese** nada acontece  e na listagem permanece a mensagem **Nenhuma ficha encontrada** |

| **Critérios de Aceitação** |
| --- |
| * A busca deve filtrar corretamente os cadastros de alunos. |
| * O modelo de anamnese selecionado deve abrir com sucesso para o preenchimento das perguntas estruturadas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1V7sDdPIEofzjCAJTtkYiNBRupi0qRDVc/view?usp=sharing |

---

### Caso de Teste 02: Preenchimento, Tentativa de Finalização com Erro no Servidor e Salvamento de Rascunho

| ID | Descrição |
| --- | --- |
| **C41-CT02** | Validar o fluxo de revisão e finalização da anamnese, o tratamento de exceção em caso de erro no servidor e a funcionalidade de salvar rascunho. |

| **Pré-condições** |
| --- |
| O usuário estar na etapa de revisão e finalização de uma ficha de anamnese aberta para um aluno. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a tela **"Revisar e Finalizar"** com as respostas inseridas<br> |
| **QUANDO** clica no botão **"Finalizar Anamnese"** e o sistema simula uma falha de conexão/servidor exibindo o pop-up **"Erro no servidor"**<br> |
| **E** fecha a mensagem de erro clicando em "Fechar" |
| **QUANDO** aciona o botão **"Salvar rascunho"** para preservar os dados preenchidos sem concluir formalmente a ficha<br> |
| **ENTÃO** o sistema processa a solicitação de rascunho temporariamente e retorna ao estado padrão de salvamento. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve tratar falhas de servidor exibindo mensagens claras de erro por meio de pop-up. |
| * A opção de salvar rascunho deve permitir gravar o andamento do preenchimento quando houver interrupções no envio. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1TxdKmCaGbufBF7FS42Sx4AtkSjMvqGQ0/view?usp=sharing |

---

### Caso de Teste 03: Filtragem de Fichas de Anamnese por Status na Tela Principal

| ID | Descrição |
| --- | --- |
| **C41-CT03** | O sistema deve permitir a filtragem e consulta de fichas de anamnese cadastradas através do seletor de status e barra de pesquisa na tela principal.|

| **Pré-condições** |
| --- |
| O usuário estar posicionado na página principal de **Fichas de Anamnese**. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza os cards de indicadores (Total de fichas, Concluídas, Pendentes, Clientes avaliados)<br> |
| **QUANDO** utiliza a barra de pesquisa por nome de aluno e o filtro de status (alternando entre "Todos os status", "Concluído" ou "Pendente")<br> |
| **ENTÃO** a tabela ou o painel central deve atualizar os registros exibidos de acordo com o filtro selecionado. |
| **E** pela ausência de conteúdo, na listagem permanece a mensagem **Nenhuma ficha encontrada** |

| **Critérios de Aceitação** |
| --- |
| * Os filtros de status devem atualizar dinamicamente a exibição das fichas e refletir a listagem correta correspondente aos critérios aplicados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11LuK3RJrX1qypahSx4SAlgFt0T-2FSlE/view?usp=sharing |
