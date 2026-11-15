# ✅ **Relatório Final de Execução de Testes - SIFIT**

**Sistema testado:** SIFIT — Sistema de gestão para academia/box

**Responsável:**

* Arthur Miranda Rodrigues — RA 14538
* Larissa Fernanda O. — RA 14536
* Felype Augusto Dos Santos Silva — RA 14537
* Guilherme Felipe de Morais — RA 5608
* Gabrielle Bonini Barbosa — RA 14506
* Gabriel de Abreu da Silva — RA 14525

**Data de execução:** 08/10/2026

**Data do relatório:** 08/11/2026 (atualização da versão de 29/10/2026)

**Ambiente:** Aplicação web de testes

* Sistema operacional: não especificado de forma única nos artefatos de execução disponíveis.
* Navegador: Chrome/Firefox/Brave, conforme ferramentas previstas no plano; versão exata não consolidada.
* URL: [https://sifitalfa.centrion.com.br].

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Bugs Registrados |
| ----------------------- | -------------- | -------------- | ---------------- |
| 254  | 217 | 37 | 37 |

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s) |
| --------- | ------ | :------------: | :------------: | :--------------: | ------------------- |
| RF01 | Login na plataforma | 3 | 3 | 1 | BUG-001 |
| RF02 | Página Inicial (Parte 1) | 5 | 5 | 0 | - |
| RF03 | Página Inicial (Parte 2) | 5 | 5 | 0 | - |
| RF04 | Página Inicial (Parte 3) | 5 | 5 | 0 | - |
| RF05 | Página Inicial (Parte 4) | 5 | 5 | 0 | - |
| RF06 | Página Inicial (Parte 5) | 4 | 4 | 0 | - |
| RF07 | Acesso e visualização do Dashboard | 3 | 3 | 1 | BUG-022 |
| RF08 | Gerenciamento de Check-ins | 4 | 4 | 0 | - |
| RF09 | Consulta e Filtragem de Presenças de Clientes | 4 | 4 | 0 | - |
| RF10 | Gestão de Clientes | 4 | 4 | 1 | BUG-025 |
| RF11 | Gerenciamento de Matrículas | 4 | 4 | 1 | BUG-026 |
| RF12 | Gerenciamento de Avaliações Físicas | 11 | 11 | 0 | - |
| RF13 | Registro e Gestão de Contas a Receber | 6 | 6 | 0 | - |
| RF14 | Registro de Contas a Pagar | 1 | 1 | 3 | BUG-010, BUG-021, BUG-024 |
| RF15 | Gerenciamento de Fichas de Treino | 1 | 1 | 1 | BUG-016 |
| RF16 | Gerenciamento de Exercícios | 3 | 3 | 0 | - |
| RF17 | Gestão de Grupos Musculares | 4 | 4 | 1 | BUG-006 |
| RF18 | Gerenciamento de Objetivos Treino | 1 | 1 | 1 | BUG-017 |
| RF19 | Gestão de Grupos | 5 | 5 | 0 | - |
| RF20 | Gestão de Turmas | 4 | 4 | 3 | BUG-018, BUG-019, BUG-020 |
| RF21 | Gestão de Categorias Crossfit | 6 | 6 | 0 | - |
| RF22 | Gestão de Box (Turmas e Modalidades) | 6 | 6 | 0 | - |
| RF23 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | 5 | 5 | 1 | BUG-027 |
| RF24 | Gestão Financeira e Cobranças via Pagar.me | 10 | 10 | 0 | - |
| RF25 | Gerenciamento e Cadastro de Despesas Fixas | 5 | 5 | 0 | - |
| RF26 | Geração e Filtragem de Relatórios Operacionais e Financeiros | 8 | 8 | 0 | - |
| RF27 | Gestão de Colaboradores via Sistema SIFIT | 7 | 7 | 0 | - |
| RF28 | Gestão de Funções | 5 | 5 | 0 | - |
| RF29 | Gerenciamento de Fornecedores | 5 | 5 | 0 | - |
| RF30 | Gerenciamento de Tipos de Documentos | 5 | 5 | 0 | - |
| RF31 | Gerenciamento de Atividades | 4 | 4 | 1 | BUG-007 |
| RF32 | Gerenciamento de Pontuações | 5 | 5 | 3 | BUG-009, BUG-011, BUG-012 |
| RF33 | Gerenciamento de Produtos | 4 | 4 | 1 | BUG-008 |
| RF34 | Módulo de Enquetes | 1 | 1 | 3 | BUG-013, BUG-014, BUG-015 |
| RF35 | Gestão e consulta de leads no módulo Prospecção | 5 | 5 | 0 | - |
| RF36 | Gestão e consulta de planos | 5 | 5 | 0 | - |
| RF37 | Gestão de Modelos de Contrato | 7 | 7 | 1 | BUG-023 |
| RF38 | Gestão de Tipos de Pagamento | 5 | 5 | 0 | - |
| RF39 | Gestão de Bandeiras de Cartão | 2 | 2 | 1 | BUG-028 |
| RF40 | Aplicação de Fichas de Anamnese | 1 | 1 | 1 | BUG-005 |
| RF41 | Gerenciamento de Modelos de Anamnese | 5 | 5 | 0 | - |
| RF42 | Gerenciamento de Categorias de Anamnese | 5 | 5 | 0 | - |
| RF43 | Gestão de Pergunta de Anamnese | 4 | 4 | 1 | BUG-029 |
| RF44 | Módulo Inteligência & Automação e Gestão de Clientes | 9 | 9 | 0 | - |
| RF45 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | 1 | 1 | 0 | - |
| RF46 | Gerenciamento de Modelos de Ficha | 1 | 1 | 1 | BUG-037 |
| RF47 | Gerenciamento de Notificações | 7 | 7 | 0 | - |
| RF48 | Alternância de Tema da Interface (Claro / Escuro) | 2 | 2 | 0 | - |
| — | Gerenciamento de Aulas do SifitBox *(sem arquivo na pasta)* | 0 | 0 | 3 | BUG-002, BUG-003, BUG-004 |
| — | Gestão de configurações *(sem arquivo na pasta)* | 0 | 0 | 7 | BUG-030, BUG-031, BUG-032, BUG-033, BUG-034, BUG-035, BUG-036 |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID | Título | Caso de teste (numeração atual) | Severidade | Prioridade | Status |
| -- | ------ | ------------------------------- | ---------- | ---------- | ------ |
| BUG-001 | Link “Esqueci minha senha” não executa nenhuma ação | C01-CT04 | Média | Média | Aberto |
| BUG-002 | Botão “Buscar” não filtra as aulas por período (data digitada ou calendário) | SifitBox-CT01, CT02* | Alta | Alta | Aberto |
| BUG-003 | Sistema aceita data final anterior à data inicial sem exibir validação | SifitBox-CT03* | Baixa | Média | Aberto |
| BUG-004 | Botão “Gerar aulas” não executa nenhum fluxo | SifitBox-CT04* | Alta | Alta | Aberto |
| BUG-005 | “Finalizar Anamnese” não conclui a ficha | C40-CT01, C40-CT02 | Alta | Alta | Aberto |
| BUG-006 | Grupo muscular é cadastrado sem Nome e sem Tipo Membro | C17-CT04 | Média | Alta | Aberto |
| BUG-007 | Atividade é cadastrada com todos os campos em branco | C31-CT03 | Média | Alta | Aberto |
| BUG-008 | Produto é cadastrado sem nome e sem valor | C33-CT05 | Alta | Alta | Aberto |
| BUG-009 | Pontuação é cadastrada sem datas (período 0000-00-00) | C32-CT08 | Média | Média | Aberto |
| BUG-010 | Conta a pagar é cadastrada sem Título e sem Local de Pagamento | C14-CT01 | Média | Média | Aberto |
| BUG-011 | Erro ao salvar a edição de uma pontuação (alteração válida) | C32-CT03 | Alta | Alta | Aberto |
| BUG-012 | “Erro no servidor” ao acionar ação da coluna Ações em Pontuação | C32-CT06 | Média | Média | Aberto |
| BUG-013 | Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete” | C34-CT02 | Alta | Alta | Aberto |
| BUG-014 | Edição de enquete existente retorna “Erro ao salvar enquete” | C34-CT03 | Alta | Alta | Aberto |
| BUG-015 | Exclusão de enquete retorna “Erro ao deletar Enquete” | C34-CT04 | Média | Média | Aberto |
| BUG-016 | Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha” | C15-CT02 | Alta | Alta | Aberto |
| BUG-017 | Cadastro de objetivo de treino retorna “Erro ao salvar objetivo” | C18-CT01 | Alta | Alta | Aberto |
| BUG-018 | Campo Status vazio ao abrir “Editar Turma” | C20-CT04 | Média | Média | Aberto |
| BUG-019 | Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não | C20-CT04 | Média | Média | Aberto |
| BUG-020 | Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição | C20-CT04 | Baixa | Baixa | Aberto |
| BUG-021 | Modal “Visualizar Conta a Pagar” exibe dados sem tratamento | C14-CT03 | Baixa | Baixa | Aberto |
| BUG-022 | Baixo contraste nos títulos e informações dos gráficos do Dashboard | C07-CT04 | Média | Média | Aberto |
| BUG-023 | Erro ao salvar modelo de contrato (listagem permanece em branco) | C37-CT08 | Alta | Alta | Aberto |
| BUG-024 | Filtro de status (Vencido/Pago) não é aplicado em Contas a Pagar | C14-CT02 | Média | Alta | Aberto |
| BUG-025 | Exclusão de cliente retorna “Erro no servidor – Erro interno inesperado” | C10-CT04 | Média | Média | Aberto |
| BUG-026 | Exclusão de matrícula retorna “Erro no servidor – Erro interno inesperado” | C11-CT05 | Média | Média | Aberto |
| BUG-027 | Busca de contas no fechamento de caixa retorna “Erro ao buscar contas” | C23-CT06 | Média | Média | Aberto |
| BUG-028 | Cadastro de bandeira de cartão não salva e a listagem continua vazia | C39-CT02 | Alta | Alta | Aberto |
| BUG-029 | Edição do tipo de resposta de pergunta de anamnese retorna “Erro ao salvar pergunta” | C43-CT02 | Alta | Alta | Aberto |
| BUG-030 | Erro ao salvar configurações gerais na aba Home | C46-CT01 | Alta | Alta | Aberto |
| BUG-031 | Erro ao salvar configurações de biometria e catraca | C46-CT02 | Alta | Alta | Aberto |
| BUG-032 | Erro ao salvar parâmetros de avaliação física nas configurações | C46-CT03 | Alta | Alta | Aberto |
| BUG-033 | Erro ao salvar mensagens automáticas de aniversário nas configurações | C46-CT04 | Média | Média | Aberto |
| BUG-034 | Erro ao salvar pagamento online e token de integração nas configurações | C46-CT05 | Alta | Alta | Aberto |
| BUG-035 | Erro de conectividade/servidor ao salvar integração com WhatsApp nas configurações | C46-CT06 | Média | Média | Aberto |
| BUG-036 | Erro ao salvar identidade visual (cores, logotipo e capa) nas configurações | C46-CT07 | Média | Média | Aberto |
| BUG-037 | Cadastro de modelo de ficha retorna “Erro ao salvar modelo” | C47-CT01 | Alta | Alta | Aberto |

