## Cenário 47: Gerenciamento de Modelos de Ficha

### Caso de Teste 02: Filtragem e Pesquisa de Modelos de Ficha por Parâmetros

| ID | Descrição |
| --- | --- |
| **C47-CT02** | Validar a busca e filtragem de registros na listagem de modelos de ficha utilizando os campos de código, título e criador. |

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
