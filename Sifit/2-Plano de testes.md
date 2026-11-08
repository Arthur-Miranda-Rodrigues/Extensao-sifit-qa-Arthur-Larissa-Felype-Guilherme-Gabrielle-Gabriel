# 🧪 **Plano de Testes — SIFIT**

> Documento de planejamento dos testes manuais do sistema **SIFIT** (gestão de academia/box), consolidando os **49 cenários de teste** (RF01–RF49) da pasta `Cenario de Testes`, com **232 casos de teste**, além de **22 casos** documentados apenas no Relatório de Bugs (24 bugs registrados).

---

## 📌 1. Identificação

| Item | Descrição |
|---|---|
| **Nome do Projeto** | SIFIT — Sistema de gestão para academia/box |
| **Projeto de QA** | Extensão em Qualidade de Software — testes manuais do SIFIT |
| **Versão Avaliada** | Versão disponível no ambiente de testes na data da execução (outubro/2026) |
| **Ambiente de Testes** | [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br) |
| **Tipo de Teste** | Teste funcional manual (caixa-preta) |
| **Repositório** | `Extensao-sifit-qa` — GitHub (autor: Arthur-Miranda-Rodrigues), pasta `Sifit/` |
| **Data do Documento** | 08/11/2026 (atualizado; versão original de 24/10/2026) |
| **Versão do Documento** | 1.1 |
| **Responsável** | Arthur Miranda Rodrigues — RA 14538  
Larissa Fernanda O. RA:14536
Felype Augusto Dos Santos Silva 
RA: 14537
Guilherme: Guilherme Felipe de Morais 
RA: 5608
Gabrielle Bonini Barbosa 
RA: 14506
Gabriel de Abreu da Silva — RA 14525 |

---

## 🎯 2. Objetivo

Verificar manualmente, por meio de cenários e casos de teste escritos em BDD (Dado / Quando / Então), se as funcionalidades do SIFIT se comportam conforme o esperado, cobrindo fluxos felizes, validações de campos obrigatórios, filtros, mensagens de erro e restrições de integridade. O foco do trabalho é **avaliar uma aplicação já existente** (sem desenvolvê-la), identificar defeitos e documentar tudo de forma rastreável: requisitos → cenários → casos de teste → evidências → bugs → relatório final.

---

## 🧩 3. Escopo

### ✅ Incluído (49 cenários / 232 casos de teste na pasta)

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

### ❌ Excluído

* Testes de performance, carga e estresse
* Testes de segurança aprofundados (pentest) e de acessibilidade formal
* Testes automatizados
* Testes em aplicativos móveis nativos (apenas a gestão de notificações pela interface web)
* Integrações externas além do que a interface web expõe (ex.: execução real de saque no Pagar.me, envio real por WhatsApp/SMS)

---

## 🔧 4. Ferramentas Utilizadas

| Finalidade | Ferramenta |
|---|---|
| Execução dos testes | Navegador (Chrome/Firefox/Brave) com DevTools |
| Documentação dos cenários | Markdown (`.md`) no padrão Dado/Quando/Então |
| Versionamento | Git / GitHub (commits verificados) |
| Evidências | Gravações de tela em vídeo (links do Google Drive) e prints |
| Consulta ao banco (apoio) | MySQL Workbench |
| Gestão de defeitos | Relatório de Bugs em Markdown (`3-Relatorio de Bugs.md`) |

---

## 🧪 5. Técnicas de Teste

* **Caminho feliz (Happy Path):** cadastro, edição, consulta e exclusão com dados válidos.
* **Testes negativos:** campos obrigatórios em branco, credenciais inválidas, datas inconsistentes.
* **Particionamento de equivalência:** filtros por código, nome, status e tipo (Ativo/Inativo, Aberto/Fechado, Pendente/Realizado).
* **Análise de valor limite:** períodos de datas (data final anterior à inicial), atalhos de período (7, 30, 90 dias).
* **Testes de integridade referencial:** exclusão de registros com vínculos (planos, grupos, categorias, tipos de pagamento).
* **Testes de interface:** modais, tooltips de gráficos, alternância de tema e navegação entre telas.
* **Teste exploratório:** casos extras incluídos durante a execução (ex.: C01-CT04, recuperação de senha).

---

## 📄 6. Critérios de Aceitação

