
---

## Cenário 7: Acesso e visualização do Dashboard.

### Caso de Teste 01: Navegação para a Tela de Dashboard e Alternância Dinâmica de Cores ao Recarregar
---
| ID | Descrição |
| --- | --- |
| **C07-CT01** | Verificar o direcionamento para a tela "Dashboard" pelo menu lateral, a correta renderização dos painéis e o comportamento de alternância/mudança de tema de cores ao recarregar a página. |

| **Pré-condições** |
| --- |
| Utilizador autenticado no sistema SIFIT. |

| **Passos** |
| --- |
| **DADO** que o utilizador está autenticado no SIFIT. |
| **QUANDO** clicar no item "Dashboard" do menu lateral principal. |
| **E** recarregar/atualizar a página do Dashboard (F5 / Refresh). |
| **ENTÃO** o sistema deve carregar a página de Dashboard (`/dashboard`), apresentando a alternância dinâmica na paleta de cores/tema dos gráficos e painéis a cada recarregamento, além de exibir o bloco de "Inteligência Sifit" e as métricas principais. |

| **Critérios de aceitação** |
| --- |
| O Dashboard deve ser carregado com sucesso pelo menu lateral e adaptar/alterar o tema de cores dos gráficos e componentes ao reiniciar/recarregar a página. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wB_CdpNSVpde0k2M5K2rhg7mAnFdX5_7/view?usp=sharing |



---

### Caso de Teste 02: Interação com Gráficos Interativos e Exibição de Tooltips (Hover)

| ID | Descrição |
| --- | --- |
| **C07-CT02** | Validar a interatividade dos gráficos do Dashboard ao posicionar o cursor sobre as barras e seções, conferindo a exibição das etiquetas informativas (*tooltips*). |

| **Pré-condições** |
| --- |
| Utilizador posicionado na tela de Dashboard. |

| **Passos** |
| --- |
| **DADO** que o utilizador está visualizando a tela de Dashboard. |
| **QUANDO** rolar a página e passar o cursor (*hover*) sobre as barras e seções dos diferentes gráficos (ex.: faixa etária *18 a 25*, gráfico de pizza *Masculino*, barras mensais de *Janeiro*, *Junho*, *Julho*, *Outubro*, *Novembro* e gráfico de distribuição por personal). |
| **ENTÃO** o sistema deve destacar a seção selecionada e exibir o balão explicativo (*tooltip*) contendo os rótulos e os valores exatos de cada métrica. |

| **Critérios de aceitação** |
| --- |
| Todos os elementos dos gráficos devem responder ao *hover* do mouse, renderizando os valores corretos em balões de informação interativos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/13GSJspN11hIRllEf8oG5slC2UR2NOU54/view?usp=sharing |

---

### Caso de Teste 03: Acesso ao Painel "Resultados da Inteligência" e Filtragem Temporal

| ID | Descrição |
| --- | --- |
| **C07-CT03** | Validar o acionamento do botão "Ver Inteligência" no card "Inteligência Sifit" e a atualização das métricas ao alternar os filtros de período temporal. |

| **Pré-condições** |
| --- |
| Utilizador na tela de Dashboard visualizando o card de Inteligência Sifit. |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela de Dashboard. |
| **E** localiza o bloco "Inteligência Sifit". |
| **QUANDO** clicar no botão "Ver inteligência >". |
| **ENTÃO** o sistema deve redirecionar para a tela "Resultados da Inteligência". |
| **E** ao alternar entre os botões de filtro no canto superior direito (ex.: *Hoje*, *Últimos 7 dias*, *Últimos 30 dias*, *Últimos 90 dias*), as contagens de automações executadas, relatórios enviados, alunos em risco, aniversariantes e demais indicadores devem recalcular e atualizar dinamicamente na tela. |

| **Critérios de aceitação** |
| --- |
| O painel de Resultados da Inteligência deve ser aberto corretamente e responder com precisão aos comandos de seleção do filtro temporal.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1jHxBStstB3JBHW8RBBCIF0m5EY6yqBwt/view?usp=sharing |

