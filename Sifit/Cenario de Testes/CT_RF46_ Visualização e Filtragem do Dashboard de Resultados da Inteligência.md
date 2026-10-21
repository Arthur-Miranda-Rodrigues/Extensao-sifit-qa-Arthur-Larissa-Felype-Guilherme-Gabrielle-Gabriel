

---

## Cenário de teste: Visualização e Filtragem do Dashboard de Resultados da Inteligência

### Caso de Teste 01: Filtragem do dashboard por período temporal

| ID | Descrição |
| --- | --- |
| C07-CT01 | O sistema deve atualizar os indicadores, gráficos e listas do dashboard conforme o período temporal selecionado pelo usuário. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela "Resultados da Inteligência". |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Resultados da Inteligência" |
| **QUANDO** alternar entre os filtros de período: "Hoje", "Últimos 7 dias", "Últimos 30 dias" e "Últimos 90 dias" |
| **ENTÃO** os dados dos cards superiores (Automações executadas, Relatórios enviados, Alunos em risco, Aniversariantes, etc.) e o histórico do que o SIFIT identificou devem recarregar atualizando as informações correspondentes ao período selecionado |

| **Critérios de aceitação** |
| --- |
| As requisições de carregamento devem ser disparadas ao clicar em cada filtro e os valores dos cards devem ser atualizados dinamicamente sem erros na tela. |

https://jam.dev/c/58cc6143-8d39-4efa-8379-bfccf7e6a77d

---

### Caso de Teste 02: Alternância de tema da interface (Modo Claro / Modo Escuro)

| ID | Descrição |
| --- | --- |
| C07-CT02 | O sistema deve permitir a alteração do tema visual da aplicação entre o modo Claro e Escuro através do alternador no topo da página. |

| **Pré-condições** |
| --- |
| O usuário deve estar na página "Resultados da Inteligência". |

| **Passos** |
| --- |
| **DADO** que a interface está exibindo o tema Claro |
| **QUANDO** o usuário clicar na opção "Escuro" localizada no cabeçalho superior direito |
| **ENTÃO** as cores de fundo, cards, sidebar e fontes do sistema devem alternar instantaneamente para o tema escuro |
| **E** ao clicar em "Claro", a interface deve retornar ao tema original claro |

| **Critérios de aceitação** |
| --- |
| O contraste dos elementos e texto deve ser preservado de forma legível em ambos os modos. |

---

### Caso de Teste 03: Exibição dos cards de inteligência e alertas do SIFIT

| ID | Descrição |
| --- | --- |
| C07-CT03 | O painel deve exibir o resumo das identificações do sistema (Atenção para risco de evasão e Financeiro para inadimplência). |

| **Pré-condições** |
| --- |
| Existirem registros de alunos monitorados com risco de evasão ou inadimplência cadastrados no banco de dados. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o dashboard "Resultados da Inteligência" |
| **QUANDO** visualizar a seção "Inteligência Sifit" no lado direito |
| **ENTÃO** o card de "Atenção" deve exibir a contagem atual de alunos com risco de evasão |
| **E** o card "Financeiro" deve exibir a quantidade exata de alunos inadimplentes sendo monitorados |

| **Critérios de aceitação** |
| --- |
| Os números apresentados no painel de alertas laterais devem corresponder aos totais contabilizados pelo backend para o período selecionado. |
