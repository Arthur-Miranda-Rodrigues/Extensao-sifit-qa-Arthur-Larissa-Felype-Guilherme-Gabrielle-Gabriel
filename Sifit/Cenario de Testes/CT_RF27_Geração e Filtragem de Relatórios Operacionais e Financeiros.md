
---

# Cenário 27: Geração e Filtragem de Relatórios Operacionais e Financeiros

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo de **Relatórios** do sistema **SiFit**. O objetivo é validar a emissão de relatórios operacionais e financeiros (Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar e Caixas), testando a aplicação de filtros por período, tipos de planos, status de pagamento, formas de pagamento, bem como a alteração entre formatos normais e detalhados.

---

## 2. Cenários de Teste

### Caso de Teste 01: Visualização do Painel Geral de Relatórios e Navegação de Tipos

| ID | Descrição |
| --- | --- |
| **C27-CT01** | O sistema deve exibir o painel central de relatórios com as opções de modelos disponíveis para seleção. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SiFit e localizado na tela de **Relatórios**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a aba "Relatórios" no menu lateral |
| **QUANDO** visualizar o painel de tipos de relatórios disponíveis na interface (Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar, Caixas) |
| **ENTÃO** todas as opções de relatórios operacionais e financeiros devem ser listadas corretamente com suas descrições. |

| **Critérios de Aceitação** |
| --- |
| * A interface deve carregar todos os modelos de relatórios suportados pelo sistema de forma integrada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1NOMrAbcpq4-im9KCfWKY2piSgL4wwAPF/view?usp=sharing |

---

### Caso de Teste 02: Geração de Relatório de Avaliações Físicas por Período

| ID | Descrição |
| --- | --- |
| **C27-CT02** | O sistema deve permitir a emissão do relatório de "Avaliações" filtrando por um intervalo de datas específico. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de relatórios com o tipo "Avaliações" selecionado. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o tipo de relatório "Avaliações" |
| **QUANDO** define o intervalo de datas (Data Início e Data Fim) |
| **E** clica no botão **Gerar Relatório**<br> |
| **ENTÃO** o sistema processa e dispara o download do arquivo em formato PDF contendo o histórico de avaliações físicas do período. |

| **Critérios de Aceitação** |
| --- |
| * O arquivo PDF correspondente deve ser gerado e baixado com sucesso no navegador. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tGFLLMJroyh8HwPWT0cGnz_c7oENd4vR/view?usp=sharing |

---

### Caso de Teste 03: Geração de Relatório de Cadastro de Clientes

| ID | Descrição |
| --- | --- |
| **C27-CT03** | O sistema deve permitir a emissão do relatório de "Clientes" com base no período selecionado. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de relatórios do SiFit. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona a opção "Clientes" no campo de tipo de relatório |
| **QUANDO** define as datas inicial e final para a busca de cadastros |
| **E** clica no botão **Gerar Relatório**<br> |
| **ENTÃO** o relatório consolidado de cadastro de alunos/clientes deve ser gerado e disponibilizado para exportação. |

| **Critérios de Aceitação** |
| --- |
| * O relatório de clientes deve ser baixado corretamente em PDF. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1SOkU7etE4zIFMC0it-p2THJU_H6cHmFf/view?usp=sharing |

---

### Caso de Teste 04: Geração de Relatório de Colaboradores (Dados e Acessos Internos)

| ID | Descrição |
| --- | --- |
| **C27-CT04** | O sistema deve permitir a emissão de relatórios referentes aos colaboradores da academia por período. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de relatórios do SiFit. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o tipo de relatório "Colaboradores" |
| **QUANDO** define o período desejado nos campos de data |
| **E** clica no botão **Gerar Relatório**<br> |
| **ENTÃO** o sistema gera e exporta o documento PDF com as informações cadastrais e dados de colaboradores. |

| **Critérios de Aceitação** |
| --- |
| * O relatório de colaboradores deve ser gerado de acordo com o intervalo informado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1HKX9pCbifSQM9mopakfKo18eBeZeYNc_/view?usp=sharing |

---

### Caso de Teste 05: Geração de Relatório de Matrículas com Filtro por Tipo de Plano

