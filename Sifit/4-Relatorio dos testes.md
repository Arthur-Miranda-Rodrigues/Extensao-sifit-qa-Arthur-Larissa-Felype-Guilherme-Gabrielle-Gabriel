# ✅ Relatório Final de Execução de Testes — SIFIT

**Sistema testado:** SIFIT — Sistema de gestão para academia/box  
**Responsável:** 
Arthur Miranda Rodrigues — RA 14538  
Larissa Fernanda O. RA:14536
Felype Augusto Dos Santos Silva 
RA: 14537
Guilherme: Guilherme Felipe de Morais 
RA: 5608
Gabrielle Bonini Barbosa 
RA: 14506
Gabriel de Abreu da Silva — RA 14525
**Data do relatório:** 08/11/2026 (atualização da versão de 29/10/2026)  
**Ambiente:** Aplicação web de testes  

- **Sistema operacional:** Não especificado de forma única nos artefatos de execução disponíveis.
- **Navegador:** Chrome/Firefox/Brave, conforme ferramentas previstas no plano; versão exata não consolidada.
- **URL:** https://sifitalfa.centrion.com.br
- **Tipo de teste:** Teste funcional manual (caixa-preta).
- **Base:** 49 cenários (RF01–RF49) e 232 casos de teste presentes na pasta `Cenario de Testes`, mais 22 casos registrados apenas no Relatório de Bugs (18 em cenários da pasta e 4 do cenário de Aulas do SifitBox, sem arquivo), conforme o Plano de Testes.

---

## 📊 Resumo da Execução

| Indicador | Resultado |
|---|---:|
| Cenários documentados (arquivos na pasta) | 49 |
| Casos de teste na pasta | 232 |
| Casos registrados apenas no Relatório de Bugs | 22 |
| Total de casos documentados (pasta + Relatório de Bugs) | 254 |
| Bugs registrados | 24 |
| Bugs de severidade alta | 10 |
| Bugs de severidade média | 11 |
| Bugs de severidade baixa | 3 |
| Casos aprovados | Não consolidado nos arquivos fornecidos |
| Casos reprovados | Não consolidado nos arquivos fornecidos |
| Casos bloqueados | Não consolidado nos arquivos fornecidos |

> **Nota sobre os resultados:** os cenários da pasta não trazem um campo de status (Passou/Falhou) por caso e o Relatório de Bugs lista 24 defeitos. Por isso não é possível afirmar com segurança um total global de casos aprovados, reprovados ou bloqueados. Os números não foram estimados nem inventados. A contagem de 254 casos é a soma dos casos presentes na pasta com os 22 que, pela comparação com o Plano de Testes anterior (254 casos), hoje constam apenas no Relatório de Bugs.

---

## 🔍 Cobertura por Requisito / Módulo

