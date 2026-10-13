
---

## Cenário de teste: Geração e Filtragem de Relatórios Operacionais e Financeiros

### Caso de Teste 01: Gerar relatório operacional com filtro por período

| ID | Descrição |
| --- | --- |
| C09-CT01 | O sistema deve permitir a emissão de relatórios operacionais (Avaliações, Clientes e Colaboradores) com base em um intervalo de datas definido. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela "Relatórios". |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a aba "Relatórios"

 |
| **E** escolhe um tipo de relatório operacional no painel à direita (ex.: "Avaliações", "Clientes" ou "Colaboradores")

 |
| **E** preenche o campo "Data Início" (ex.: "14/05/2026") e "Data Fim" (ex.: "30/09/2026")

 |
| **QUANDO** clicar no botão "Gerar Relatório"

 |
| **ENTÃO** o sistema deve processar o relatório e iniciar o download do arquivo no formato configurado (ex.: PDF)

 |

| **Critérios de aceitação** |
| --- |
| O arquivo PDF deve ser baixado com sucesso contendo as informações correspondentes ao período especificado. |

---

### Caso de Teste 02: Gerar relatório financeiro com filtros avançados (Contas a Receber, Pagar e Matrículas)

| ID | Descrição |
| --- | --- |
| C09-CT02 | O sistema deve permitir a aplicação de filtros específicos (status, planos, detalhamento) para emissão de relatórios financeiros e contratuais. |

| **Pré-condições** |
| --- |
| Devem existir registros financeiros e de matrículas cadastrados no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário escolhe um tipo de relatório com parâmetros adicionais, como "Contas a Receber" ou "Matrículas"

 |
| **E** configura os filtros específicos (ex.: "Status: Pendente", checkbox "Detalhado" marcado para Contas a Receber, ou filtros de "Planos" em Matrículas)

 |
| **E** define o intervalo de datas inicial e final

 |
| **QUANDO** clicar no botão "Gerar Relatório"

 |
| **ENTÃO** o relatório em PDF deve ser gerado respeitando estritamente todos os filtros aplicados

 |

| **Critérios de aceitação** |
| --- |
| O contador de "Filtros ativos" no topo da página deve atualizar conforme os parâmetros selecionados antes da geração. |

---

### Caso de Teste 03: Gerar relatório de fluxo de caixas alternando o formato (Normal vs. Detalhado)

| ID | Descrição |
| --- | --- |
| C09-CT03 | O sistema deve permitir a alteração entre as opções do campo "Formato" ao emitir o relatório de Caixas. |

| **Pré-condições** |
| --- |
| O usuário deve estar na aba de "Caixas" na tela de Relatórios. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o modelo de relatório "Caixas"

 |
| **E** clica no dropdown "Formato" alternando a seleção entre "Normal" e "Detalhado"

 |
| **E** define as datas de início e fim do movimento

 |
| **QUANDO** clicar no botão "Gerar Relatório"

 |
| **ENTÃO** o documento exportado deve apresentar a estrutura correspondente ao formato escolhido

 |

| **Critérios de aceitação** |
| --- |
| O relatório no formato "Detalhado" deve exibir a discriminação individualizada de cada movimentação de caixa no período selecionado. |

https://jam.dev/c/448e633b-4073-4b50-a158-20ec1dcc75b5
