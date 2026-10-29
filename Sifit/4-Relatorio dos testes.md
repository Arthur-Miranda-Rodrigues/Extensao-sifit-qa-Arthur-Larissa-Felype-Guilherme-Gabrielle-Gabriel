# ✅ Relatório Final de Execução de Testes — SIFIT

**Sistema testado:** SIFIT — Sistema de gestão para academia/box  
**Responsável:** Arthur Miranda Rodrigues — RA 14538  
**Data do relatório:** 29/10/2026  
**Ambiente:** Aplicação web de testes  

- **Sistema operacional:** Não especificado de forma única nos artefatos de execução disponíveis.
- **Navegador:** Chrome/Firefox/Brave, conforme ferramentas previstas no plano; versão exata não consolidada.
- **URL:** https://sifitalfa.centrion.com.br
- **Tipo de teste:** Teste funcional manual (caixa-preta).
- **Base:** 50 cenários RF01–RF50 e 254 casos de teste conforme o Plano de Testes.

---

## 📊 Resumo da Execução

| Indicador | Resultado |
|---|---:|
| Cenários documentados | 50 |
| Casos de teste previstos/documentados | 254 |
| Bugs registrados | 23 |
| Bugs de severidade alta | 10 |
| Bugs de severidade média | 10 |
| Bugs de severidade baixa | 3 |
| Casos aprovados | Não consolidado nos arquivos fornecidos |
| Casos reprovados | Não consolidado nos arquivos fornecidos |
| Casos bloqueados | Não consolidado nos arquivos fornecidos |

> **Nota sobre os resultados:** o repositório contém cenários com evidências e um relatório detalhado de 23 defeitos, mas o arquivo `4-Relatorio dos testes.md` estava vazio. Por isso, não é possível afirmar com segurança um total global de casos aprovados, reprovados ou bloqueados. Os números não foram estimados nem inventados.

---

## 🔍 Cobertura por Requisito / Módulo

| Código RF | Módulo / cenário | Casos previstos | Bugs associados |
|---|---|---:|---|
| RF01 | Login na plataforma | 4 | BUG-001 |
| RF02 | Página Inicial (Parte 1) | 5 | — |
| RF03 | Página Inicial (Parte 2) | 5 | — |
| RF04 | Página Inicial (Parte 3) | 5 | — |
| RF05 | Página Inicial (Parte 4) | 5 | — |
| RF06 | Página Inicial (Parte 5) | 4 | — |
| RF07 | Acesso e visualização do Dashboard | 3 | — |
| RF08 | Gerenciamento de Check-ins | 4 | — |
| RF09 | Consulta e Filtragem de Presenças de Clientes | 4 | — |
| RF10 | Gerenciamento de Aulas do SifitBox | 4 | BUG-002, BUG-003, BUG-004 |
| RF11 | Gestão de Clientes | 5 | — |
| RF12 | Gerenciamento de Matrículas | 5 | — |
| RF13 | Gerenciamento de Avaliações Físicas | 11 | — |
| RF14 | Registro e Gestão de Contas a Receber | 6 | — |
| RF15 | Registro de Contas a Pagar | 4 | BUG-010, BUG-021, BUG-022, BUG-023 |
| RF16 | Gerenciamento de Fichas de Treino | 2 | BUG-016 |
| RF17 | Gerenciamento de Exercícios | 3 | — |
| RF18 | Gestão de Grupos Musculares | 5 | BUG-006 |
| RF19 | Gerenciamento de Objetivos Treino | 2 | BUG-017 |
| RF20 | Gestão de Grupos | 5 | — |
| RF21 | Gestão de Turmas | 5 | BUG-018, BUG-019, BUG-020 |
| RF22 | Gestão de Categorias Crossfit | 6 | — |
| RF23 | Gestão de Box – Turmas e Modalidades | 6 | — |
| RF24 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | 7 | — |
| RF25 | Gestão Financeira e Cobranças via Pagar.me no SIFIT | 10 | — |
| RF26 | Gerenciamento e Cadastro de Despesas Fixas | 5 | — |
| RF27 | Geração e Filtragem de Relatórios Operacionais e Financeiros | 8 | — |
| RF28 | Gestão de Colaboradores via Sistema SIFIT | 7 | — |
| RF29 | Gestão de Funções | 5 | — |
| RF30 | Gerenciamento de Fornecedores no SIFIT | 5 | — |
| RF31 | Gerenciamento de Tipos de Documentos no SIFIT | 5 | — |
| RF32 | Gerenciamento de Atividades no SIFIT | 5 | BUG-007 |
| RF33 | Gerenciamento de Pontuações no SIFIT | 8 | BUG-009, BUG-011, BUG-012 |
| RF34 | Gerenciamento de Produtos no SIFIT | 5 | BUG-008 |
| RF35 | Módulo de Enquetes (filtro por Código, Nome e Status) | 4 | BUG-013, BUG-014, BUG-015 |
| RF36 | Gestão e consulta de leads no módulo Prospecção | 5 | — |
| RF37 | Gestão e consulta de planos no sistema SIFIT | 5 | — |
| RF38 | Gestão de Modelos de Contrato no sistema SIFIT | 8 | — |
| RF39 | Gestão de Tipos de Pagamento no Sistema SIFIT | 5 | — |
| RF40 | Gestão de Bandeiras de Cartão (modal de cadastro) | 3 | — |
| RF41 | Aplicação de Fichas de Anamnese no sistema SIFIT | 3 | BUG-005 |
| RF42 | Gerenciamento de Modelos de Anamnese no Sistema SIFIT | 5 | — |
| RF43 | Gerenciamento de Categorias de Anamnese no sistema SIFIT | 5 | — |
| RF44 | Gestão de Pergunta de Anamnese no Sistema SIFIT | 5 | — |
| RF45 | Módulo Inteligência & Automação e Gestão de Clientes | 9 | — |
| RF46 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | 1 | — |
| RF47 | Gestão de configurações | 7 | — |
| RF48 | Gerenciamento de Modelos de Ficha | 2 | — |
| RF49 | Gerenciamento de Notificações | 7 | — |
| RF50 | Alternância de Tema da Interface (Claro / Escuro) | 2 | — |