* O comportamento observado de cada caso de teste deve corresponder ao **Critério de aceitação** descrito no cenário.
* Campos obrigatórios devem impedir o envio e exibir mensagem clara.
* Filtros devem retornar apenas registros compatíveis; ao limpar, a listagem retorna ao estado padrão.
* Falhas de servidor devem ser informadas ao usuário e **não** podem ser apresentadas como sucesso.
* Exclusões devem solicitar confirmação e respeitar vínculos existentes.

## 🚦 7. Critérios de Saída (Exit Criteria)

* Os 232 casos de teste dos 49 cenários da pasta, mais os 22 casos registrados apenas no Relatório de Bugs, foram executados e possuem evidência (vídeo/print).
* Todas as divergências foram registradas no **Relatório de Bugs** com título, passos, resultado esperado/obtido, evidência e severidade.
* O **Relatório dos Testes** consolida o total de casos passados, falhos e bloqueados.
* Requisitos (RF01–RF49) rastreáveis até os arquivos de cenário.

## ⏸️ 8. Critérios de Suspensão e Retomada

| Situação | Ação |
|---|---|
| Ambiente fora do ar ou lento | Suspender e retomar após intervalo |
| Acesso ao banco/servidor bloqueado (ex.: conta bloqueada no Workbench) | Suspender os testes que dependem do banco; retomar após liberação de acesso pelo responsável/coordenação |
| Erro de servidor generalizado em um módulo | Registrar bug, marcar casos afetados como bloqueados e seguir para o próximo cenário |

---

## ⏱️ 9. Cronograma Realizado

Linha do tempo reconstruída a partir do histórico de commits do repositório (outubro/2026):

| Data | Atividade |
|---|---|
| 08/10 | Início do repositório; cenários RF01 (Login) e Página Inicial partes 1 a 4 (RF02–RF05) |
| 09/10 | Página Inicial parte 5 (RF06); reorganização da numeração (Dashboard → RF07, Check-ins → RF08) |
| 10/10 | RF09 a RF12 (presenças, aulas do SifitBox, clientes, matrículas) |
| 12/10 | RF13 — Avaliações físicas |
| 13/10 | Contas a receber/pagar (RF14–RF15), fichas de treino (RF16); renumeração em lote dos cenários seguintes |
| 14/10 | Revisões de RF01–RF06, RF14–RF17 e formatação |
| 15/10 | RF18 a RF23 — grupos musculares, objetivos, grupos, turmas, categorias Crossfit, Box |
| 16/10 | RF24 a RF28 — caixas, Pagar.me, despesas fixas, relatórios, colaboradores |
| 17/10 | RF29 a RF35 — funções, fornecedores, documentos, atividades, pontuações, produtos, enquetes |
| 18/10 | RF36 a RF40 — leads, planos, contratos, tipos de pagamento, bandeiras |
| 19/10 | RF41 e RF42 — anamnese; ajustes no RF01 |
| 21/10 | Revisão geral de vários cenários (RF21–RF50) |
| 22/10 | RF45 a RF47 — inteligência, dashboard de resultados e configurações |
| 23/10 | RF48 a RF50; `1-Analise de requistos.md`; atualização do `README.md` |
| 24/10 | Elaboração deste Plano de Testes; próximos: Relatório de Bugs e Relatório dos Testes |
| 29/10 | Relatório de Bugs (24 bugs) e Relatório dos Testes |
| 08/11 | Atualização da Análise de Requisitos, do Plano e do Relatório dos Testes conforme os 49 cenários e os 24 bugs atuais |

> Os números RF citados nas linhas acima seguem a numeração vigente à época de cada commit. A numeração atual (RF01–RF49) é a da seção 10.

---

## 📋 10. Cenários de Teste (Rastreabilidade RF → CT)