\* Casos do cenário SifitBox – Aulas e do Gestão de configurações, que não possui arquivo na pasta de cenários.

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 217
* ❌ Falharam: 37

**Severidade dos bugs:**

* 🟥 Alta: 17
* 🟨 Média: 17
* 🟩 Baixa: 3

---

## 📁 **Evidências e Documentos**

* ✔️ [Análise de Requisitos (Markdown)]
* ✔️ [Plano de Testes (Markdown)]
* ✔️ [Casos de Teste (Markdown)]
* 🐛 [Relatório de Bugs com Evidências em Vídeo] 
* 📹 Evidências em vídeo/prints hospedadas no Google Drive e no Jam.dev, linkadas nos arquivos de cenário e no relatório de bugs

---

## ✅ **Conclusão**

A execução documentada dos testes funcionais do SIFIT identificou **37 defeitos** distribuídos entre os módulos de autenticação, aulas do SifitBox, anamnese, cadastros de apoio, engajamento, fichas/objetivos de treino, turmas, modelos de contrato e de ficha, bandeiras de cartão, configurações, dashboard e financeiro. A distribuição registrada é de **17 bugs de severidade alta, 17 média e 3 baixa**, indicando que há problemas que podem afetar fluxos operacionais e a confiabilidade dos dados.

Os achados que merecem prioridade incluem falhas de gravação (configurações do sistema em todas as abas, enquetes, pontuações, fichas e objetivos de treino, modelos de contrato e de ficha, bandeiras de cartão), ações que não executam o fluxo esperado (Aulas do SifitBox, anamnese) e validações obrigatórias ausentes em vários cadastros. Recomenda-se corrigir primeiro os defeitos de severidade alta, executar retestes direcionados e realizar testes de regressão nos módulos relacionados.
