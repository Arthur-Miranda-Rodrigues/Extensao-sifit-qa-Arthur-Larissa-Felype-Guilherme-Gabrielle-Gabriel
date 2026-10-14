---
# Cenário 4: Página Inicial (Parte 3)
---
### Caso de Teste 01: Ações Recomendadas - Falar com Alunos Inativos


| ID | Descrição |
| --- | --- |
| **C04-CT01** | Validar a abertura do modal "Falar com inativos" a partir da seção "Ações recomendadas para hoje", a busca por alunos, personalização de mensagem e seleção do canal de envio.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT e posicionado no bloco "Ações recomendadas para hoje". |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial. |
| **QUANDO** clicar no botão "Enviar mensagem" dentro do card "Falar com inativos". |
| **E** o modal de comunicação for exibido. |
| **E** utilizar o campo "Buscar aluno..." para filtrar os alunos destinatários. |
| **E** verificar os campos de personalização da mensagem (mensagens sugeridas, templates, variáveis dinâmicas) e escolha do canal de envio (ex.: WhatsApp). |
| **ENTÃO** o sistema deve carregar as opções de envio e permitir a configuração/envio da mensagem para a lista de alunos selecionados. |

| **Critérios de aceitação** |
| --- |
| O modal "Falar com inativos" deve carregar os dados dos alunos inativos há mais de 15 dias, permitir filtragem por busca e apresentar os modelos de mensagem e canais de comunicação disponíveis. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1kkjRtBYSNtbofbZqa2vVh0zY3FqK41P4/view?usp=sharing |

---

### Caso de Teste 02: Ações Recomendadas - Cobrar Alunos com Pagamento em Aberto

| ID | Descrição |
| --- | --- |
| **C04-CT02** | Verificar a funcionalidade do card "Cobrar alunos", validando a abertura do modal de cobrança, busca por alunos inadimplentes e personalização da mensagem de cobrança segura. |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT. |

| **Passos** |
| --- |
| **DADO** que o utilizador está no bloco "Ações recomendadas para hoje". |
| **QUANDO** clicar no botão "Cobrar agora" dentro do card "Cobrar alunos". |
| **E** o modal de cobrança em aberto for exibido. |
| **E** utilizar o campo de busca de alunos no passo 1 ("Selecione os alunos"). |
| **E** visualizar o resumo das métricas de cobrança (total a receber, taxa de resposta) e o template de mensagem no passo 2. |
| **ENTÃO** o sistema deve filtrar os alunos devedores e preparar o lote para envio da mensagem de cobrança. |

| **Critérios de aceitação** |
| --- |
| O modal de cobrança deve abrir corretamente com as métricas de pagamentos em aberto e disponibilizar o fluxo de envio e busca de alunos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/10u5M5_lnJRy-3HOeoy6bK5a22CpI5PwM/view?usp=sharing |

---

### Caso de Teste 03: Visualização e Filtro da Seção de Aniversariantes do Dia

| ID | Descrição |
| --- | --- |
| **C04-CT03** | Validar o redirecionamento ao clicar em "Ver todos" na seção "Aniversariantes do dia" e a filtragem no modal por período (7 dias, 33 dias) e navegação mensal no calendário. |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial. |
| **QUANDO** clicar no link "Ver todos" do bloco "Aniversariantes do dia". |
| **E** o modal "Aniversariantes" for exibido. |
| **E** alternar entre as abas de período (ex.: *Próximos 7 dias*, *Próximos 33 dias*). |
| **E** navegar entre os meses no calendário de visualização (ex.: *Outubro de 2026*, *Setembro de 2026*). |
| **ENTÃO** o sistema deve atualizar dinamicamente a contagem e a tabela de aniversariantes conforme o mês e o intervalo de dias selecionado. |

| **Critérios de aceitação** |
| --- |
| O modal de aniversariantes deve filtrar e listar corretamente os aniversariantes do período e permitir a navegação entre os meses do ano. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1n0zkEwa_epGNjDbN2koPkTV_GcTA4IU_/view?usp=sharing |

---

### Caso de Teste 04: Redirecionamento da Seção "Últimas Entradas na Academia"

| ID | Descrição |
| --- | --- |
| **C04-CT04** | Garantir que o link "Ver todos" no bloco "Últimas entradas na academia" redireciona o utilizador para a tela operacional de Presenças. |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT. |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial visualizando a tabela de "Últimas entradas na academia". |
| **QUANDO** clicar no link "Ver todos" localizado no cabeçalho desse bloco. |
| **ENTÃO** o sistema deve redirecionar o utilizador para a tela de **Presenças** (`/presencas`). |
| **E** exibir a tela completa de gerenciamento e histórico de presenças da academia com seus respectivos filtros e indicadores. |

| **Critérios de aceitação** |
| --- |
| O clique em "Ver todos" nas últimas entradas deve efetuar o redirecionamento imediato para a página de Presenças do sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DS4DgTOavEO8JWwgCemy4tf9-YZXP1L2/view?usp=sharing |

---

### Caso de Teste 05: Navegação e Execução de Automações na Inteligência de Retenção

| ID | Descrição |
| --- | --- |
| **C04-CT05** | Validar o direcionamento para a "Central de Automações" através do link "Ver análise completa" na seção de Inteligência de Retenção e a interação com a execução de automações e relatórios de risco de evasão. |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT. |

| **Passos** |
| --- |
| **DADO** que o utilizador está no bloco "Inteligência de Retenção" no Dashboard. |
| **QUANDO** clicar no link "Ver análise completa". |
| **ENTÃO** o sistema deve redirecionar para a tela "Central de Automações / Inteligência & Automação". |
| **E** ao clicar em "Executar agora" em uma automação (ex.: *Risco de Evasão* ou *Aniversariantes*), o sistema deve atualizar os resultados ou exibir o aviso referente à execução manual (ex.: *"Execução manual ainda não disponível para esta automação"*). |
| **E** ao clicar em "Ver resultados", deve expandir o "Relatório de Risco de Evasão" detalhando os alunos por nível de risco (Alto, Médio, Baixo). |

| **Critérios de aceitação** |
| --- |
| O link de análise completa deve abrir a Central de Automações, exibindo o status das automações ativas, avisos de sistema e o relatório detalhado de risco de evasão. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Dp8i5hFZfDGJWQdvwp_yFGS0a1wdqxIW/view?usp=sharing |