| RF | Cenário | Módulo | Casos na pasta | Só no Relatório de Bugs | Prioridade* | Arquivo de origem |
|---|---|---|:---:|:---:|:---:|---|
| RF01 | Login na plataforma | Autenticação | 3 | 1 | Alta | `CT_RF01_Login na plataforma.md` |
| RF02 | Página Inicial (Parte 1) | Página Inicial e Dashboard | 5 | — | Média | `CT_RF02_Acesso A Pagina Inicial Parte 1.md` |
| RF03 | Página Inicial (Parte 2) | Página Inicial e Dashboard | 5 | — | Média | `CT_RF03_Acesso A Pagina Inicial Parte 2.md` |
| RF04 | Página Inicial (Parte 3) | Página Inicial e Dashboard | 5 | — | Média | `CT_RF04_Acesso A Pagina Inicial Parte 3.md` |
| RF05 | Página Inicial (Parte 4) | Página Inicial e Dashboard | 5 | — | Média | `CT_RF05_Acesso A Pagina Inicial Parte 4.md` |
| RF06 | Página Inicial (Parte 5) | Página Inicial e Dashboard | 4 | — | Média | `CT_RF06_Acesso A Pagina  Inicial Parte 5.md` |
| RF07 | Acesso e visualização do Dashboard | Página Inicial e Dashboard | 3 | — | Média | `CT_RF07_ Acesso e visualização do Dashboard.md` |
| RF08 | Gerenciamento de Check-ins | Check-ins e Presenças | 4 | — | Média | `CT_RF08_ Gerenciamento de Check ins.md` |
| RF09 | Consulta e Filtragem de Presenças de Clientes | Check-ins e Presenças | 4 | — | Média | `CT_RF09_Consulta e Filtragem de Presenças de Clientes.md` |
| RF10 | Gestão de Clientes | Clientes, Matrículas e Avaliações | 5 | — | Alta | `CT_RF10_ Gestão de clientes.md` |
| RF11 | Gerenciamento de Matrículas | Clientes, Matrículas e Avaliações | 5 | — | Alta | `CT_RF11_ Gerenciamento de Matriculas.md` |
| RF12 | Gerenciamento de Avaliações Físicas | Clientes, Matrículas e Avaliações | 11 | — | Média | `CT_RF12_ Gestao de avaliações.md` |
| RF13 | Registro e Gestão de Contas a Receber | Financeiro e Relatórios | 6 | — | Alta | `CT_RF13_ Registro de contas a receber.md` |
| RF14 | Registro de Contas a Pagar | Financeiro e Relatórios | 1 | 3 | Alta | `CT_RF14_ Registro de contas a pagar.md` |
| RF15 | Gerenciamento de Fichas de Treino | Treinos e Exercícios | 1 | 1 | Média | `CT_RF15_ Consulta de ficha de treino.md` |
| RF16 | Gerenciamento de Exercícios | Treinos e Exercícios | 3 | — | Média | `CT_RF16_ Gerenciamento de Exercícios.md` |
| RF17 | Gestão de Grupos Musculares | Treinos e Exercícios | 4 | 1 | Baixa | `CT_RF17_ Gestão de grupos musculares.md` |
| RF18 | Gerenciamento de Objetivos Treino | Treinos e Exercícios | 1 | 1 | Baixa | `CT_RF18_ Gerenciamento de objetivos treino.md` |
| RF19 | Gestão de Grupos | Turmas, Grupos e Box | 5 | — | Baixa | `CT_RF19_ Gestão de grupos.md` |
| RF20 | Gestão de Turmas | Turmas, Grupos e Box | 4 | 1 | Média | `CT_RF20_ Gestão de turmas.md` |
| RF21 | Gestão de Categorias Crossfit | Turmas, Grupos e Box | 6 | — | Baixa | `CT_RF21_Gestão de Categorias Crossfit.md` |
| RF22 | Gestão de Box (Turmas e Modalidades) | Turmas, Grupos e Box | 6 | — | Média | `CT_RF22_Gestão de Box - Turmas.md` |
| RF23 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | Financeiro e Relatórios | 7 | — | Alta | `CT_RF23_ Gerenciamento e Filtro de Caixas .md` |
| RF24 | Gestão Financeira e Cobranças via Pagar.me no SIFIT | Financeiro e Relatórios | 10 | — | Alta | `CT_RF24_Gestão Financeira e Cobranças via Pagar.me.md` |
| RF25 | Gerenciamento e Cadastro de Despesas Fixas | Financeiro e Relatórios | 5 | — | Alta | `CT_RF25_Gerenciamento e Cadastro de Despesas Fixas.md` |
| RF26 | Geração e Filtragem de Relatórios Operacionais e Financeiros | Financeiro e Relatórios | 8 | — | Alta | `CT_RF26_Geração e Filtragem de Relatórios Operacionais e Financeiros.md` |
| RF27 | Gestão de Colaboradores via Sistema SIFIT | Colaboradores, Funções e Cadastros de apoio | 7 | — | Alta | `CT_RF27_ Gestão de colaboradores via sistema SIFIT.md` |
| RF28 | Gestão de Funções | Colaboradores, Funções e Cadastros de apoio | 5 | — | Alta | `CT_RF28_Gestão de Funções.md` |
| RF29 | Gerenciamento de Fornecedores no SIFIT | Colaboradores, Funções e Cadastros de apoio | 5 | — | Média | `CT_RF29_Gerenciamento de Fornecedores no SIFIT.md` |
| RF30 | Gerenciamento de Tipos de Documentos no SIFIT | Colaboradores, Funções e Cadastros de apoio | 5 | — | Baixa | `CT_RF30_Gerenciamento de Tipos de Documentos no SIFIT.md` |
| RF31 | Gerenciamento de Atividades no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 4 | 1 | Baixa | `CT_RF31_Gerenciamento de Atividades no SIFIT.md` |
| RF32 | Gerenciamento de Pontuações no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 5 | 3 | Baixa | `CT_RF32_Gerenciamento de Pontuações no SIFIT.md` |
| RF33 | Gerenciamento de Produtos no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 4 | 1 | Baixa | `CT_RF33_Gerenciamento de Produtos no SIFIT.md` |
| RF34 | Módulo de Enquetes | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 2 | 2 | Baixa | `CT_RF34_Filtrar Enquetes por Código, Nome e Status.md` |
| RF35 | Gestão e consulta de leads no módulo Prospecção | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | — | Média | `CT_RF35_Gestão e consulta de leads no módulo Prospecção.md` |
| RF36 | Gestão e consulta de planos no sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | — | Alta | `CT_RF36_Gestão e consulta de planos no sistema SIFIT.md` |
| RF37 | Gestão de Modelos de Contrato no sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 7 | 1 | Média | `CT_RF37_Gestão de Modelos de Contrato no sistema SIFIT.md` |
| RF38 | Gestão de Tipos de Pagamento no Sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | — | Alta | `CT_RF38_Gestão de Tipos de Pagamento no sistema SIFIT.md` |
| RF39 | Gestão de Bandeiras de Cartão no Sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 3 | — | Média | `CT_RF39_ Abrir modal de cadastro de bandeira de cartão.md` |
| RF40 | Aplicação de Fichas de Anamnese no sistema SIFIT | Anamnese | 1 | 2 | Média | `CT_RF40_ Aplicação de Fichas de Anamnese no sistema SIFIT.md` |
| RF41 | Gerenciamento de Modelos de Anamnese no Sistema SIFIT | Anamnese | 5 | — | Média | `CT_RF41_ Gerenciamento de Modelos de Anamnese no sistema SIFIT.md` |
| RF42 | Gerenciamento de Categorias de Anamnese no sistema SIFIT | Anamnese | 5 | — | Média | `CT_RF42_Gerenciamento de Categorias de Anamnese no sistema SIFIT.md` |
| RF43 | Gestão de Pergunta de Anamnese no Sistema SIFIT | Anamnese | 5 | — | Média | `CT_RF43_Gestão de Pergunta de Anamnese.md` |
| RF44 | Módulo Inteligência & Automação e Gestão de Clientes | Inteligência, Automação e Configurações | 9 | — | Média | `CT_RF44_ Gestões de inteligência.md` |
| RF45 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | Inteligência, Automação e Configurações | 1 | — | Média | `CT_RF45_ Visualização e Filtragem do Dashboard de Resultados da Inteligência.md` |
| RF46 | Gestão de configurações | Inteligência, Automação e Configurações | 7 | — | Alta | `CT_RF46_ Gestões de configurações.md` |
| RF47 | Gerenciamento de Modelos de Ficha | Inteligência, Automação e Configurações | 2 | — | Baixa | `CT_RF47_Gerenciamento de Modelos de Ficha.md` |
| RF48 | Gerenciamento de Notificações | Aplicativo e Notificações | 7 | — | Média | `CT_RF48_ Gerenciamento de Notificações e Conteúdos do Aplicativo.md` |
| RF49 | Alternância de Tema da Interface (Claro / Escuro) | Interface (Tema) | 2 | — | Baixa | `CT_RF49_Alternância de Tema da Interface.md` |
| **Total** | **49 cenários** | | **232** | **18** | | |