| Código RF | Módulo / cenário | Casos na pasta | Bugs associados |
|---|---|---:|---|
| RF01 | Login na plataforma | 3 | BUG-001 |
| RF02 | Página Inicial (Parte 1) | 5 | — |
| RF03 | Página Inicial (Parte 2) | 5 | — |
| RF04 | Página Inicial (Parte 3) | 5 | — |
| RF05 | Página Inicial (Parte 4) | 5 | — |
| RF06 | Página Inicial (Parte 5) | 4 | — |
| RF07 | Acesso e visualização do Dashboard | 3 | BUG-022 |
| RF08 | Gerenciamento de Check-ins | 4 | — |
| RF09 | Consulta e Filtragem de Presenças de Clientes | 4 | — |
| RF10 | Gestão de Clientes | 5 | — |
| RF11 | Gerenciamento de Matrículas | 5 | — |
| RF12 | Gerenciamento de Avaliações Físicas | 11 | — |
| RF13 | Registro e Gestão de Contas a Receber | 6 | — |
| RF14 | Registro de Contas a Pagar | 1 | BUG-010, BUG-021, BUG-024 |
| RF15 | Gerenciamento de Fichas de Treino | 1 | BUG-016 |
| RF16 | Gerenciamento de Exercícios | 3 | — |
| RF17 | Gestão de Grupos Musculares | 4 | BUG-006 |
| RF18 | Gerenciamento de Objetivos Treino | 1 | BUG-017 |
| RF19 | Gestão de Grupos | 5 | — |
| RF20 | Gestão de Turmas | 4 | BUG-018, BUG-019, BUG-020 |
| RF21 | Gestão de Categorias Crossfit | 6 | — |
| RF22 | Gestão de Box (Turmas e Modalidades) | 6 | — |
| RF23 | Gerenciamento e Filtro de Caixas no Módulo Financeiro | 7 | — |
| RF24 | Gestão Financeira e Cobranças via Pagar.me no SIFIT | 10 | — |
| RF25 | Gerenciamento e Cadastro de Despesas Fixas | 5 | — |
| RF26 | Geração e Filtragem de Relatórios Operacionais e Financeiros | 8 | — |
| RF27 | Gestão de Colaboradores via Sistema SIFIT | 7 | — |
| RF28 | Gestão de Funções | 5 | — |
| RF29 | Gerenciamento de Fornecedores no SIFIT | 5 | — |
| RF30 | Gerenciamento de Tipos de Documentos no SIFIT | 5 | — |
| RF31 | Gerenciamento de Atividades no SIFIT | 4 | BUG-007 |
| RF32 | Gerenciamento de Pontuações no SIFIT | 5 | BUG-009, BUG-011, BUG-012 |
| RF33 | Gerenciamento de Produtos no SIFIT | 4 | BUG-008 |
| RF34 | Módulo de Enquetes | 2 | BUG-013, BUG-014, BUG-015 |
| RF35 | Gestão e consulta de leads no módulo Prospecção | 5 | — |
| RF36 | Gestão e consulta de planos no sistema SIFIT | 5 | — |
| RF37 | Gestão de Modelos de Contrato no sistema SIFIT | 7 | BUG-023 |
| RF38 | Gestão de Tipos de Pagamento no Sistema SIFIT | 5 | — |
| RF39 | Gestão de Bandeiras de Cartão no Sistema SIFIT | 3 | — |
| RF40 | Aplicação de Fichas de Anamnese no sistema SIFIT | 1 | BUG-005 |
| RF41 | Gerenciamento de Modelos de Anamnese no Sistema SIFIT | 5 | — |
| RF42 | Gerenciamento de Categorias de Anamnese no sistema SIFIT | 5 | — |
| RF43 | Gestão de Pergunta de Anamnese no Sistema SIFIT | 5 | — |
| RF44 | Módulo Inteligência & Automação e Gestão de Clientes | 9 | — |
| RF45 | Visualização e Filtragem do Dashboard de Resultados da Inteligência | 1 | — |
| RF46 | Gestão de configurações | 7 | — |
| RF47 | Gerenciamento de Modelos de Ficha | 2 | — |
| RF48 | Gerenciamento de Notificações | 7 | — |
| RF49 | Alternância de Tema da Interface (Claro / Escuro) | 2 | — |
| — | Gerenciamento de Aulas do SifitBox *(sem arquivo na pasta)* | 0 | BUG-002, BUG-003, BUG-004 |

**Total:** 49 cenários com 232 casos na pasta. O cenário de Aulas do SifitBox aparece apenas como referência dos bugs BUG-002 a BUG-004, pois não possui arquivo em `Cenario de Testes`.

---

## 🐞 Resumo dos Bugs Reportados

