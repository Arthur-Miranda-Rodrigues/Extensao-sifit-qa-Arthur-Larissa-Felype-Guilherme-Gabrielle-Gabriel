# 🧪 **Plano de Testes — SIFIT**

> Documento de planejamento dos testes manuais do sistema **SIFIT** (gestão de academia/box), consolidando os **50 cenários de teste** (RF01–RF50) e os **254 casos de teste** documentados no repositório.

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
| **Data do Documento** | 24/10/2026 |
| **Versão do Documento** | 1.0 |
| **Responsável** | Arthur Miranda Rodrigues — RA 14538 |

---

## 🎯 2. Objetivo

Verificar manualmente, por meio de cenários e casos de teste escritos em BDD (Dado / Quando / Então), se as funcionalidades do SIFIT se comportam conforme o esperado, cobrindo fluxos felizes, validações de campos obrigatórios, filtros, mensagens de erro e restrições de integridade. O foco do trabalho é **avaliar uma aplicação já existente** (sem desenvolvê-la), identificar defeitos e documentar tudo de forma rastreável: requisitos → cenários → casos de teste → evidências → bugs → relatório final.

---

## 🧩 3. Escopo

### ✅ Incluído (50 cenários / 254 casos de teste)

* Autenticação e recuperação de senha
* Página Inicial (5 partes) e Dashboard
* Check-ins, presenças e aulas do SifitBox
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

* Os 254 casos de teste dos 50 cenários foram executados e possuem evidência (vídeo/print).
* Todas as divergências foram registradas no **Relatório de Bugs** com título, passos, resultado esperado/obtido, evidência e severidade.
* O **Relatório dos Testes** consolida o total de casos passados, falhos e bloqueados.
* Requisitos (RF01–RF50) rastreáveis até os arquivos de cenário.

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

---

## 📋 10. Cenários de Teste (Rastreabilidade RF → CT)

