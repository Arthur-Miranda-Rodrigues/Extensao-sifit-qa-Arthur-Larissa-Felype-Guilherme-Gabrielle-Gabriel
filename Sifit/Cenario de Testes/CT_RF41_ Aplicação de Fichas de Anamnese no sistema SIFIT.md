## Cenário 41: Aplicação de Fichas de Anamnese no sistema SIFIT

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