**Total:** 50 cenários e 254 casos previstos, conforme o Plano de Testes.

---

## 🐞 Resumo dos Bugs Reportados

| ID | Título | Módulo | Severidade | Prioridade | Status |
|---|---|---|---|---|---|
| BUG-001 | Link “Esqueci minha senha” não executa nenhuma ação | Login | Média | Média | Aberto |
| BUG-002 | Botão “Buscar” não filtra as aulas por período (data digitada ou calendário) | SifitBox – Aulas | Alta | Alta | Aberto |
| BUG-003 | Sistema aceita data final anterior à data inicial sem exibir validação | SifitBox – Aulas | Baixa | Média | Aberto |
| BUG-004 | Botão “Gerar aulas” não executa nenhum fluxo | SifitBox – Aulas | Alta | Alta | Aberto |
| BUG-005 | “Finalizar Anamnese” não conclui a ficha | Fichas de Anamnese | Alta | Alta | Aberto |
| BUG-006 | Grupo muscular é cadastrado sem Nome e sem Tipo Membro | Grupos Musculares | Média | Alta | Aberto |
| BUG-007 | Atividade é cadastrada com todos os campos em branco | Atividades | Média | Alta | Aberto |
| BUG-008 | Produto é cadastrado sem nome e sem valor | Produtos | Alta | Alta | Aberto |
| BUG-009 | Pontuação é cadastrada sem datas (período 0000-00-00) | Pontuação | Média | Média | Aberto |
| BUG-010 | Conta a pagar é cadastrada sem Título e sem Local de Pagamento | Contas a Pagar | Média | Média | Aberto |
| BUG-011 | Erro ao salvar a edição de uma pontuação (alteração válida) | Pontuação | Alta | Alta | Aberto |
| BUG-012 | “Erro no servidor” ao acionar ação da coluna Ações em Pontuação | Pontuação | Média | Média | Aberto |
| BUG-013 | Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete” | Enquetes | Alta | Alta | Aberto |
| BUG-014 | Edição de enquete existente retorna “Erro ao salvar enquete” | Enquetes | Alta | Alta | Aberto |
| BUG-015 | Exclusão de enquete retorna “Erro ao deletar Enquete” | Enquetes | Média | Média | Aberto |
| BUG-016 | Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha” | Fichas de Treino | Alta | Alta | Aberto |
| BUG-017 | Cadastro de objetivo de treino retorna “Erro ao salvar objetivo” | Objetivos de Treino | Alta | Alta | Aberto |
| BUG-018 | Campo Status vazio ao abrir “Editar Turma” | Turmas | Média | Média | Aberto |
| BUG-019 | Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não | Turmas | Média | Média | Aberto |
| BUG-020 | Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição | Turmas | Baixa | Baixa | Aberto |
| BUG-021 | Filtro de status (Pago/Vencido) não é aplicado em Contas a Pagar | Contas a Pagar | Média | Alta | Aberto |
| BUG-022 | Totais financeiros incorretos na listagem de Contas a Pagar | Contas a Pagar | Alta | Alta | Aberto |
| BUG-023 | Modal “Visualizar Conta a Pagar” exibe dados sem tratamento | Contas a Pagar | Baixa | Baixa | Aberto |

### 📈 Distribuição por severidade

- 🟥 **Alta:** 10 bugs
- 🟨 **Média:** 10 bugs
- 🟩 **Baixa:** 3 bugs

### 🚨 Principais áreas afetadas

- **Financeiro — Contas a Pagar (RF15):** campos obrigatórios não validados, filtro de status sem efeito, totais incorretos e dados sem tratamento no modal de visualização.
- **Pontuações (RF33):** cadastro com datas inválidas, falha ao editar registro e erro de servidor em ação da listagem.
- **SifitBox — Aulas (RF10):** filtro por período não atualiza os resultados, validação insuficiente de intervalo de datas e botão de geração sem ação.
- **Enquetes (RF35):** falhas no cadastro, edição e exclusão, inclusive com dados válidos.
- **Turmas (RF21):** status não preenchido na edição, erro ao salvar em uma condição específica e modal vazio exibido após edição.
- **Validações de cadastro:** foram observados registros aceitos sem campos que deveriam ser obrigatórios em grupos musculares, atividades e produtos.
- **Fluxos de negócio:** foram reportadas falhas na finalização de anamnese, cadastro de ficha de treino e cadastro de objetivo de treino.