| RF | Cenário | Módulo | Casos de teste | Prioridade* | Arquivo de origem |
|---|---|---|:---:|:---:|---|
| RF01 | Login na plataforma | Autenticação | 4 | Alta | `CT_RF01_Login na plataforma.md` |
| RF02 | Página Inicial (Parte 1) | Página Inicial e Dashboard | 5 | Média | `CT_RF02_Acesso A Pagina Inicial Parte 1.md` |
| RF03 | Página Inicial (Parte 2) | Página Inicial e Dashboard | 5 | Média | `CT_RF03_Acesso A Pagina Inicial Parte 2.md` |
| RF04 | Página Inicial (Parte 3) | Página Inicial e Dashboard | 5 | Média | `CT_RF04_Acesso A Pagina Inicial Parte 3.md` |
| RF05 | Página Inicial (Parte 4) | Página Inicial e Dashboard | 5 | Média | `CT_RF05_Acesso A Pagina Inicial Parte 4.md` |
| RF06 | Página Inicial (Parte 5) | Página Inicial e Dashboard | 4 | Média | `CT_RF06_Acesso A Pagina  Inicial Parte 5.md` |
| RF07 | Acesso e visualização do Dashboard | Página Inicial e Dashboard | 3 | Média | `CT_RF07_ Acesso e visualização do Dashboard.md` |
| RF08 | Gerenciamento de Check-ins | Check-ins, Presenças e Aulas | 4 | Média | `CT_RF08_ Gerenciamento de Check ins.md` |
| RF09 | Consulta e Filtragem de Presenças de Clientes | Check-ins, Presenças e Aulas | 4 | Média | `CT_RF09_Consulta e Filtragem de Presenças de Clientes.md` |
| RF10 | Gerenciamento de Aulas do SifitBox | Check-ins, Presenças e Aulas | 4 | Média | `CT_RF10_Gerenciamento de Aulas do SifitBox.md` |
| RF11 | Gestão de Clientes | Clientes, Matrículas e Avaliações | 5 | Alta | `CT_RF11_ Gestão de clientes.md` |
| RF12 | Gerenciamento de Matrículas | Clientes, Matrículas e Avaliações | 5 | Alta | `CT_RF12_ Gerenciamento de Matriculas.md` |
| RF13 | Gerenciamento de Avaliações Físicas | Clientes, Matrículas e Avaliações | 11 | Média | `CT_RF13_ Gestao de avaliações.md` |
| RF14 | Registro e Gestão de Contas a Receber | Financeiro e Relatórios | 6 | Alta | `CT_RF14_ Registro de contas a receber.md` |
| RF15 | Registro de Contas a Pagar | Financeiro e Relatórios | 4 | Alta | `CT_RF15_ Registro de contas a pagar.md` |
| RF16 | Gerenciamento de Fichas de Treino | Treinos e Exercícios | 2 | Média | `CT_RF16_ Consulta de ficha de treino.md` |
| RF17 | Gerenciamento de Exercícios | Treinos e Exercícios | 3 | Média | `CT_RF17_ Gerenciamento de Exercícios.md` |
| RF18 | Gestão de Grupos Musculares | Treinos e Exercícios | 5 | Baixa | `CT_RF18_ Gestão de grupos musculares.md` |
| RF19 | Gerenciamento de Objetivos Treino | Treinos e Exercícios | 2 | Baixa | `CT_RF19_ Gerenciamento de objetivos treino.md` |
| RF20 | Gestão de Grupos | Turmas, Grupos e Box | 5 | Baixa | `CT_RF20_ Gestão de grupos.md` |
| RF21 | Gestão de Turmas | Turmas, Grupos e Box | 5 | Média | `CT_RF21_ Gestão de turmas.md` |
| RF22 | Gestão de Categorias Crossfit | Turmas, Grupos e Box | 6 | Baixa | `CT_RF22_Gestão de Categorias Crossfit.md` |
| RF23 | Gestão de Box – Turmas e Modalidades | Turmas, Grupos e Box | 6 | Média | `CT_RF23_Gestão de Box - Turmas.md` |
| RF24 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | Financeiro e Relatórios | 7 | Alta | `CT_RF24_ Gerenciamento e Filtro de Caixas .md` |
| RF25 | Gestão Financeira e Cobranças via Pagar.me no SIFIT | Financeiro e Relatórios | 10 | Alta | `CT_RF25_Gestão Financeira e Cobranças via Pagar.me.md` |
| RF26 | Gerenciamento e Cadastro de Despesas Fixas | Financeiro e Relatórios | 5 | Alta | `CT_RF26_Gerenciamento e Cadastro de Despesas Fixas.md` |
| RF27 | Geração e Filtragem de Relatórios Operacionais e Financeiros | Financeiro e Relatórios | 8 | Alta | `CT_RF27_Geração e Filtragem de Relatórios Operacionais e Financeiros.md` |
| RF28 | Gestão de Colaboradores via Sistema SIFIT | Colaboradores, Funções e Cadastros de apoio | 7 | Alta | `CT_RF28_ Gestão de colaboradores via sistema SIFIT.md` |
| RF29 | Gestão de Funções | Colaboradores, Funções e Cadastros de apoio | 5 | Alta | `CT_RF29_Gestão de Funções.md` |
| RF30 | Gerenciamento de Fornecedores no SIFIT | Colaboradores, Funções e Cadastros de apoio | 5 | Média | `CT_RF30_Gerenciamento de Fornecedores no SIFIT.md` |
| RF31 | Gerenciamento de Tipos de Documentos no SIFIT | Colaboradores, Funções e Cadastros de apoio | 5 | Baixa | `CT_RF31_Gerenciamento de Tipos de Documentos no SIFIT.md` |
| RF32 | Gerenciamento de Atividades no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 5 | Baixa | `CT_RF32_Gerenciamento de Atividades no SIFIT.md` |
| RF33 | Gerenciamento de Pontuações no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 8 | Baixa | `CT_RF33_Gerenciamento de Pontuações no SIFIT.md` |
| RF34 | Gerenciamento de Produtos no SIFIT | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 5 | Baixa | `CT_RF34_Gerenciamento de Produtos no SIFIT.md` |
| RF35 | Módulo de Enquetes (filtro por Código, Nome e Status) | Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 4 | Baixa | `CT_RF35_Filtrar Enquetes por Código, Nome e Status.md` |
| RF36 | Gestão e consulta de leads no módulo Prospecção | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | Média | `CT_RF36_Gestão e consulta de leads no módulo Prospecção.md` |
| RF37 | Gestão e consulta de planos no sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | Alta | `CT_RF37_Gestão e consulta de planos no sistema SIFIT.md` |
| RF38 | Gestão de Modelos de Contrato no sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 8 | Média | `CT_RF38_Gestão de Modelos de Contrato no sistema SIFIT.md` |
| RF39 | Gestão de Tipos de Pagamento no Sistema SIFIT | Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | Alta | `CT_RF39_Gestão de Tipos de Pagamento no sistema SIFIT.md` |
| RF40 | Gestão de Bandeiras de Cartão (modal de cadastro) | Comercial (Leads, Planos, Contratos, Pagamentos) | 3 | Média | `CT_RF40_ Abrir modal de cadastro de bandeira de cartão.md` |
| RF41 | Aplicação de Fichas de Anamnese no sistema SIFIT | Anamnese | 3 | Média | `CT_RF41_ Aplicação de Fichas de Anamnese no sistema SIFIT.md` |
| RF42 | Gerenciamento de Modelos de Anamnese no Sistema SIFIT | Anamnese | 5 | Média | `CT_RF42_ Gerenciamento de Modelos de Anamnese no sistema SIFIT.md` |
| RF43 | Gerenciamento de Categorias de Anamnese no sistema SIFIT | Anamnese | 5 | Média | `CT_RF43_Gerenciamento de Categorias de Anamnese no sistema SIFIT.md` |
| RF44 | Gestão de Pergunta de Anamnese no Sistema SIFIT | Anamnese | 5 | Média | `CT_RF44_Gestão de Pergunta de Anamnese.md` |
| RF45 | Módulo Inteligência & Automação e Gestão de Clientes | Inteligência, Automação e Configurações | 9 | Média | `CT_RF45_ Gestões de inteligência.md` |
| RF46 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | Inteligência, Automação e Configurações | 1 | Média | `CT_RF46_ Visualização e Filtragem do Dashboard de Resultados da Inteligência.md` |
| RF47 | Gestão de configurações | Inteligência, Automação e Configurações | 7 | Alta | `CT_RF47_ Gestões de configurações.md` |
| RF48 | Gerenciamento de Modelos de Ficha | Inteligência, Automação e Configurações | 2 | Baixa | `CT_RF48_Gerenciamento de Modelos de Ficha.md` |
| RF49 | Gerenciamento de Notificações | Aplicativo e Notificações | 7 | Média | `CT_RF49_ Gerenciamento de Notificações e Conteúdos do Aplicativo.md` |
| RF50 | Alternância de Tema da Interface (Claro / Escuro) | Interface (Tema) | 2 | Baixa | `CT_RF50_Alternância de Tema da Interface.md` |
| **Total** | **50 cenários** | | **254** | | |

