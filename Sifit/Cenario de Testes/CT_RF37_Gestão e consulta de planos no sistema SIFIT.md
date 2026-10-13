
---

## Cenário de teste: Gestão e consulta de planos no sistema SIFIT

### Caso de Teste 01: Consultar plano por código ou nome com sucesso

| ID | Descrição |
| --- | --- |
| C10-CT01 | O sistema deve filtrar e retornar o plano correto ao buscar pelo seu código ou pelo nome. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na página de **Planos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de "Planos" |
| **E** insere o código (ex: "38") ou o nome do plano (ex: "Baratão") nos campos de filtro |
| **QUANDO** clica no botão "Buscar" |
| **ENTÃO** a tabela de resultados deve listar apenas o registro correspondente ao filtro informado |

| **Critérios de aceitação** |
| --- |
| As informações exibidas na tabela (Código, Nome, Alunos, Valor, Duração e Status) devem ser condizentes com o plano pesquisado. |

---

### Caso de Teste 02: Cadastrar um novo plano com sucesso

| ID | Descrição |
| --- | --- |
| C10-CT02 | O sistema deve permitir o cadastro de um novo plano com período fixo, valores, grupo e equipe definidos. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na tela de **Planos**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "+ Novo Plano" |
| **E** preenche o Nome (ex: "Aba 10"), Grupo (ex: "Treino Personal") e Status ("Ativo") |
| **E** seleciona a Cobrança como "Período fixo", define Duração (ex: "12 Meses") e Parcelas ("1") |
| **E** informa o Valor Mensal (ex: "120,00") e Valor Matrícula (ex: "30,00") |
| **E** configura os parâmetros de Personal ("Sim"), Função ("Jaimes") e Molde de Dependentes ("5") |
| **QUANDO** clica no botão "Salvar Plano" |
| **ENTÃO** o modal é fechado e o novo plano é adicionado à listagem com status "ATIVO" |

| **Critérios de aceitação** |
| --- |
| O plano deve ser salvo com sucesso e refletir nos contadores e na listagem geral do sistema. |

---

### Caso de Teste 03: Editar dados e status de um plano cadastrado

| ID | Descrição |
| --- | --- |
| C10-CT03 | O sistema deve permitir a alteração das informações e do status (Ativo/Inativo) de um plano existente. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e possuir planos previamente cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o plano desejado na listagem |
| **E** clica no ícone de edição (lupa/lápis) do registro |
| **E** altera as configurações necessárias no modal (ex: Função do Professor ou alteração de Status para "Ativo") |
| **QUANDO** clica no botão "Salvar Plano" |
| **ENTÃO** as alterações devem ser gravadas e atualizadas na listagem imediatamente |

| **Critérios de aceitação** |
| --- |
| As informações modificadas devem ser persistidas e exibidas corretamente na tabela. |

---

### Caso de Teste 04: Tentar deletar plano vinculado e validar mensagem de erro

| ID | Descrição |
| --- | --- |
| C10-CT04 | O sistema deve impedir a exclusão de um plano que possua vínculos/restrições ativas e apresentar mensagem de erro apropriada. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na tela de **Planos**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão ("X") de um plano na tabela |
| **E** confirma a ação no modal com a pergunta "Deseja deletar o Plano?" clicando em "Confirmar" |
| **QUANDO** o sistema processa a solicitação de exclusão |
| **ENTÃO** deve ser exibida uma mensagem de alerta/modal informando "Erro ao deletar Plano" |

| **Critérios de aceitação** |
| --- |
| O plano não deve ser removido do banco de dados e a mensagem de erro deve ser exibida de forma visível para o usuário. |

https://jam.dev/c/ce82077d-9ab0-4cb7-917d-22cdd235d920
