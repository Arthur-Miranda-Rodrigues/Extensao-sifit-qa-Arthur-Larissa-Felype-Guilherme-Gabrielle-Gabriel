
---

# Cenário 9: Consulta e Filtragem de Presenças de Clientes

### Caso de Teste 01: Consulta de Presenças por Nome do Cliente

| ID | Descrição |
| --- | --- |
| **CT09-01** | Validar a busca de registros de presença informando o nome ou parte do nome do cliente no campo "Buscar por cliente..." (ex.: pesquisando por "gabrielli bononi" ou "albetro"), conferindo a atualização dos cards de resumo e o feedback da listagem.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SiFit e posicionado na tela de **Presenças** (`/presencas`).

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Presenças**<br> |
| **QUANDO** preencher o campo "Buscar por cliente..." com o nome do cliente (ex.: "gabrielli bononi")

 |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** o sistema deve processar a consulta, recalcular os cards superiores (*Total no período*, *Alunos devedores*, *Visita por dia*, *Dias no período*) e exibir os registros correspondentes ou a mensagem *"Nenhuma presença encontrada"* caso não haja ocorrências.

 |

| **Critérios de Aceitação** |
| --- |
| O sistema deve filtrar com precisão os dados com base no nome inserido, atualizando as métricas dos cards em tempo real.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Uu6ROP9y54yUFcz2bRM8_z4nziK6pusO/view?usp=sharing |

---

### Caso de Teste 02: Consulta de Presenças por Número / Código do Cliente

| ID | Descrição |
| --- | --- |
| **CT09-02** | Validar a busca de registros de presença informando o número ou código identificador do aluno no campo de pesquisa.

 |

| **Pré-condições** |
| --- |
| O usuário está posicionado na tela de consulta de presenças/check-ins.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de controle de presenças

 |
| **QUANDO** inserir o número ou código do cliente no campo de busca (ex.: "397" ou "404")

 |
| **E** acionar a consulta/busca

 |
| **ENTÃO** o sistema deve filtrar e exibir estritamente o registro vinculado ao número/código informado.

 |

| **Critérios de Aceitação** |
| --- |
| A busca por número/código deve localizar e retornar o registro de atendimento do aluno de forma direta.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1UYkbT4XRAO_L7E2_FxQvkw7uI2O8wxxC/view?usp=sharing |

---

### Caso de Teste 03: Filtragem Através dos Três Filtros de Período Rápido ("Hoje", "Esta semana", "Este mês")

| ID | Descrição |
| --- | --- |
| **CT09-03** | Validar o preenchimento automático das datas e a atualização imediata das métricas ao acionar os três botões de filtro rápido de período disponíveis (*"Hoje"*, *"Esta semana"* e *"Este mês"*).

 |

| **Pré-condições** |
| --- |
| O usuário está posicionado na tela de **Presenças**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de consulta de presenças

 |
| **QUANDO** clicar sucessivamente nos três botões de filtro rápido no topo (*"Hoje"*, *"Esta semana"* e *"Este mês"*)

 |
| **ENTÃO** o sistema deve ajustar automaticamente e de forma instantânea os campos de data "DE" e "ATÉ" para abranger o intervalo de cada filtro selecionado

 |
| **E** recalcular os indicadores dos cartões e os registros de presença em tela para cada opção acionada.

 |

| **Critérios de Aceitação** |
| --- |
| Os três filtros rápidos devem atualizar corretamente os intervalos de data e recalcular os dados exibidos sem falhas.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1rQKVQBzjg3Ts6JQrwtPB_IrQQC5CLTNm/view?usp=sharing |

---

### Caso de Teste 04: Busca e Filtragem por Data Customizada (Período e Calendário)

| ID | Descrição |
| --- | --- |
| **CT09-04** | Validar a seleção manual de datas customizadas nos campos "DE" e "ATÉ", incluindo a navegação pelos meses através do componente de calendário (ex.: alternando entre setembro, agosto e outubro) e a aplicação da busca.

 |

| **Pré-condições** |
| --- |
| O usuário está posicionado na tela de **Presenças**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Presenças**<br> |
| **QUANDO** clicar nos seletores de data "DE" ou "ATÉ"

 |
| **E** navegar pelo calendário alterando os meses e selecionando os dias desejados

 |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** o sistema deve atualizar o intervalo de datas da pesquisa e recalcular os cards de resumo e a listagem de presenças conforme o período customizado estipulado.

 |

| **Critérios de Aceitação** |
| --- |
| O sistema deve permitir a navegação livre pelo calendário e o filtro por datas customizadas, atualizando todas as métricas correspondentes ao intervalo definido.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1xrH39mQ1RuoC74RyNNOZsOCvgz8Yeg4o/view?usp=sharing |