\* Prioridade **proposta** pelo responsável do teste com base em criticidade para o negócio (acesso, dinheiro, dados de clientes); pode ser revista com o professor/responsável pelo produto.

### 📊 Resumo por módulo

| Módulo | Cenários | Casos de teste |
|---|:---:|:---:|
| Autenticação | 1 | 4 |
| Página Inicial e Dashboard | 6 | 27 |
| Check-ins, Presenças e Aulas | 3 | 12 |
| Clientes, Matrículas e Avaliações | 3 | 21 |
| Financeiro e Relatórios | 6 | 40 |
| Treinos e Exercícios | 4 | 12 |
| Turmas, Grupos e Box | 4 | 22 |
| Colaboradores, Funções e Cadastros de apoio | 4 | 22 |
| Engajamento (Atividades, Pontuações, Produtos, Enquetes) | 4 | 22 |
| Comercial (Leads, Planos, Contratos, Pagamentos) | 5 | 26 |
| Anamnese | 4 | 18 |
| Inteligência, Automação e Configurações | 4 | 19 |
| Aplicativo e Notificações | 1 | 7 |
| Interface (Tema) | 1 | 2 |
| **Total** | **50** | **254** |


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
| RF01 — Login | C01-CT04 | Link de recuperação de senha: nada acontece ao clicar |
| RF10 — Aulas do SifitBox | CT01–CT04 | Filtro por datas e botão "Gerar aulas" sem efeito visível; data final anterior à inicial não é bloqueada |
| RF11 — Clientes | CT04 | Exclusão retorna "Erro no servidor – Erro interno inesperado" |
| RF12 — Matrículas | CT05 | Exclusão retorna "Erro no servidor – Erro interno inesperado" |
| RF16 — Fichas de treino | CT01, CT02 | Filtros por código/status não retornam registros; cadastro falha com "Erro ao salvar ficha" |
| RF19 — Objetivos de treino | CT01, CT02 | Cadastro falha com "Erro ao salvar objetivo"; busca sem resultados |
| RF33 — Pontuações | CT03, CT06 | "Erro ao salvar pontuação" e "Erro no servidor" em ação da coluna Ações |
| RF35 — Enquetes | CT02–CT04 | "Erro ao salvar enquete" (cadastro e edição) e "Erro ao deletar Enquete" |
| RF40 — Bandeiras de cartão | CT02 | Ao salvar, nada acontece e a lista continua vazia |
| RF41 — Anamnese (aplicação) | CT01, CT02 | "Finalizar Anamnese" sem efeito; "Erro no servidor" ao finalizar |
| RF44 — Perguntas de anamnese | CT02 | Alteração do tipo de resposta retorna "Erro ao salvar pergunta" |
| RF47 — Configurações | CT01–CT07 | Todas as abas retornam erro ao salvar (ex.: "Erro ao salvar configurações") |
| RF48 — Modelos de ficha | CT01 | Cadastro retorna "Erro ao salvar modelo" |

