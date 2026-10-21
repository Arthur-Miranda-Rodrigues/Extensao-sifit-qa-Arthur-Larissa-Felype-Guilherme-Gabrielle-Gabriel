## Cenário 2: Página Inicial (Parte 1)
### Caso de Teste 01: Consulta e Filtro no Modal "Clientes Sem Matrículas"

| ID | Descrição |
| --- | --- |
| **C02-CT01** | Validar a abertura e a busca por nome de alunos no modal de "Clientes Sem Matrículas" a partir da Página Inicial.


| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e posicionado na **Página Inicial**.


| **Passos** |
| --- |
| **DADO** que o usuário está na **Página Inicial**<br> |
| **QUANDO** clicar no link ou card de atalho **Clientes Sem Matrículas** (ou "Ver detalhes").|
| **ENTÃO** o sistema deve abrir o modal *"Clientes Sem Matrículas"* listando os alunos que não possuem matrícula ativa.|
| **E** ao digitar um nome no campo "Buscar por nome ou código..." (ex.: "guilher").|
| **ENTÃO** o sistema deve filtrar os registros e exibir a mensagem de feedback caso nenhum cliente seja localizado.|

| **Critérios de Aceitação** |
| --- |
| * O modal deve exibir resumos operacionais e listagem com colunas: Código, Nome, Dias sem Visita, Última Visita e Ações.
| * A busca deve atualizar a lista de alunos em tempo real ou mediante confirmação.|

 
 | **Evidência** |
| --- |
|  https://drive.google.com/file/d/1i4IfNOHijkgTu4uBFYjmlrA1_sEOwfZz/view?usp=sharing  |


---

### Caso de Teste 02: Visualização e Filtragem no Modal "Clientes Ausentes"

| ID | Descrição |
| --- | --- |
| **C02-CT02** | Validar a consulta detalhada de alunos sumidos ou ausentes há mais tempo na academia.

| **Pré-condições** |
| --- |
| Usuário autenticado e posicionado no dashboard inicial.

| **Passos** |
| --- |
| **DADO** que o usuário observa os cards da **Página Inicial**<br> |
| **QUANDO** clicar no card **Clientes Ausentes**<br> |
| **ENTÃO** o sistema deve exibir o modal *"Clientes Ausentes"* com indicadores de métricas e lista de alunos|
| **E** permitir a filtragem por nome ou código do aluno no campo de busca interno.|

| **Critérios de Aceitação** |
| --- |
| * O modal deve apresentar contadores de ausência e atalhos para ações de recuperação/contato via WhatsApp.|

 
 | **Evidência** |
| --- |
|   https://drive.google.com/file/d/1bJuvOZ-WPyPUthbEcGnsdja2B_zy7vfq/view?usp=sharing |


---

### Caso de Teste 03: Redirecionamento e Filtro no Card "Avaliações"

| ID | Descrição |
| --- | --- |
| **C02-CT03** | Validar o redirecionamento direto da Página Inicial para a tela de gestão de Avaliações físicas.

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit.|

| **Passos** |
| --- |
| **DADO** que o usuário está na **Página Inicial**<br> |
| **QUANDO** clicar na opção **Ver detalhes** do card **0 Avaliações** (ou Avaliações Pendentes). |
| **ENTÃO** o sistema deve navegar diretamente para o menu **Operação da Academia > Avaliações**<br> |
| **E** carregar a listagem de avaliações físicas com o filtro padrão (ex.: status *Pendente*). |

| **Critérios de Aceitação** |
| --- |
| * O redirecionamento deve ocorrer sem erros e mantendo os parâmetros de filtro correspondentes ao card acionado.|

 
  | **Evidência** |
| --- |
| https://drive.google.com/file/d/1iid5UaySagOawaHuNqJAWYu4i9AEGiZ0/view?usp=sharing |


---

### Caso de Teste 04: Detalhamento do Modal "Financeiro em Aberto" e Filtros de Vencimento

| ID | Descrição |
| --- | --- |
| **C02-CT04** | Validar a exibição do modal de mensalidades pendentes e a alternância de atalhos por período de atraso.

| **Pré-condições** |
| --- |
| Usuário autenticado na Página Inicial.

| **Passos** |
| --- |
| **DADO** que o usuário está na **Página Inicial**<br> |
| **QUANDO** clicar no link **Ver detalhes** do card de valores em aberto (ex.: "R$ 0,00 em aberto") |
| **ENTÃO** o sistema deve abrir a janela modal *"Financeiro em Aberto"*<br> |
| **E** permitir a alternância entre os filtros rápidos: **Todos**, **Vence hoje**, **Até 7 dias**, **8 a 15 dias**, **15 a 30 dias** e **+30 dias**.|

| **Critérios de Aceitação** |
| --- |
| * Os cards financeiros superiores do modal (*Valor total em aberto*, *Horas para cobrança*, *Alunos*, *Cobrar todos no WhatsApp*, etc.) devem atualizar conforme o filtro de vencimento selecionado.|

 | **Evidência** |
| --- |
|  https://drive.google.com/file/d/1xR2uFV7fjqiEjpHFMpbfZA9k6816h5w_/view?usp=sharing |


---

### Caso de Teste 05: Consulta ao "Radar de Evasão" e Explicação da Regra de Cálculo

| ID | Descrição |
| --- | --- |
| **C02-CT05** | Validar a abertura do Radar de Evasão e a visualização das regras de pontuação/risco de cancelamento do aluno.

| **Pré-condições** |
| --- |
| Usuário autenticado no dashboard inicial.

| **Passos** |
| --- |
| **DADO** que o usuário está na **Página Inicial**<br> |
| **QUANDO** clicar na opção **Ver detalhes** do card **Alunos em risco de evasão**<br> |
| **ENTÃO** o sistema deve abrir o modal *"Radar de Evasão"* com as classificações de risco (*Em risco alto*, *Em risco médio*, *Sem treinar há 15+ dias*,  *Mensalidades atrasadas*)|
| **E** ao clicar no botão **Saiba mais sobre o cálculo**<br> |
| **ENTÃO** o sistema deve exibir um sub-modal explicativo detalhando os critérios de pontuação (ex.: percentuais de risco, assiduidade e situação financeira).|

| **Critérios de Aceitação** |
| --- |
| * O modal deve disponibilizar o botão **Exportar relatório** para extração das informações de evasão.|
| * As explicações das regras de cálculo devem ser apresentadas com clareza em tela.|

 
 | **Evidência** |
| --- |
| https://drive.google.com/file/d/1CtFW2LN8H2tDjZ21SBi7slmTf3wHspEZ/view?usp=sharing  |


