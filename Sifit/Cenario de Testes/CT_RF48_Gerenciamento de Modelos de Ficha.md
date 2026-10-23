## Cenário 48: Gerenciamento de Modelos de Ficha

### Caso de Teste 01: Criação de novo modelo de ficha e tratamento de erro na gravação

| ID | Descrição |
| --- | --- |
| **C48-CT01** | Validar o comportamento do sistema ao preencher o formulário de cadastro de um novo modelo de ficha e submeter a gravação. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SiFit e posicionado no menu **Modelos de Ficha**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Modelos de Ficha** e clica no botão de adicionar um novo modelo **(+)**. <br>|
| **QUANDO** preencher o campo "Nome do Modelo" (ex.: "Hipertorfia") e selecionar um personal no campo correspondente (ex.: "Gabriella").<br> |
| **E** clicar no botão **Criar Modelo**.<br> |
| **ENTÃO** o sistema deve processar a requisição e, em caso de falha de comunicação com o servidor, exibir um modal de alerta com a mensagem *"Erro ao salvar modelo"*. |

| **Critérios de Aceitação** |
| --- |
| O modal de erro deve ser apresentado claramente com a opção de fechar, permitindo retornar à tela de listagem de modelos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1oDvPksSC7n5nHmVQXFQ5rCnqqPbTm7zS/view?usp=sharing |

---

### Caso de Teste 02: Filtragem e Pesquisa de Modelos de Ficha por Parâmetros

| ID | Descrição |
| --- | --- |
| **C48-CT02** | Validar a busca e filtragem de registros na listagem de modelos de ficha utilizando os campos de código, título e criador. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de gerenciamento de **Modelos de Ficha**. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a listagem de modelos de ficha.<br> |
| **QUANDO** preencher os campos de filtro de pesquisa (como *Código*, *Título do modelo* ou *Nome do criador*).<br> |
| **E** acionar o botão de busca (ícone de lupa).<br> |
| **ENTÃO** o sistema deve consultar a base de dados e atualizar os resultados na tabela ou exibir a mensagem de estado vazio *"Nenhum modelo de ficha encontrado"*.|

| **Critérios de Aceitação** |
| --- |
| Os campos de filtro devem processar as consultas informadas e atualizar a interface de acordo com os critérios definidos.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/191k97YZRlvUkOogX6qtUE1B2dytOaP0Y/view?usp=sharing |