**Erros esperados por integridade referencial** (comportamento correto a validar): RF20-CT05 (grupo com vínculos), RF22-CT06 (categoria Crossfit), RF37-CT04 (plano com vínculos) e RF39-CT05 (tipo de pagamento vinculado).

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
| Renumeração de cenários ao longo do projeto (RF04→RF08, RF09→RF11 etc.) | Baixo | Usar a tabela da seção 10 como referência oficial de IDs |
| Falta de especificação oficial do produto | Médio | Basear o resultado esperado no comportamento lógico e na análise de requisitos |

---

## 📁 15. Entregáveis e Referências

### Documentos do projeto (`Sifit/`)

| Arquivo | Conteúdo | Situação |
|---|---|---|
| `1-Analise de requistos.md` | Requisitos funcionais (RF01–RF50) e não funcionais propostos (RNF01–RNF10) | ✅ Concluído (23/10/2026) |
| `2-Plano de testes.md` | Este documento | ✅ Elaborado |
| `Cenario de Testes/CT_RF01 … CT_RF50` | 50 cenários, 254 casos de teste | ✅ Escritos |
| `3-Relatorio de Bugs.md` | Registro dos defeitos encontrados | ⏳ A preencher |
| `4-Relatorio dos testes.md` | Relatório final de execução | ⏳ A preencher |

### Referências

* **Sistema sob teste:** [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)
* **Repositório:** `Extensao-sifit-qa` (GitHub — Arthur-Miranda-Rodrigues), branch `main`, commits verificados de 08/10/2026 a 23/10/2026
* **Evidências:** gravações de tela hospedadas no Google Drive, linkadas dentro de cada caso de teste
* **Modelo de plano:** plano de testes do OrangeHRM (Demo), usado como base estrutural
* **README do repositório:** metodologia (testes positivos, negativos, exploratório e funcional; formatos BDD, tabelas e checklist)

---

## ✅ 16. Resumo

| Indicador | Valor |
|---|:---:|
| Requisitos funcionais (RF) | 50 |
| Cenários de teste | 50 |
| Casos de teste documentados | 254 |
| Módulos funcionais agrupados | 14 |
| Requisitos não funcionais propostos | 10 |
| Período de elaboração | 08/10/2026 a 24/10/2026 |