| ID | Título | Módulo | Caso de teste (numeração atual) | Severidade | Prioridade | Status |
|---|---|---|---|---|---|---|
| BUG-001 | Link “Esqueci minha senha” não executa nenhuma ação | Login | C01-CT04 | Média | Média | Aberto |
| BUG-002 | Botão “Buscar” não filtra as aulas por período (data digitada ou calendário) | SifitBox – Aulas | C10-CT01, C10-CT02* | Alta | Alta | Aberto |
| BUG-003 | Sistema aceita data final anterior à data inicial sem exibir validação | SifitBox – Aulas | C10-CT03* | Baixa | Média | Aberto |
| BUG-004 | Botão “Gerar aulas” não executa nenhum fluxo | SifitBox – Aulas | C10-CT04* | Alta | Alta | Aberto |
| BUG-005 | “Finalizar Anamnese” não conclui a ficha | Fichas de Anamnese | C40-CT01, C40-CT02 | Alta | Alta | Aberto |
| BUG-006 | Grupo muscular é cadastrado sem Nome e sem Tipo Membro | Grupos Musculares | C17-CT04 | Média | Alta | Aberto |
| BUG-007 | Atividade é cadastrada com todos os campos em branco | Atividades | C31-CT03 | Média | Alta | Aberto |
| BUG-008 | Produto é cadastrado sem nome e sem valor | Produtos | C33-CT05 | Alta | Alta | Aberto |
| BUG-009 | Pontuação é cadastrada sem datas (período 0000-00-00) | Pontuação | C32-CT08 | Média | Média | Aberto |
| BUG-010 | Conta a pagar é cadastrada sem Título e sem Local de Pagamento | Contas a Pagar | C14-CT01 | Média | Média | Aberto |
| BUG-011 | Erro ao salvar a edição de uma pontuação (alteração válida) | Pontuação | C32-CT03 | Alta | Alta | Aberto |
| BUG-012 | “Erro no servidor” ao acionar ação da coluna Ações em Pontuação | Pontuação | C32-CT06 | Média | Média | Aberto |
| BUG-013 | Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete” | Enquetes | C34-CT02 | Alta | Alta | Aberto |
| BUG-014 | Edição de enquete existente retorna “Erro ao salvar enquete” | Enquetes | C34-CT03 | Alta | Alta | Aberto |
| BUG-015 | Exclusão de enquete retorna “Erro ao deletar Enquete” | Enquetes | C34-CT04 | Média | Média | Aberto |
| BUG-016 | Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha” | Fichas de Treino | C15-CT02 | Alta | Alta | Aberto |
| BUG-017 | Cadastro de objetivo de treino retorna “Erro ao salvar objetivo” | Objetivos de Treino | C18-CT01 | Alta | Alta | Aberto |
| BUG-018 | Campo Status vazio ao abrir “Editar Turma” | Turmas | C20-CT04 | Média | Média | Aberto |
| BUG-019 | Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não | Turmas | C20-CT04 | Média | Média | Aberto |
| BUG-020 | Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição | Turmas | C20-CT04 | Baixa | Baixa | Aberto |
| BUG-021 | Modal “Visualizar Conta a Pagar” exibe dados sem tratamento | Contas a Pagar | C14-CT03 | Baixa | Baixa | Aberto |
| BUG-022 | Baixo contraste nos títulos e informações dos gráficos do Dashboard | Dashboard | C07-CT01 | Média | Média | Aberto |
| BUG-023 | Erro ao salvar modelo de contrato (listagem permanece em branco) | Modelos de Contrato | C37-CT08 | Alta | Alta | Aberto |
| BUG-024 | Filtro de status (Vencido/Pago) não é aplicado em Contas a Pagar | Contas a Pagar | C14-CT02 | Média | Alta | Aberto |

\* Os casos do SifitBox – Aulas seguem a numeração antiga (C10), que hoje pertence ao cenário de Gestão de Clientes. Os demais casos foram convertidos para a numeração atual dos arquivos (o Relatório de Bugs ainda cita parte deles pela numeração anterior, por exemplo C21-CT04 = C20-CT04 atual). O BUG-022 cita C02-CT01 no relatório de bugs, mas o Dashboard corresponde ao cenário RF07.

### 📈 Distribuição por severidade

- 🟥 **Alta:** 10 bugs
- 🟨 **Média:** 11 bugs
- 🟩 **Baixa:** 3 bugs

### 🚨 Principais áreas afetadas

- **Financeiro — Contas a Pagar (RF14):** 3 bugs — conta cadastrada sem campos obrigatórios (BUG-010), modal de visualização com dados sem tratamento (BUG-021) e filtro de status sem efeito (BUG-024).
- **Pontuações (RF32):** 3 bugs — cadastro com datas inválidas (BUG-009), falha ao editar registro (BUG-011) e erro de servidor em ação da listagem (BUG-012).
- **SifitBox — Aulas:** 3 bugs — filtro por período não atualiza os resultados (BUG-002), validação insuficiente de intervalo de datas (BUG-003) e botão “Gerar aulas” sem ação (BUG-004).
- **Enquetes (RF34):** 3 bugs — falhas no cadastro, edição e exclusão, inclusive com dados válidos (BUG-013 a BUG-015).
- **Turmas (RF20):** 3 bugs — status não preenchido na edição, erro ao salvar em uma condição específica e modal vazio exibido após edição (BUG-018 a BUG-020).
- **Validações de cadastro:** registros aceitos sem campos que deveriam ser obrigatórios em grupos musculares (BUG-006), atividades (BUG-007), produtos (BUG-008), pontuações (BUG-009) e contas a pagar (BUG-010).
- **Fluxos de negócio:** falhas na finalização de anamnese (BUG-005), no cadastro de ficha de treino (BUG-016), no cadastro de objetivo de treino (BUG-017) e no salvamento de modelo de contrato (BUG-023).
- **Interface e acesso:** link de recuperação de senha sem ação (BUG-001) e baixo contraste nos gráficos do Dashboard (BUG-022).

