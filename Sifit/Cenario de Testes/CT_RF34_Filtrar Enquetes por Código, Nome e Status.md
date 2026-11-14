## Cenário 34: Módulo de Enquetes

### Caso de Teste 01: Filtrar enquetes por Código, Nome e Status

| ID | Descrição |
| --- | --- |
| **C34-CT01** | O sistema deve permitir a filtragem da lista de enquetes pelos campos Código, Nome e Status (Todos/Ativo/Inativo). |

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
