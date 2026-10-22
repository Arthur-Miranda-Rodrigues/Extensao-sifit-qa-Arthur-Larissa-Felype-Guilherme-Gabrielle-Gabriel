## Cenário 46: Visualização e Filtragem do Dashboard de Resultados da Inteligência

### Caso de Teste 01: Filtragem do dashboard por período temporal

| ID | Descrição |
| --- | --- |
| **C46-CT01** | O sistema deve atualizar os indicadores, gráficos e listas do dashboard conforme o período temporal selecionado pelo usuário.|

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela "Resultados da Inteligência".|

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Resultados da Inteligência"<br>|
| **QUANDO** alternar entre os filtros de período: "Hoje", "Últimos 7 dias", "Últimos 30 dias" e "Últimos 90 dias"<br>|
| **ENTÃO** os dados dos cards superiores (Automações executadas, Relatórios enviados, Alunos em risco, Aniversariantes, etc.) e o histórico do que o SIFIT identificou devem recarregar atualizando as informações correspondentes ao período selecionado. |

| **Critérios de aceitação** |
| --- |
| As requisições de carregamento devem ser disparadas ao clicar em cada filtro e os valores dos cards devem ser atualizados dinamicamente sem erros na tela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nl9Q8FyjpiQedTegKhipW6YXfutt1Pmm/view?usp=sharing |