\* Prioridade **proposta** pelo responsável do teste com base em criticidade para o negócio (acesso, dinheiro, dados de clientes); pode ser revista com o professor/responsável pelo produto.

### 📊 Resumo por módulo

| Módulo | Cenários | Casos na pasta | Só no Relatório de Bugs |
|---|:---:|:---:|:---:|
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

> **Como ler as contagens:** “Casos na pasta” é o número de casos presentes hoje nos arquivos de `Cenario de Testes/` (49 arquivos). “Só no Relatório de Bugs” são casos que existiam no planejamento anterior (254 casos) e hoje aparecem apenas no `3-Relatorio de Bugs.md` — 18 em cenários da pasta e 4 do cenário **Gerenciamento de Aulas do SifitBox**, que não possui arquivo na pasta e por isso não tem número RF na tabela acima.

---

## 🧱 11. Padrão dos Casos de Teste

Cada arquivo em `Sifit/Cenario de Testes/` segue a convenção:

* **Nome do arquivo:** `CT_RFxx_<descrição>.md`
* **ID do caso:** `Cxx-CTyy` (cenário `xx`, caso `yy`) — ex.: `C01-CT04`
* **Estrutura:** ID/Descrição → Pré-condições → Passos (**DADO / QUANDO / ENTÃO**) → Critérios de aceitação → Evidência (link de vídeo no Google Drive)
* **Regra de elaboração:** 1 caso de teste por gravação de tela, quando o cenário é derivado de vídeos.

