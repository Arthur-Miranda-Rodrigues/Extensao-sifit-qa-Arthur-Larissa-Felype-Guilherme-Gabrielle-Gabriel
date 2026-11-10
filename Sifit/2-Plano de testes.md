## 🧪 **Plano de Testes - SIFIT**

### 📌 1. **Identificação**

* **Nome do Projeto**: SIFIT - Sistema de gestão para academia/box
* **Projeto de QA**: Extensão em Qualidade de Software — testes manuais do SIFIT
* **Versão Avaliada**: Demo pública
* **Ambiente de Testes**: [https://sifitalfa.centrion.com.br]
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 08/11/2026
* **Versão do Documento**: 1.2
* **Responsáveis**:

  * Arthur Miranda Rodrigues — RA 14538
  * Larissa Fernanda O. — RA 14536
  * Felype Augusto Dos Santos Silva — RA 14537
  * Guilherme Felipe de Morais — RA 5608
  * Gabrielle Bonini Barbosa — RA 14506
  * Gabriel de Abreu da Silva — RA 14525

---

### 🎯 2. **Objetivo**

Verificar manualmente, por meio de cenários e casos de teste escritos em BDD (Dado / Quando / Então), se as funcionalidades do SIFIT se comportam conforme o esperado, cobrindo fluxos felizes, validações de campos obrigatórios, filtros, mensagens de erro e restrições de integridade. O foco do trabalho é **avaliar uma aplicação já existente** (sem desenvolvê-la), identificar defeitos e documentar tudo de forma rastreável: requisitos → cenários → casos de teste → evidências → bugs → relatório final.

---

### 🧩 3. **Escopo**

**Incluído (49 cenários / 232 casos de teste na pasta):**

* Autenticação e recuperação de senha
* Página Inicial (5 partes) e Dashboard
* Check-ins e presenças; aulas do SifitBox (cenário documentado apenas no Relatório de Bugs, BUG-002 a BUG-004)
* Clientes, matrículas e avaliações físicas
* Financeiro: contas a receber, contas a pagar, caixas, cobranças via Pagar.me, despesas fixas e relatórios
* Treinos: fichas, exercícios, grupos musculares e objetivos
* Turmas, grupos, categorias Crossfit e Box (modalidades e turmas recorrentes)
* Colaboradores, funções, fornecedores e tipos de documentos
* Engajamento: atividades, pontuações, produtos e enquetes
* Comercial: leads (Prospecção), planos, modelos de contrato, tipos de pagamento e bandeiras de cartão
* Anamnese: aplicação de fichas, modelos, categorias e perguntas
* Inteligência & Automação, dashboard de resultados, configurações e modelos de ficha
* Notificações/conteúdos do aplicativo e alternância de tema (claro/escuro)

**Excluído:**

* Testes de performance, carga e estresse
* Testes de segurança aprofundados (pentest) e de acessibilidade formal
* Testes automatizados
* Testes em aplicativos móveis nativos (apenas a gestão de notificações pela interface web)
* Integrações externas além do que a interface web expõe (ex.: execução real de saque no Pagar.me, envio real por WhatsApp/SMS)

---

### 🔧 4. **Ferramentas Utilizadas**

* Navegador Google Chrome / Firefox / Brave
* Ferramentas de inspeção do navegador (DevTools)
* Markdown (`.md`) no padrão Dado/Quando/Então (documentação dos cenários)
* Git / GitHub (versionamento, com commits verificados)
* Gravações de tela em vídeo (links do Google Drive) e prints (evidências)
* MySQL Workbench (consulta ao banco, como apoio)
* Relatório de Bugs em Markdown (`3-Relatorio de Bugs.md`) para gestão de defeitos

---

### 🧪 5. **Técnicas de Teste**

* **Particionamento de equivalência:** filtros por código, nome, status e tipo (Ativo/Inativo, Aberto/Fechado, Pendente/Realizado).
* **Análise de valor limite:** períodos de datas (data final anterior à inicial) e atalhos de período (7, 30, 90 dias).
* **Caminho feliz (Happy Path):** cadastro, edição, consulta e exclusão com dados válidos.
* **Testes negativos:** campos obrigatórios em branco, credenciais inválidas, datas inconsistentes.
* **Testes de integridade referencial:** exclusão de registros com vínculos (planos, grupos, categorias, tipos de pagamento).
* **Testes de interface:** modais, tooltips de gráficos, alternância de tema e navegação entre telas.
* **Testes exploratórios:** casos extras incluídos durante a execução (ex.: C01-CT04, recuperação de senha).

---

### 📄 6. **Critérios de Aceitação**

* O comportamento observado de cada caso de teste deve corresponder ao **critério de aceitação** descrito no cenário.
* Campos obrigatórios devem impedir o envio e exibir mensagem clara.
* Filtros devem retornar apenas registros compatíveis; ao limpar, a listagem retorna ao estado padrão.
* Falhas de servidor devem ser informadas ao usuário e **não** podem ser apresentadas como sucesso.
* Exclusões devem solicitar confirmação e respeitar vínculos existentes.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* Os 232 casos de teste dos 49 cenários da pasta, mais os 22 casos registrados apenas no Relatório de Bugs, foram executados e possuem evidência (vídeo/print).
* Todas as divergências foram registradas no **Relatório de Bugs** com título, passos, resultado esperado/obtido, evidência e severidade.
* O **Relatório dos Testes** consolida o total de casos passados, falhos e bloqueados.
* Requisitos (RF01–RF49) rastreáveis até os arquivos de cenário.

**⏸️ Critérios de Suspensão e Retomada**

| Situação | Ação |
| -------- | ---- |
| Ambiente fora do ar ou lento | Suspender e retomar após intervalo |
| Acesso ao banco/servidor bloqueado (ex.: conta bloqueada no Workbench) | Suspender os testes que dependem do banco; retomar após liberação de acesso pelo responsável/coordenação |
| Erro de servidor generalizado em um módulo | Registrar bug, marcar casos afetados como bloqueados e seguir para o próximo cenário |

---

### ⏱️ 8. **Cronograma Realizado**

Linha do tempo reconstruída a partir do histórico de commits do repositório (outubro/2026).

| Atividade | Data Início | Data Fim |
| --------- | ----------- | -------- |
| Cenários RF01 (Login) e Página Inicial partes 1 a 4 (RF02–RF05) | 08/10/2026 | 08/10/2026 |
| Página Inicial parte 5 (RF06); reorganização da numeração (Dashboard → RF07, Check-ins → RF08) | 09/10/2026 | 09/10/2026 |
| Presenças, aulas do SifitBox, clientes e matrículas (RF09–RF12) | 10/10/2026 | 10/10/2026 |
| Avaliações físicas (RF13) | 12/10/2026 | 12/10/2026 |
| Contas a receber/pagar, fichas de treino; renumeração em lote dos cenários seguintes | 13/10/2026 | 13/10/2026 |
| Revisões de RF01–RF06, RF14–RF17 e formatação | 14/10/2026 | 14/10/2026 |
| Grupos musculares, objetivos, grupos, turmas, categorias Crossfit e Box (RF18–RF23) | 15/10/2026 | 15/10/2026 |
| Caixas, Pagar.me, despesas fixas, relatórios e colaboradores (RF24–RF28) | 16/10/2026 | 16/10/2026 |
| Funções, fornecedores, documentos, atividades, pontuações, produtos e enquetes (RF29–RF35) | 17/10/2026 | 17/10/2026 |
| Leads, planos, contratos, tipos de pagamento e bandeiras (RF36–RF40) | 18/10/2026 | 18/10/2026 |
| Anamnese (RF41 e RF42); ajustes no RF01 | 19/10/2026 | 19/10/2026 |
| Revisão geral de vários cenários (RF21–RF50) | 21/10/2026 | 21/10/2026 |
| Inteligência, dashboard de resultados e configurações (RF45–RF47) | 22/10/2026 | 22/10/2026 |
| Cenários RF48 a RF50; Análise de Requisitos; atualização do `README.md` | 23/10/2026 | 23/10/2026 |
| Elaboração do Plano de Testes | 24/10/2026 | 24/10/2026 |
| Registro e Report de Bugs (24 bugs) e Relatório dos Testes | 29/10/2026 | 29/10/2026 |
| Atualização da Análise de Requisitos, do Plano e do Relatório dos Testes conforme os 49 cenários e os 24 bugs atuais | 08/11/2026 | 08/11/2026 |

> Os números RF citados nas linhas acima seguem a numeração vigente à época de cada commit. A numeração atual (RF01–RF49) é a da seção 9.

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo | Prioridade | Casos de teste* |
| --------- | ------ | ---------- | --------------- |
| RF01 | Login na plataforma | Alta | 3 (+1) |
| RF02 | Página Inicial (Parte 1) | Média | 5 |
| RF03 | Página Inicial (Parte 2) | Média | 5 |
| RF04 | Página Inicial (Parte 3) | Média | 5 |
| RF05 | Página Inicial (Parte 4) | Média | 5 |
| RF06 | Página Inicial (Parte 5) | Média | 4 |
| RF07 | Acesso e visualização do Dashboard | Média | 3 |
| RF08 | Gerenciamento de Check-ins | Média | 4 |
| RF09 | Consulta e Filtragem de Presenças de Clientes | Média | 4 |
| RF10 | Gestão de Clientes | Alta | 5 |
| RF11 | Gerenciamento de Matrículas | Alta | 5 |
| RF12 | Gerenciamento de Avaliações Físicas | Média | 11 |
| RF13 | Registro e Gestão de Contas a Receber | Alta | 6 |
| RF14 | Registro de Contas a Pagar | Alta | 1 (+3) |
| RF15 | Gerenciamento de Fichas de Treino | Média | 1 (+1) |
| RF16 | Gerenciamento de Exercícios | Média | 3 |
| RF17 | Gestão de Grupos Musculares | Baixa | 4 (+1) |
| RF18 | Gerenciamento de Objetivos Treino | Baixa | 1 (+1) |
| RF19 | Gestão de Grupos | Baixa | 5 |
| RF20 | Gestão de Turmas | Média | 4 (+1) |
| RF21 | Gestão de Categorias Crossfit | Baixa | 6 |
| RF22 | Gestão de Box (Turmas e Modalidades) | Média | 6 |
| RF23 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | Alta | 7 |
| RF24 | Gestão Financeira e Cobranças via Pagar.me | Alta | 10 |
| RF25 | Gerenciamento e Cadastro de Despesas Fixas | Alta | 5 |
| RF26 | Geração e Filtragem de Relatórios Operacionais e Financeiros | Alta | 8 |
| RF27 | Gestão de Colaboradores via Sistema SIFIT | Alta | 7 |
| RF28 | Gestão de Funções | Alta | 5 |
| RF29 | Gerenciamento de Fornecedores | Média | 5 |
| RF30 | Gerenciamento de Tipos de Documentos | Baixa | 5 |
| RF31 | Gerenciamento de Atividades | Baixa | 4 (+1) |
| RF32 | Gerenciamento de Pontuações | Baixa | 5 (+3) |
| RF33 | Gerenciamento de Produtos | Baixa | 4 (+1) |
| RF34 | Módulo de Enquetes | Baixa | 2 (+2) |
| RF35 | Gestão e consulta de leads no módulo Prospecção | Média | 5 |
| RF36 | Gestão e consulta de planos | Alta | 5 |
| RF37 | Gestão de Modelos de Contrato | Média | 7 (+1) |
| RF38 | Gestão de Tipos de Pagamento | Alta | 5 |
| RF39 | Gestão de Bandeiras de Cartão | Média | 3 |
| RF40 | Aplicação de Fichas de Anamnese | Média | 1 (+2) |
| RF41 | Gerenciamento de Modelos de Anamnese | Média | 5 |
| RF42 | Gerenciamento de Categorias de Anamnese | Média | 5 |
| RF43 | Gestão de Pergunta de Anamnese | Média | 5 |
| RF44 | Módulo Inteligência & Automação e Gestão de Clientes | Média | 9 |
| RF45 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | Média | 1 |
| RF46 | Gestão de configurações | Alta | 7 |
| RF47 | Gerenciamento de Modelos de Ficha | Baixa | 2 |
| RF48 | Gerenciamento de Notificações | Média | 7 |
| RF49 | Alternância de Tema da Interface (Claro / Escuro) | Baixa | 2 |
| **Total** | **49 cenários** | | **232 (+18)** |

\* Número de casos presentes na pasta `Cenario de Testes/`; o valor entre parênteses indica casos que constam **apenas** no Relatório de Bugs. Prioridade **proposta** pelo responsável do teste com base na criticidade para o negócio (acesso, dinheiro, dados de clientes); pode ser revista com o professor/responsável pelo produto.

Cada RFxx corresponde ao arquivo `CT_RFxx_<descrição>.md`, em `Sifit/Cenario de Testes/`.

**📊 Resumo por módulo**

| Módulo | Cenários | Casos na pasta | Só no Relatório de Bugs |
| ------ | :------: | :------------: | :---------------------: |
| Autenticação | 1 | 3 | 1 |
| Página Inicial e Dashboard | 6 | 27 | — |
| Check-ins e Presenças | 2 | 8 | — |
| Clientes, Matrículas e Avaliações | 3 | 21 | — |
| Financeiro e Relatórios | 6 | 37 | 3 |
| Treinos e Exercícios | 4 | 9 | 3 |
| Turmas, Grupos e Box | 4 | 21 | 1 |
| Colaboradores, Funções e Cadastros de apoio | 4 | 22 | — |
| Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 4 | 15 | 7 |
| Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | 25 | 1 |
| Anamnese | 4 | 16 | 2 |
| Inteligência, Automação e Configurações | 4 | 19 | — |
| Aplicativo e Notificações | 1 | 7 | — |
| Interface (Tema) | 1 | 2 | — |
| **Total** | **49** | **232** | **18** |

> **Como ler as contagens:** as 18 ocorrências "só no Relatório de Bugs" são casos de cenários da pasta que existiam no planejamento anterior (254 casos) e hoje aparecem apenas no `3-Relatorio de Bugs.md`. Somam-se a elas 4 casos do cenário **Gerenciamento de Aulas do SifitBox**, que não possui arquivo na pasta nem número RF (22 casos no total fora da pasta).

**🧱 Padrão dos Casos de Teste**

* **Nome do arquivo:** `CT_RFxx_<descrição>.md`
* **ID do caso:** `Cxx-CTyy` (cenário `xx`, caso `yy`) — ex.: `C01-CT04`
* **Estrutura:** ID/Descrição → Pré-condições → Passos (**DADO / QUANDO / ENTÃO**) → Critérios de aceitação → Evidência (link de vídeo no Google Drive)
* **Regra de elaboração:** 1 caso de teste por gravação de tela, quando o cenário é derivado de vídeos.

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão documentados em `3-Relatorio de Bugs.md` com:

  * ID (BUG-xx) e título
  * Cenário/caso de teste de origem (ex.: C47-CT01)
  * Passos para reproduzir
  * Resultado esperado × resultado obtido
  * Evidência (print ou vídeo)
  * Gravidade (Crítica, Alta, Média, Baixa)
  * Prioridade e situação (Aberto, Em análise, Corrigido, Reteste)
* Ferramenta utilizada: Relatório de Bugs em Markdown (`3-Relatorio de Bugs.md`)
* Defeitos confirmados: **24 bugs** (10 de severidade alta, 11 média e 3 baixa)

| Severidade | Critério |
| ---------- | -------- |
| **Crítica** | Impede uso de função essencial (login, cobrança, gravação de dados principais) |
| **Alta** | Falha de gravação/exclusão em módulo importante, sem contorno |
| **Média** | Filtro, validação ou mensagem incorretos, com contorno possível |
| **Baixa** | Problema visual, de texto ou de usabilidade |

**⚠️ Pontos de Atenção Observados nos Cenários**

Comportamentos descritos nos próprios cenários como falha, erro de gravação ou ausência de resposta. Devem ser confirmados e detalhados no Relatório de Bugs; não são tratados como requisito de funcionamento correto.

| Cenário | Casos | Observação registrada |
| ------- | ----- | --------------------- |
| RF01 — Login | C01-CT04 | Link de recuperação de senha: nada acontece ao clicar (BUG-001) |
| Aulas do SifitBox (sem arquivo na pasta) | CT01–CT04 | Filtro por datas e botão "Gerar aulas" sem efeito visível; data final anterior à inicial não é bloqueada (BUG-002 a BUG-004) |
| RF07 — Dashboard | CT01 | Baixo contraste nos títulos e informações dos gráficos (BUG-022) |
| RF10 — Clientes | CT04 | Exclusão retorna "Erro no servidor – Erro interno inesperado" (ponto a confirmar) |
| RF11 — Matrículas | CT05 | Exclusão retorna "Erro no servidor – Erro interno inesperado" (ponto a confirmar) |
| RF14 — Contas a Pagar | CT01, CT02, CT03 | Conta cadastrada sem Título e sem Local de Pagamento; filtro de status não aplicado; modal de visualização com dados sem tratamento (BUG-010, BUG-021, BUG-024) |
| RF15 — Fichas de treino | CT01, CT02 | Filtros por código/status não retornam registros; cadastro falha com "Erro ao salvar ficha" (BUG-016) |
| RF17 — Grupos musculares | CT04 | Cadastro aceito sem Nome e sem Tipo Membro (BUG-006) |
| RF18 — Objetivos de treino | CT01, CT02 | Cadastro falha com "Erro ao salvar objetivo"; busca sem resultados (BUG-017) |
| RF20 — Turmas | CT04 | Status vazio na edição, "Erro ao salvar turma" e modal vazio após salvar (BUG-018 a BUG-020) |
| RF31 — Atividades | CT03 | Atividade cadastrada com todos os campos em branco (BUG-007) |
| RF32 — Pontuações | CT03, CT06, CT08 | "Erro ao salvar pontuação", "Erro no servidor" em ação da coluna Ações e cadastro sem datas (BUG-009, BUG-011, BUG-012) |
| RF33 — Produtos | CT05 | Produto cadastrado sem nome e sem valor (BUG-008) |
| RF34 — Enquetes | CT02–CT04 | "Erro ao salvar enquete" (cadastro e edição) e "Erro ao deletar Enquete" (BUG-013 a BUG-015) |
| RF37 — Modelos de contrato | CT08 | Ao salvar o modelo, a listagem retorna em branco (BUG-023) |
| RF39 — Bandeiras de cartão | CT02 | Ao salvar, nada acontece e a lista continua vazia |
| RF40 — Anamnese (aplicação) | CT01, CT02 | "Finalizar Anamnese" sem efeito; "Erro no servidor" ao finalizar (BUG-005) |
| RF43 — Perguntas de anamnese | CT02 | Alteração do tipo de resposta retorna "Erro ao salvar pergunta" |
| RF46 — Configurações | CT01–CT07 | Todas as abas retornam erro ao salvar (ex.: "Erro ao salvar configurações") |
| RF47 — Modelos de ficha | CT01 | Cadastro retorna "Erro ao salvar modelo" |

**Erros esperados por integridade referencial** (comportamento correto a validar): RF19-CT05 (grupo com vínculos), RF21-CT06 (categoria Crossfit), RF36-CT04 (plano com vínculos) e RF38-CT05 (tipo de pagamento vinculado).

As linhas sem referência a BUG-xxx ainda não possuem bug formal e aparecem como "pontos a confirmar" ou aguardam registro.

---

### 📌 11. **Riscos Identificados**

| Risco | Impacto | Mitigação |
| ----- | ------- | --------- |
| Sistema fora do ar ou instável (erros de servidor recorrentes) | Alto | Tentar novamente após intervalo; registrar o erro como evidência |
| Bloqueio de acesso ao banco/servidor (já ocorrido com a conta do Workbench) | Médio | Acionar o responsável/coordenação; priorizar testes pela interface web |
| Dados de teste alterados ou excluídos por outros usuários | Médio | Registrar os dados usados em cada caso e recriar quando necessário |
| Evidências em links externos (Google Drive) indisponíveis | Médio | Manter links com acesso configurado e guardar cópia dos vídeos |
| Renumeração de cenários ao longo do projeto (o cenário de Aulas deixou de ter arquivo e os demais foram renumerados; o Relatório de Bugs ainda cita parte dos casos pela numeração antiga, ex.: C21-CT04 = RF20-CT04 atual) | Médio | Usar a tabela da seção 9 como referência oficial de IDs e conferir a correspondência ao consultar o Relatório de Bugs |
| Falta de especificação oficial do produto | Médio | Basear o resultado esperado no comportamento lógico e na análise de requisitos |

---

### 📁 12. **Entregáveis**

* **Análise de Requisitos** (`1-Analise de Requisitos.md`) .
* **Plano de Testes** (`2-Plano de testes.md`) — este documento · 
* **Casos de Teste** (`Cenario de Testes/CT_RF01 … CT_RF49`) — 49 cenários, 232 casos ·
* **Evidências de Execução** — gravações de tela hospedadas no Google Drive, linkadas dentro de cada caso de teste
* **Registro de Bugs** (`3-Relatorio de Bugs.md`) — 24 bugs ·
* **Relatório Final de Execução** (`4-Relatorio dos testes.md`) ·