---

## 📹 Evidências e Documentos

- 📋 **Análise de Requisitos:** `1-Analise de requistos.md` — requisitos funcionais RF01–RF50.
- 🧪 **Plano de Testes:** `2-Plano de testes.md` — escopo, critérios, técnicas, cronograma e rastreabilidade.
- 🐛 **Relatório de Bugs:** `3-Relatorio de Bugs.md` — detalhes, passos para reprodução, resultado esperado/obtido e evidências.
- 🎬 **Evidências dos cenários:** links de vídeo/prints registrados nos arquivos de cenário e no relatório de bugs.
- 📄 **Relatório de Execução:** este documento (`4-Relatorio dos testes.md`).

> As evidências estão referenciadas nos documentos de origem. Este relatório não duplica os arquivos de vídeo nem presume que todos os casos tenham evidência individual.

---

## 🔍 Análise de Causa Raiz (Root Cause Analysis)

A causa raiz deve ser confirmada pela equipe técnica após inspeção do código, logs, requisições e dados persistidos. Os registros disponíveis comprovam os sintomas observados durante os testes, mas não demonstram, por si só, a origem técnica definitiva de cada defeito. Assim, os pontos abaixo são **hipóteses para investigação**, não conclusões confirmadas.

| Grupo de defeitos | Hipótese a investigar | Verificação recomendada |
|---|---|---|
| Validações ausentes (BUG-006, 007, 008, 009, 010) | Regras de obrigatoriedade podem não estar aplicadas na interface, no backend ou em ambos. | Tentar reproduzir com DevTools; verificar validação frontend, regras do servidor e restrições do banco. |
| Falhas ao salvar/editar/excluir (BUG-011 a 017, BUG-019) | Possíveis inconsistências na lógica de persistência, no contrato da API ou no tratamento de exceções. | Inspecionar requisições/respostas, logs do servidor, payloads e transações de banco. |
| Filtros e totais incorretos (BUG-002, BUG-021, BUG-022) | A consulta pode ignorar filtros ou calcular/agrupar valores de forma incorreta. | Comparar parâmetros enviados, consulta executada e valores persistidos com o resultado da interface. |
| Ações sem resposta e feedback insuficiente (BUG-001, BUG-004) | Evento de interface, rota ou fluxo de navegação pode não estar conectado à ação esperada. | Verificar eventos, console do navegador, rotas e chamadas de rede. |
| Dados exibidos sem tratamento (BUG-023) | O modal pode estar apresentando diretamente valores técnicos ou sem formatação. | Conferir mapeamento dos dados e regras de formatação antes da apresentação. |

### 🧰 Método sugerido para confirmar a causa

1. Reproduzir o defeito seguindo exatamente os passos registrados.
2. Capturar o estado da interface, console do navegador e requisições de rede.
3. Consultar logs da aplicação e, quando autorizado, verificar os registros persistidos.
4. Aplicar os **5 Porquês** ou um **Diagrama de Ishikawa** quando houver evidência suficiente.
5. Registrar a causa confirmada, correção aplicada e resultado do reteste no relatório de bugs.

---

## ✅ Conclusão

A execução documentada dos testes funcionais do SIFIT identificou **23 defeitos** distribuídos entre os módulos de autenticação, aulas do SifitBox, anamnese, cadastros de apoio, engajamento, fichas/objetivos de treino, turmas e financeiro. A distribuição registrada é de **10 bugs de severidade alta, 10 média e 3 baixa**, indicando que há problemas que podem afetar fluxos operacionais e a confiabilidade dos dados.

Os achados que merecem prioridade incluem falhas em operações financeiras, erros de gravação de dados, ações que não executam o fluxo esperado e validações obrigatórias ausentes. Recomenda-se corrigir primeiro os defeitos de severidade alta, executar retestes direcionados e realizar testes de regressão nos módulos relacionados.

Como o relatório consolidado de execução ainda não possuía os totais por status, **não é possível declarar uma taxa de aprovação geral nem concluir que todos os 254 casos foram executados** apenas com os documentos fornecidos. Para fechar a execução, deve-se preencher o resultado individual de cada caso (Passou/Falhou/Bloqueado/Não executado), vincular a evidência e atualizar os totais.

### 📌 Critérios recomendados para encerramento

- [ ] Registrar o status individual dos 254 casos previstos.
- [ ] Garantir que cada falha tenha bug associado ou justificativa documentada.
- [ ] Retestar os 23 bugs após as correções.
- [ ] Executar regressão nos módulos impactados.
- [ ] Atualizar severidade/status dos bugs conforme os resultados do reteste.
- [ ] Consolidar os totais finais de aprovados, reprovados, bloqueados e não executados.

---

**Documento elaborado com base nos arquivos do projeto SIFIT fornecidos no repositório de QA.**