---

## ⚠️ 12. Pontos de Atenção Observados nos Cenários

Comportamentos descritos nos próprios cenários como falha, erro de gravação ou ausência de resposta. Devem ser confirmados e detalhados no **Relatório de Bugs**; não são tratados como requisito de funcionamento correto.

| Cenário | Casos | Observação registrada |
|---|---|---|
| RF01 — Login | C01-CT04 | Link de recuperação de senha: nada acontece ao clicar (BUG-001) |
| Aulas do SifitBox (sem arquivo na pasta) | CT01–CT04 | Filtro por datas e botão “Gerar aulas” sem efeito visível; data final anterior à inicial não é bloqueada (BUG-002 a BUG-004) |
| RF10 — Clientes | CT04 | Exclusão retorna “Erro no servidor – Erro interno inesperado” (ponto a confirmar) |
| RF11 — Matrículas | CT05 | Exclusão retorna “Erro no servidor – Erro interno inesperado” (ponto a confirmar) |
| RF14 — Contas a Pagar | CT01, CT02, CT03 | Conta cadastrada sem Título e sem Local de Pagamento; filtro de status não aplicado; modal de visualização com dados sem tratamento (BUG-010, BUG-021, BUG-024) |
| RF15 — Fichas de treino | CT01, CT02 | Filtros por código/status não retornam registros; cadastro falha com “Erro ao salvar ficha” (BUG-016) |
| RF17 — Grupos musculares | CT04 | Cadastro aceito sem Nome e sem Tipo Membro (BUG-006) |
| RF18 — Objetivos de treino | CT01, CT02 | Cadastro falha com “Erro ao salvar objetivo”; busca sem resultados (BUG-017) |
| RF20 — Turmas | CT04 | Status vazio na edição, “Erro ao salvar turma” e modal vazio após salvar (BUG-018 a BUG-020) |
| RF31 — Atividades | CT03 | Atividade cadastrada com todos os campos em branco (BUG-007) |
| RF32 — Pontuações | CT03, CT06, CT08 | “Erro ao salvar pontuação”, “Erro no servidor” em ação da coluna Ações e cadastro sem datas (BUG-009, BUG-011, BUG-012) |
| RF33 — Produtos | CT05 | Produto cadastrado sem nome e sem valor (BUG-008) |
| RF34 — Enquetes | CT02–CT04 | “Erro ao salvar enquete” (cadastro e edição) e “Erro ao deletar Enquete” (BUG-013 a BUG-015) |
| RF37 — Modelos de contrato | CT08 | Ao salvar o modelo, a listagem retorna em branco (BUG-023) |
| RF39 — Bandeiras de cartão | CT02 | Ao salvar, nada acontece e a lista continua vazia |
| RF40 — Anamnese (aplicação) | CT01, CT02 | “Finalizar Anamnese” sem efeito; “Erro no servidor” ao finalizar (BUG-005) |
| RF43 — Perguntas de anamnese | CT02 | Alteração do tipo de resposta retorna “Erro ao salvar pergunta” |
| RF46 — Configurações | CT01–CT07 | Todas as abas retornam erro ao salvar (ex.: “Erro ao salvar configurações”) |
| RF47 — Modelos de ficha | CT01 | Cadastro retorna “Erro ao salvar modelo” |
| RF07 — Dashboard | CT01 | Baixo contraste nos títulos e informações dos gráficos (BUG-022) |