| ID | Descrição |
| --- | --- |
| **C27-CT05** | O sistema deve permitir a emissão do relatório de "Matrículas" aplicando filtros por planos específicos e período. |

| **Pré-condições** |
| --- |
| Existirem planos e matrículas cadastradas no sistema.|

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o tipo de relatório "Matrículas" |
| **QUANDO** seleciona um "Tipo de Plano" específico no filtro (ex.: planos de meses, trimestrais ou anuais) e define as datas |
| **E** clica no botão **Gerar Relatório**<br> |
| **ENTÃO** o relatório PDF de matrículas deve ser gerado contemplando apenas os registros do plano selecionado. |

| **Critérios de Aceitação** |
| --- |
| * O filtro por tipo de plano deve ser respeitado na exportação do relatório. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1E_5EW0lVq61giTiEM05tlN2EJQ5TmeBo/view?usp=sharing |

---

### Caso de Teste 06: Geração de Relatório de Contas a Receber com Opção Detalhada

| ID | Descrição |
| --- | --- |
| **C27-CT06** | O sistema deve permitir a emissão do relatório de "Contas a Receber" com filtros avançados de status, forma de pagamento e formato detalhado. |

| **Pré-condições** |
| --- |
| Existirem registros de contas a receber no módulo financeiro. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o tipo de relatório "Contas a Receber" |
| **QUANDO** configura os filtros de forma de pagamento (ex.: Cartão de Crédito, Dinheiro, Pix), status (ex.: Pendente/Recebido) e marca a opção **Detalhado**<br> |
| **E** define o período e clica em **Gerar Relatório**<br> |
| **ENTÃO** o relatório detalhado de recebimentos deve ser gerado contendo o resumo geral e os lançamentos individualizados. |

| **Critérios de Aceitação** |
| --- |
| * O relatório financeiro de recebimentos deve detalhar corretamente os valores líquidos, brutos e datas de vencimento conforme os filtros. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1e7spLntaV23bau5gg1dQzCA6dFUfA3Nm/view?usp=sharing |

---

### Caso de Teste 07: Geração de Relatório de Contas a Pagar (Despesas e Pagamentos)

| ID | Descrição |
| --- | --- |
| **C27-CT07** | O sistema deve permitir a emissão do relatório de "Contas a Pagar" filtrando por período de vencimento ou pagamento. |

| **Pré-condições** |
| --- |
| Existirem registros de contas a pagar cadastradas no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona o tipo de relatório "Contas a Pagar" |
| **QUANDO** define o intervalo de datas desejado |
| **E** clica no botão **Gerar Relatório**<br> |
| **ENTÃO** o documento PDF de contas a pagar (pagas/a vencer) deve ser gerado e exportado com os totalizadores calculados. |

| **Critérios de Aceitação** |
| --- |
| * O relatório de contas a pagar deve apresentar os valores totais consolidados do período selecionado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1WAMJ74KEPWEgVlnvZ6dkDz6tUAcvcZTk/view?usp=sharing |

---

### Caso de Teste 08: Geração de Relatório de Caixas (Movimento de Caixa Normal vs. Detalhado)

| ID | Descrição |
| --- | --- |
| **C27-CT08** | O sistema deve permitir a emissão do relatório de "Caixas" alternando o formato de visualização entre "Normal" e "Detalhado". |

| **Pré-condições** |
| --- |
| O usuário estar na aba de relatórios com o tipo "Caixas" selecionado. |

| **Passos** |
| --- |
| **DADO** que o usuário escolhe o tipo de relatório "Caixas" |
| **QUANDO** define o campo **Formato** como "Detalhado" |
| **E** seleciona o período de fechamento de caixa e clica em **Gerar Relatório**<br> |
| **ENTÃO** o relatório de fechamento de caixa deve ser gerado em PDF apresentando os saldos iniciais, finais e as entradas detalhadas correspondentes. |

| **Critérios de Aceitação** |
| --- |
| * A alternância para o formato detalhado deve incluir a listagem analítica das entradas e recebíveis no relatório exportado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1He9ietmya6B1Cru_Z6HvZ1nOmRDc1HZ-/view?usp=sharing |