---

## 📹 Evidências e Documentos

- 📋 **Análise de Requisitos:** `1-Analise de requistos.md` — requisitos funcionais RF01–RF49.
- 🧪 **Plano de Testes:** `2-Plano de testes.md` — escopo, critérios, técnicas, cronograma e rastreabilidade.
- 🐛 **Relatório de Bugs:** `3-Relatorio de Bugs.md` — 24 bugs, com passos para reprodução, resultado esperado/obtido e evidências.
- 🎬 **Evidências dos cenários:** links de vídeo/prints registrados nos arquivos de cenário e no relatório de bugs.
- 📄 **Relatório de Execução:** este documento (`4-Relatorio dos testes.md`).

> As evidências estão referenciadas nos documentos de origem. Este relatório não duplica os arquivos de vídeo nem presume que todos os casos tenham evidência individual.

---

## 🔍 Análise de Causa Raiz (Root Cause Analysis)

A causa raiz deve ser confirmada pela equipe técnica após inspeção do código, logs, requisições e dados persistidos. Os registros disponíveis comprovam os sintomas observados durante os testes, mas não demonstram, por si só, a origem técnica definitiva de cada defeito. Assim, os pontos abaixo são **hipóteses para investigação**, não conclusões confirmadas.

| Grupo de defeitos | Hipótese a investigar | Verificação recomendada |
|---|---|---|
| Validações ausentes (BUG-006, 007, 008, 009, 010) | Regras de obrigatoriedade podem não estar aplicadas na interface, no backend ou em ambos. | Tentar reproduzir com DevTools; verificar validação frontend, regras do servidor e restrições do banco. |
| Falhas ao salvar/editar/excluir (BUG-005, 011 a 017, 019, 023) | Possíveis inconsistências na lógica de persistência, no contrato da API ou no tratamento de exceções. | Inspecionar requisições/respostas, logs do servidor, payloads e transações de banco. |
| Filtros que não atualizam resultados (BUG-002, 024) e validação de período (BUG-003) | A consulta pode ignorar filtros ou o componente pode não enviar os parâmetros informados. | Comparar parâmetros enviados, consulta executada e resultado exibido na interface. |
| Ações sem resposta e feedback insuficiente (BUG-001, 004) | Evento de interface, rota ou fluxo de navegação pode não estar conectado à ação esperada. | Verificar eventos, console do navegador, rotas e chamadas de rede. |
| Dados e telas sem tratamento visual (BUG-018, 020, 021, 022) | Valores técnicos exibidos sem formatação, campos não preenchidos ao abrir a edição e estilos com contraste insuficiente. | Conferir mapeamento dos dados, regras de formatação e tokens de cor antes da apresentação. |

### 🧰 Método sugerido para confirmar a causa

1. Reproduzir o defeito seguindo exatamente os passos registrados.
2. Capturar o estado da interface, console do navegador e requisições de rede.
3. Consultar logs da aplicação e, quando autorizado, verificar os registros persistidos.
4. Aplicar os **5 Porquês** ou um **Diagrama de Ishikawa** quando houver evidência suficiente.
5. Registrar a causa confirmada, correção aplicada e resultado do reteste no relatório de bugs.

---

## ✅ Conclusão

A execução documentada dos testes funcionais do SIFIT identificou **24 defeitos** distribuídos entre os módulos de autenticação, aulas do SifitBox, anamnese, cadastros de apoio, engajamento, fichas/objetivos de treino, turmas, modelos de contrato, dashboard e financeiro. A distribuição registrada é de **10 bugs de severidade alta, 11 média e 3 baixa**, indicando que há problemas que podem afetar fluxos operacionais e a confiabilidade dos dados.

Os achados que merecem prioridade incluem falhas de gravação (enquetes, pontuações, fichas e objetivos de treino, modelo de contrato), ações que não executam o fluxo esperado (Aulas do SifitBox, anamnese) e validações obrigatórias ausentes em vários cadastros. Recomenda-se corrigir primeiro os defeitos de severidade alta, executar retestes direcionados e realizar testes de regressão nos módulos relacionados.