**Erros esperados por integridade referencial** (comportamento correto a validar): RF19-CT05 (grupo com vínculos), RF21-CT06 (categoria Crossfit), RF36-CT04 (plano com vínculos) e RF38-CT05 (tipo de pagamento vinculado).

Os defeitos confirmados estão consolidados no `3-Relatorio de Bugs.md` (24 bugs: 10 de severidade alta, 11 média e 3 baixa). As linhas sem referência a BUG-xxx acima ainda não possuem bug formal e aparecem como “pontos a confirmar” ou aguardam registro.

---

## 🐞 13. Gestão de Defeitos

Cada defeito será documentado em `3-Relatorio de Bugs.md` com:

* **ID** (BUG-xx) e **título**
* **Cenário/caso de teste** de origem (ex.: C47-CT01)
* **Passos para reproduzir**
* **Resultado esperado × resultado obtido**
* **Evidência** (vídeo/print)
* **Severidade:** Crítica, Alta, Média ou Baixa
* **Prioridade** e **situação** (Aberto, Em análise, Corrigido, Reteste)

| Severidade | Critério |
|---|---|
| **Crítica** | Impede uso de função essencial (login, cobrança, gravação de dados principais) |
| **Alta** | Falha de gravação/exclusão em módulo importante, sem contorno |
| **Média** | Filtro, validação ou mensagem incorretos, com contorno possível |
| **Baixa** | Problema visual, de texto ou de usabilidade |

---

## 📌 14. Riscos Identificados

| Risco | Impacto | Mitigação |
|---|---|---|
| Sistema fora do ar ou instável (erros de servidor recorrentes) | Alto | Tentar novamente após intervalo; registrar o erro como evidência |
| Bloqueio de acesso ao banco/servidor (já ocorrido com a conta do Workbench) | Médio | Acionar o responsável/coordenação; priorizar testes pela interface web |
| Dados de teste alterados ou excluídos por outros usuários | Médio | Registrar os dados usados em cada caso e recriar quando necessário |
| Evidências em links externos (Google Drive) indisponíveis | Médio | Manter links com acesso configurado e guardar cópia dos vídeos |
| Renumeração de cenários ao longo do projeto (o cenário de Aulas deixou de ter arquivo e os demais foram renumerados; o Relatório de Bugs ainda cita parte dos casos pela numeração antiga, ex.: C21-CT04 = RF20-CT04 atual) | Médio | Usar a tabela da seção 10 como referência oficial de IDs e conferir a correspondência de IDs ao consultar o Relatório de Bugs |
| Falta de especificação oficial do produto | Médio | Basear o resultado esperado no comportamento lógico e na análise de requisitos |

---

## 📁 15. Entregáveis e Referências

### Documentos do projeto (`Sifit/`)

| Arquivo | Conteúdo | Situação |
|---|---|---|
| `1-Analise de requistos.md` | Requisitos funcionais (RF01–RF49) e não funcionais propostos (RNF01–RNF04) | ✅ Atualizado (versão 2.1, 08/11/2026) |
| `2-Plano de testes.md` | Este documento | ✅ Elaborado |
| `Cenario de Testes/CT_RF01 … CT_RF49` | 49 cenários, 232 casos de teste | ✅ Escritos |
| `3-Relatorio de Bugs.md` | Registro dos defeitos encontrados (24 bugs) | ✅ Elaborado (29/10/2026) |
| `4-Relatorio dos testes.md` | Relatório final de execução | ✅ Atualizado (08/11/2026) |

### Referências

* **Sistema sob teste:** [https://sifitalfa.centrion.com.br]
* **Repositório:** `Extensao-sifit-qa` (GitHub — Arthur-Miranda-Rodrigues), branch `main`, commits verificados de 08/10/2026 a 23/10/2026
* **Evidências:** gravações de tela hospedadas no Google Drive, linkadas dentro de cada caso de teste
* **Modelo de plano:** plano de testes do OrangeHRM (Demo), usado como base estrutural
* **README do repositório:** metodologia (testes positivos, negativos, exploratório e funcional; formatos BDD, tabelas e checklist)

---

## ✅ 16. Resumo

| Indicador | Valor |
|---|:---:|
| Requisitos funcionais (RF) | 49 |
| Cenários de teste (pasta) | 49 |
| Casos de teste na pasta | 232 |
| Casos documentados apenas no Relatório de Bugs | 22 |
| Bugs registrados | 24 |
| Módulos funcionais agrupados | 14 |
| Requisitos não funcionais propostos | 4 |
| Período de elaboração | 08/10/2026 a 08/11/2026 |
