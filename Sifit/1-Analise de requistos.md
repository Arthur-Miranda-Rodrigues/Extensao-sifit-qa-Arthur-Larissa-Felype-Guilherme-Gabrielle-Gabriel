# 📋 **Análise de Requisitos — SIFIT**

🏋️ **Projeto:** SIFIT — Sistema de gestão para academia/box  
📄 **Documento:** Análise de Requisitos Funcionais e Não Funcionais  
🧪 **Base de elaboração:** 49 arquivos de cenários de teste (`CT_RF01` a `CT_RF49`), com 232 casos de teste, fornecidos no projeto de QA do SIFIT  
👨‍💻 **Responsável pelo trabalho:** Arthur Miranda Rodrigues, Larissa Fernanda O., Felype Augusto Dos Santos Silva, Guilherme Felipe de Morais, Gabrielle Bonini Barbosa, Gabriel de Abreu da Silva  
🔖 **Versão:** 2.1  
📅 **Data:** 08/11/2026  

---

## 🎯 1. Objetivo

Este documento consolida os requisitos funcionais identificados nos 49 cenários de teste do SIFIT presentes na pasta `Sifit/Cenario de Testes/`. Cada requisito foi detalhado e correlacionado diretamente a partir do objetivo dos casos de teste existentes, preservando a rastreabilidade, os módulos, os fluxos e os comportamentos observados nos arquivos de origem.

---

## 🧭 2. Escopo

A análise contempla autenticação, página inicial e dashboard, check-ins e presenças, clientes, matrículas, avaliações físicas, contas a receber, contas a pagar, fichas de treino, exercícios, grupos musculares, objetivos de treino, grupos financeiro/administrativos, turmas, categorias CrossFit, turmas do box, caixas e fechamentos, integração Pagar.me, despesas fixas, relatórios operacionais e financeiros, colaboradores, funções e permissões, fornecedores, tipos de documentos, atividades, pontuações e programas de fidelidade, produtos, enquetes, prospecção e leads, planos, modelos de contrato, tipos de pagamento, bandeiras de cartão, fichas/modelos/categorias/perguntas de anamnese, inteligência e retenção, configurações gerais, modelos de ficha, notificações/conteúdos do aplicativo e alternância de temas.

---

## 📝 3. Convenções

- **RFxx:** Requisito Funcional associado ao cenário de teste de mesmo número (RF01–RF49 ↔ `CT_RF01`–`CT_RF49`).
- **CT:** Referência ao caso de teste específico descrito no arquivo de origem (ex.: `C01-CT01`).
- **Comportamento observado no teste:** Registros onde o teste evidencia validação de erros de preenchimento, limitações de interface ou falhas tratadas pelo sistema.
- Os requisitos listados abaixo refletem os casos de teste **presentes hoje nos arquivos da pasta**. Casos que constam apenas no `3-Relatorio de Bugs.md` (por exemplo, `C01-CT04`) e o cenário de Aulas do SifitBox, que não possui arquivo na pasta, não aparecem nesta lista (ver seção 8).

---

## 📦 4. Requisitos Funcionais


---

### 🧩 RF01 — Login na plataforma

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C01-CT01:** O login será realizado com um nome de usuário e uma senha válidos na plataforma SIFIT.
- **🧪 C01-CT02:** O login falhará quando o nome de usuário ou a senha forem inválidos.
- **🧪 C01-CT03:** O login falhará quando os campos de login e senha forem apagados ou mantidos em branco.

📎 **Fonte:** `CT_RF01_Login na plataforma.md`

---

### 🧩 RF02 — Página Inicial (Parte 1)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C02-CT01:** Validar a abertura e a busca por nome de alunos no modal de "Clientes Sem Matrículas" a partir da Página Inicial.
- **🧪 C02-CT02:** Validar a consulta detalhada de alunos sumidos ou ausentes há mais tempo na academia.
- **🧪 C02-CT03:** Validar o redirecionamento direto da Página Inicial para a tela de gestão de Avaliações físicas.
- **🧪 C02-CT04:** Validar a exibição do modal de mensalidades pendentes e a alternância de atalhos por período de atraso.
- **🧪 C02-CT05:** Validar a abertura do Radar de Evasão e a visualização das regras de pontuação/risco de cancelamento do aluno.

📎 **Fonte:** `CT_RF02_Acesso A Pagina Inicial Parte 1.md`

---

### 🧩 RF03 — Página Inicial (Parte 2)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C03-CT01:** Verificar se o modal/painel de "Mensalidades pendentes / Financeiro em Aberto" abre corretamente ao clicar em "Ver detalhes" e se os filtros por período de vencimento funcionam adequadamente.
- **🧪 C03-CT02:** Validar a exibição do modal de "Desistências no Período" ao clicar no card correspondente e testar a busca por nome ou código.
- **🧪 C03-CT03:** Validar a abertura e o funcionamento da pesquisa no modal "Matrículas no Período" a partir do card do Dashboard.
- **🧪 C03-CT04:** Verificar se a modalidade/card de "Personais" abre a lista de profissionais cadastrados e permite a busca individualizada.
- **🧪 C03-CT05:** Validar a expansão do modal "Agenda de hoje" ao clicar em "Ver agenda", a busca por aulas, a seleção de unidades e a alteração dinâmica de detalhes ao selecionar aulas como *Turma dos Bodybuilders*, *Teste* e *Horario da manhã*, disponibilizando os botões de ações rápidas.

📎 **Fonte:** `CT_RF03_Acesso A Pagina Inicial Parte 2.md`

---

### 🧩 RF04 — Página Inicial (Parte 3)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C04-CT01:** Validar a abertura do modal "Falar com inativos" a partir da seção "Ações recomendadas para hoje", a busca por alunos, personalização de mensagem e seleção do canal de envio.
- **🧪 C04-CT02:** Verificar a funcionalidade do card "Cobrar alunos", validando a abertura do modal de cobrança, busca por alunos inadimplentes e personalização da mensagem de cobrança segura.
- **🧪 C04-CT03:** Validar o redirecionamento ao clicar em "Ver todos" na seção "Aniversariantes do dia" e a filtragem no modal por período (7 dias, 33 dias) e navegação mensal no calendário.
- **🧪 C04-CT04:** Garantir que o link "Ver todos" no bloco "Últimas entradas na academia" redireciona o utilizador para a tela operacional de Presenças.
- **🧪 C04-CT05:** Validar o direcionamento para a "Central de Automações" através do link "Ver análise completa" na seção de Inteligência de Retenção e a interação com a execução de automações e relatórios de risco de evasão.

📎 **Fonte:** `CT_RF04_Acesso A Pagina Inicial Parte 3.md`

---

### 🧩 RF05 — Página Inicial (Parte 4)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C05-CT01:** Validar a abertura do modal "Cadastrar Avaliação" a partir do painel de Ações Rápidas, a busca/substituição do aluno, seleção do personal responsável, data e horário, finalizando com o salvamento da avaliação.
- **🧪 C05-CT02:** Validar o envio e troca de templates de mensagem (Falta, Cobrança, Retorno de treino, Aniversário, Avaliação) através das Ações Rápidas do painel "Inteligência Sifit" do cliente.
- **🧪 C05-CT03:** Validar a edição completa dos dados de um cliente (RG, foto de perfil, telefones, endereço, biometria e dados adicionais) salvando as alterações.
- **🧪 C05-CT04:** Verificar o direcionamento do modal "Clientes Sem Matrículas" (acessado pelos cards do Dashboard) para a tela de visualização do perfil do cliente.
- **🧪 C05-CT05:** Garantir o correto direcionamento da ação rápida "Ver avaliações" no card de Ações Recomendadas para a tela de gestão de Avaliações.

📎 **Fonte:** `CT_RF05_Acesso A Pagina Inicial Parte 4.md`

---

### 🧩 RF06 — Página Inicial (Parte 5)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C06-CT01:** Validar o direcionamento do modal "Personais" para a tela "Visualizar Cliente" ao clicar na ação correspondente do profissional cadastrado.
- **🧪 C06-CT02:** Validar o fluxo de aplicação de anamnese para o aluno, selecionando o modelo disponível, preenchendo o questionário e finalizando o processo.
- **🧪 C06-CT03:** Garantir a visualização do modal de histórico de presenças a partir do painel de desempenho do cliente.
- **🧪 C06-CT04:** Validar o comportamento do modal "Registrar pagamento" através das Ações Rápidas do cliente quando o aluno não possui contas pendentes.

📎 **Fonte:** `CT_RF06_Acesso A Pagina  Inicial Parte 5.md`

---

### 🧩 RF07 — Acesso e visualização do Dashboard

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C07-CT01:** Verificar o direcionamento para a tela "Dashboard" pelo menu lateral, a correta renderização dos painéis e o comportamento de alternância/mudança de tema de cores ao recarregar a página.
- **🧪 C07-CT02:** Validar a interatividade dos gráficos do Dashboard ao posicionar o cursor sobre as barras e seções, conferindo a exibição das etiquetas informativas (*tooltips*).
- **🧪 C07-CT03:** Validar o acionamento do botão "Ver Inteligência" no card "Inteligência Sifit" e a atualização das métricas ao alternar os filtros de período temporal.

📎 **Fonte:** `CT_RF07_ Acesso e visualização do Dashboard.md`

---

### 🧩 RF08 — Gerenciamento de Check-ins

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C08-CT01:** Validar a busca por código ou nome diretamente no campo de pesquisa da listagem principal de check-ins.
- **🧪 C08-CT02:** Confirmar a confirmação de presença clicando na ação "Registrar entrada" na linha do aluno com status Pendente.
- **🧪 C08-CT03:** Validar o comportamento do painel lateral "Entrada rápida" ao inserir um código de cliente e acionar "Realizar check-in".
- **🧪 C08-CT04:** Validar o fluxo completo do modal "+ Check-in manual", incluindo busca por cliente, seleção e inserção de observação opcional.

📎 **Fonte:** `CT_RF08_ Gerenciamento de Check ins.md`

---

### 🧩 RF09 — Consulta e Filtragem de Presenças de Clientes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C09-CT01:** Validar a busca de registros de presença informando o nome ou parte do nome do cliente no campo "Buscar por cliente..." (ex.: pesquisando por "gabrielli bononi" ou "albetro"), conferindo a atualização dos cards de resumo e o feedback da listagem.
- **🧪 C09-CT02:** Validar a busca de registros de presença informando o número ou código identificador do aluno no campo de pesquisa.
- **🧪 C09-CT03:** Validar o preenchimento automático das datas e a atualização imediata das métricas ao acionar os três botões de filtro rápido de período disponíveis (*"Hoje"*, *"Esta semana"* e *"Este mês"*).
- **🧪 C09-CT04:** Validar a seleção manual de datas customizadas nos campos "DE" e "ATÉ", incluindo a navegação pelos meses através do componente de calendário (ex.: alternando entre setembro, agosto e outubro) e a aplicação da busca.

📎 **Fonte:** `CT_RF09_Consulta e Filtragem de Presenças de Clientes.md`

---

### 🧩 RF10 — Gestão de Clientes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C10-CT01:** Validar o fluxo de cadastro de um novo cliente informando identificação, documentos, foto, contatos, endereço, dados biométricos, credenciais de aplicativo e informações complementares/responsável.
- **🧪 C10-CT02:** Validar o comportamento do sistema ao tentar submeter o formulário de cadastro de cliente deixando campos obrigatórios em branco.
- **🧪 C10-CT03:** Validar a atualização cadastral de um cliente existente a partir de seu perfil, alterando dados de endereço, biometria, aplicativo e dados complementares.
- **🧪 C10-CT04:** Validar o comportamento do sistema ao acionar a exclusão de um registro de cliente na listagem, tratando eventuais falhas de servidor (*Erro no servidor*).
- **🧪 C10-CT05:** Validar a consulta de clientes combinando filtros de código e nome diretamente nos campos de busca da listagem principal.

📎 **Fonte:** `CT_RF10_ Gestão de clientes.md`

---

### 🧩 RF11 — Gerenciamento de Matrículas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C11-CT01:** Validar a filtragem da listagem de matrículas utilizando os campos de busca por nome (ex.: "Rafaela Andrade") e por código numérico (ex.: "232").
- **🧪 C11-CT02:** Garantir que o sistema bloqueie a gravação e exiba aviso quando o utilizador tentar cadastrar uma matrícula sem selecionar um cliente associado.
- **🧪 C11-CT03:** Verificar se é possível abrir os detalhes de uma matrícula existente, habilitar a edição, alterar o campo de observação e persistir as modificações.
- **🧪 C11-CT04:** Validar o fluxo de cancelamento de uma matrícula ativa através da ação específica na listagem de registros.
- **🧪 C11-CT05:** Validar o comportamento do sistema ao acionar a exclusão de um registro de matrícula na listagem, tratando eventuais falhas do servidor (*Erro no servidor*).

📎 **Fonte:** `CT_RF11_ Gerenciamento de Matriculas.md`

---

### 🧩 RF12 — Gerenciamento de Avaliações Físicas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C12-CT01:** Validar os filtros por Código, Nome e Status (Todos / Pendente / Realizado) e a exibição dos indicadores no topo da tela "Avaliações".
- **🧪 C12-CT02:** Validar o fluxo do modal "Cadastrar Avaliação": busca do aluno por código ou nome, seleção do personal responsável, data e hora.
- **🧪 C12-CT03:** Verificar as mensagens de aviso ao tentar salvar a avaliação sem aluno, sem personal ou sem hora.
- **🧪 C12-CT04:** Validar o lançamento das medidas em centímetros e milímetros e a exibição automática da aba "Composição" na avaliação de um aluno.
- **🧪 C12-CT05:** Validar o modal "Alterar Data / Hora da avaliação" para uma avaliação com status Pendente.
- **🧪 C12-CT06:** Validar o preenchimento da aba "IMC" (idade, altura e peso) em uma avaliação pendente e a mudança de status ao salvar.
- **🧪 C12-CT07:** Validar o modal "Comparar Avaliação" entre uma avaliação antiga e uma nova do mesmo aluno.
- **🧪 C12-CT08:** Validar a página "Sua Avaliação Física" com dados pessoais, nível de gordura, composição corporal, índices e gráficos.
- **🧪 C12-CT09:** Validar a geração e o download do relatório "avaliação completa" em PDF pelo botão verde da linha.
- **🧪 C12-CT10:** Validar o relatório "Avaliação Física" (Dados Básicos, Circunferências, Dobras Subcutâneas e Composição Corporal) aberto pela ação de impressão da linha.
- **🧪 C12-CT11:** Validar a exclusão de uma avaliação mediante confirmação no modal.

📎 **Fonte:** `CT_RF12_ Gestao de avaliações.md`

---

### 🧩 RF13 — Registro e Gestão de Contas a Receber

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C13-CT01:** Validar os filtros da listagem de Contas a Receber: Código, Nome do cliente, Tipo de Data (Vencimento/Recebimento), Data Inicial/Final e Status.
- **🧪 C13-CT02:** Validar o cadastro de uma conta a receber pelo botão **Nova Conta**, incluindo a busca de cliente, a parametrização de cópias, o preenchimento dos dados do recebimento e a validação de campos obrigatórios.
- **🧪 C13-CT03:** Validar as restrições e mensagens de alerta emitidas pelo sistema ao tentar salvar uma nova conta a receber com campos obrigatórios em branco (cliente, valor a receber, tipo de pagamento, local de recebimento e caixa fechado).
- **🧪 C13-CT04:** Validar os botões de atalho de período (*Hoje*, *Ontem*, *Últimos 7 dias* e *Este mês*) na atualização das datas, da grid e dos cards.
- **🧪 C13-CT05:** Validar a visualização dos detalhes de uma conta recebida e a edição dos valores com o aviso de **Ajuste Administrativo**.
- **🧪 C13-CT06:** Validar a remoção de um lançamento na listagem de Contas a Receber mediante confirmação.

📎 **Fonte:** `CT_RF13_ Registro de contas a receber.md`

---

### 🧩 RF14 — Registro de Contas a Pagar

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C14-CT04:** Validar a exclusão de uma conta a pagar na listagem mediante confirmação no modal.

📎 **Fonte:** `CT_RF14_ Registro de contas a pagar.md`

---

### 🧩 RF15 — Gerenciamento de Fichas de Treino

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C15-CT01:** Validar o comportamento da listagem ao aplicar filtros por código de ficha (ex.: "236") e diferentes opções de **Status** (Ativo, Inativo, Cancelado, Finalizado), evidenciando que a filtragem por status ou código isolado na tabela não retorna registros correspondentes.

📎 **Fonte:** `CT_RF15_ Consulta de ficha de treino.md`

---

### 🧩 RF16 — Gerenciamento de Exercícios

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C16-CT01:** Validar a criação de um novo exercício e sua vinculação a um grupo muscular específico preenchendo o nome e anexando imagens e vídeos demonstrativos.
- **🧪 C16-CT02:** Validar a visualização e alteração de um exercício já cadastrado na biblioteca, atualizando seu nome ou dados complementares.
- **🧪 C16-CT03:** Validar a remoção de um exercício vinculado a um grupo muscular por meio do botão de exclusão e confirmação no modal.

📎 **Fonte:** `CT_RF16_ Gerenciamento de Exercícios.md`

---

### 🧩 RF17 — Gestão de Grupos Musculares

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C17-CT01:** Validar o funcionamento dos filtros por Código, Nome e Tipo Membro na listagem de Grupos Musculares, e a limpeza dos filtros.
- **🧪 C17-CT02:** Validar a inclusão de um novo grupo muscular com preenchimento de Nome, Tipo Membro e anexo de imagem.
- **🧪 C17-CT03:** Validar a alteração do nome e da imagem de um grupo muscular já cadastrado.
- **🧪 C17-CT05:** Validar a exclusão de um grupo muscular pela listagem, com confirmação.

📎 **Fonte:** `CT_RF17_ Gestão de grupos musculares.md`

---

### 🧩 RF18 — Gerenciamento de Objetivos Treino

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C18-CT02:** Validar o funcionamento da ferramenta de busca e filtragem utilizando o campo **Nome** na listagem de Objetivos de Treino.

📎 **Fonte:** `CT_RF18_ Gerenciamento de objetivos treino.md`

---

### 🧩 RF19 — Gestão de Grupos

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C19-CT01:** Validar o funcionamento dos filtros por Código, Nome, Status e Tipo de Caixa na listagem de grupos.
- **🧪 C19-CT02:** Validar o registro de um novo grupo preenchendo os campos obrigatórios e definindo o status como inativo.
- **🧪 C19-CT03:** Validar a obrigatoriedade de preenchimento dos campos essenciais ao tentar salvar um novo grupo sem as informações necessárias.
- **🧪 C19-CT04:** Verificar a alteração das configurações de código, descrição, tipo de caixa e status em grupos cadastrados.
- **🧪 C19-CT05:** Verificar a validação de integridade referencial do sistema ao tentar excluir um grupo que possui vínculos ativos.

📎 **Fonte:** `CT_RF19_ Gestão de grupos.md`

---

### 🧩 RF20 — Gestão de Turmas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C20-CT01:** Validar o funcionamento dos filtros por Nome da Turma, Código e Status, e do botão de limpar filtros, na listagem de turmas.
- **🧪 C20-CT02:** Validar o cadastro de uma nova turma preenchendo nome, plano, aula experimental, tempo, horários, personal e dias da semana.
- **🧪 C20-CT03:** Verificar as mensagens de validação exibidas ao tentar salvar uma turma sem preencher os campos obrigatórios (nome, plano, dia da semana e personal).
- **🧪 C20-CT05:** Verificar a funcionalidade de remoção de uma turma do sistema.

📎 **Fonte:** `CT_RF20_ Gestão de turmas.md`

---

### 🧩 RF21 — Gestão de Categorias Crossfit

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C21-CT01:** Validar a filtragem de registros na listagem utilizando o campo de busca por Código.
- **🧪 C21-CT02:** Validar o cadastramento bem-sucedido de uma nova categoria preenchendo o campo nome.
- **🧪 C21-CT03:** Validar a emissão de aviso de campo obrigatório ao tentar salvar uma categoria sem preencher o nome.
- **🧪 C21-CT04:** Validar a consistência da listagem principal após a inclusão de novas categorias.
- **🧪 C21-CT05:** Validar a alteração do nome de uma categoria existente através do modal de edição.
- **🧪 C21-CT06:** Validar o tratamento de erro do sistema ao tentar excluir uma categoria que possui dependências/vínculos.

📎 **Fonte:** `CT_RF21_Gestão de Categorias Crossfit.md`

---

### 🧩 RF22 — Gestão de Box (Turmas e Modalidades)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C22-CT01:** Validar o cadastro de uma nova modalidade preenchendo o nome correspondente no painel de Modalidades.
- **🧪 C22-CT02:** Validar o cadastro de uma nova turma recorrente vinculada a uma modalidade com configuração de horário e vagas.
- **🧪 C22-CT03:** Validar a edição do nome e do status de uma modalidade existente.
- **🧪 C22-CT04:** Validar a edição dos dados de uma turma recorrente existente (nome, modalidade vinculada, horários, vagas, dias da semana e status).
- **🧪 C22-CT05:** Validar a funcionalidade de exclusão de uma modalidade cadastrada na tabela de modalidades.
- **🧪 C22-CT06:** Testar a remoção de uma turma recorrente cadastrada na listagem de turmas do Box.

📎 **Fonte:** `CT_RF22_Gestão de Box - Turmas.md`

---

### 🧩 RF23 — Gerenciamento e Filtro de Caixas no Módulo Financeiro

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C23-CT01:** Validar a abertura de um novo caixa selecionando um local de contas válido no sistema.
- **🧪 C23-CT02:** Validar a filtragem dos caixas na tabela com base no status ("Aberto" ou "Fechado") e intervalo de datas.
- **🧪 C23-CT03:** Validar a visualização detalhada das entradas financeiras ao acessar a aba **Ver Entradas** no painel de fechamento do caixa.
- **🧪 C23-CT04:** Validar a visualização detalhada das saídas/despesas ao acessar a aba **Ver Saídas** no painel de fechamento do caixa.
- **🧪 C23-CT05:** Validar que o sistema obriga o preenchimento do campo **"Motivo"** ao registrar uma divergência na conferência física do caixa.
- **🧪 C23-CT06:** Validar o comportamento do sistema ao tentar buscar contas com parâmetros ou locais que gerem conflito na janela de fechamento de caixa.
- **🧪 C23-CT07:** Validar a funcionalidade de geração e impressão do relatório oficial de fechamento de caixa em formato PDF.

📎 **Fonte:** `CT_RF23_ Gerenciamento e Filtro de Caixas .md`

---

### 🧩 RF24 — Gestão Financeira e Cobranças via Pagar.me no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C24-CT01:** Validar a abertura do modal de consulta de valores **Em processamento** e visualização de prazos de liberação no Pagar.me.
- **🧪 C24-CT02:** Validar a consulta de **Recebíveis Futuros** e a listagem ou mensagem de retorno na modal correspondente.
- **🧪 C24-CT03:** Validar o fluxo de preenchimento e solicitação de saque de valores disponíveis na conta Pagar.me.
- **🧪 C24-CT04:** Validar a abertura e exibição do **Relatório — Assinaturas Ativas** a partir do painel financeiro.
- **🧪 C24-CT05:** Validar a alteração do período de visualização no gráfico de **Recebimentos** (alternando entre 7, 30 e 90 dias).
- **🧪 C24-CT06:** Validar a consulta detalhada do **Extrato de Transações** através do atalho na listagem de transações recentes.
- **🧪 C24-CT07:** Validar o registro e geração de uma nova cobrança avulsa preenchendo descrição, valor e selecionando o método de pagamento.
- **🧪 C24-CT08:** Validar o redirecionamento e a navegação para o painel de **Configurações** gerais de integração do sistema.
- **🧪 C24-CT09:** Validar a verificação de registros no extrato de transações utilizando o botão de listagem completa na tabela de repasses/transações.
- **🧪 C24-CT10:** Validar a visualização dos indicadores de **Repasses**, **Assinaturas** e **Chargebacks** na visão geral do Pagar.me.

📎 **Fonte:** `CT_RF24_Gestão Financeira e Cobranças via Pagar.me.md`

---

### 🧩 RF25 — Gerenciamento e Cadastro de Despesas Fixas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C25-CT01:** O sistema deve permitir a busca e filtragem de despesas fixas utilizando os filtros de nome e recorrência na interface.
- **🧪 C25-CT02:** O sistema deve permitir o cadastro de uma nova despesa fixa preenchendo todos os campos obrigatórios no modal correspondente.
- **🧪 C25-CT03:** O sistema deve permitir editar os parâmetros (como valor, status ou recorrência) de uma despesa fixa já existente.
- **🧪 C25-CT04:** O sistema deve permitir a remoção definitiva de uma despesa fixa mediante confirmação em modal.
- **🧪 C25-CT05:** O sistema deve validar o preenchimento dos campos obrigatórios e exibir mensagens de erro/alerta caso o usuário tente salvar uma nova despesa com campos vazios.

📎 **Fonte:** `CT_RF25_Gerenciamento e Cadastro de Despesas Fixas.md`

---

### 🧩 RF26 — Geração e Filtragem de Relatórios Operacionais e Financeiros

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C26-CT01:** O sistema deve exibir o painel central de relatórios com as opções de modelos disponíveis para seleção.
- **🧪 C26-CT02:** O sistema deve permitir a emissão do relatório de "Avaliações" filtrando por um intervalo de datas específico.
- **🧪 C26-CT03:** O sistema deve permitir a emissão do relatório de "Clientes" com base no período selecionado.
- **🧪 C26-CT04:** O sistema deve permitir a emissão de relatórios referentes aos colaboradores da academia por período.
- **🧪 C26-CT05:** O sistema deve permitir a emissão do relatório de "Matrículas" aplicando filtros por planos específicos e período.
- **🧪 C26-CT06:** O sistema deve permitir a emissão do relatório de "Contas a Receber" com filtros avançados de status, forma de pagamento e formato detalhado.
- **🧪 C26-CT07:** O sistema deve permitir a emissão do relatório de "Contas a Pagar" filtrando por período de vencimento ou pagamento.
- **🧪 C26-CT08:** O sistema deve permitir a emissão do relatório de "Caixas" alternando o formato de visualização entre "Normal" e "Detalhado".

📎 **Fonte:** `CT_RF26_Geração e Filtragem de Relatórios Operacionais e Financeiros.md`

---

### 🧩 RF27 — Gestão de Colaboradores via Sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C27-CT01:** O sistema deve filtrar e retornar corretamente o colaborador pesquisado através dos filtros de código ou nome.
- **🧪 C27-CT02:** O sistema deve permitir o cadastro bem-sucedido de um novo colaborador com o preenchimento de todos os dados válidos.
- **🧪 C27-CT03:** O sistema deve permitir alterar os dados cadastrais e o status de um colaborador já existente.
- **🧪 C27-CT04:** O sistema deve permitir gerenciar, vincular ou adicionar novas funções (ex.: "Treinador da academia", "Personal") a um colaborador.
- **🧪 C27-CT05:** O sistema deve exibir uma tela de perfil detalhado com todas as informações e métricas consolidadas ao selecionar um colaborador.
- **🧪 C27-CT06:** O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar um colaborador com campos obrigatórios vazios.
- **🧪 C27-CT07:** O sistema deve permitir a remoção definitiva de um colaborador cadastrado mediante confirmação em modal.

📎 **Fonte:** `CT_RF27_ Gestão de colaboradores via sistema SIFIT.md`

---

### 🧩 RF28 — Gestão de Funções

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C28-CT01:** O sistema deve filtrar e retornar corretamente a listagem de funções com base nos critérios de nome, código e tipo (interno ou externo).
- **🧪 C28-CT02:** O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar uma nova função deixando campos obrigatórios em branco.
- **🧪 C28-CT03:** O sistema deve permitir o cadastro de uma nova função preenchendo corretamente os campos de nome, tipo de funcionário e parâmetros relacionados.
- **🧪 C28-CT04:** O sistema deve permitir visualizar e alterar as permissões de acesso liberadas para uma determinada função.
- **🧪 C28-CT05:** O sistema deve exibir o modal com os dados detalhados de uma função ao acionar a opção de visualização.

📎 **Fonte:** `CT_RF28_Gestão de Funções.md`

---

### 🧩 RF29 — Gerenciamento de Fornecedores no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C29-CT01:** O sistema deve permitir a busca e filtragem de fornecedores cadastrados utilizando os campos de código ou nome.
- **🧪 C29-CT02:** O sistema deve permitir o cadastro de um novo fornecedor preenchendo corretamente os campos obrigatórios e complementares no modal "Novo Fornecedor".
- **🧪 C29-CT03:** O sistema deve impedir o cadastro e emitir mensagens de alerta caso o usuário tente salvar um fornecedor sem preencher os campos obrigatórios.
- **🧪 C29-CT04:** O sistema deve exibir todas as informações consolidadas de um fornecedor ao acionar a opção de visualização de cadastro.
- **🧪 C29-CT05:** O sistema deve exigir confirmação em modal ao solicitar a exclusão de um fornecedor e processar a requisição de remoção.

📎 **Fonte:** `CT_RF29_Gerenciamento de Fornecedores no SIFIT.md`

---

### 🧩 RF30 — Gerenciamento de Tipos de Documentos no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C30-CT01:** O sistema deve permitir a filtragem de tipos de documentos cadastrados utilizando os campos de código, nome ou o filtro de aplicação.
- **🧪 C30-CT02:** O sistema deve permitir a criação bem-sucedida de um novo tipo de documento definindo seu nome e a respectiva aplicação.
- **🧪 C30-CT03:** O sistema deve impedir o salvamento e emitir um aviso caso o usuário tente cadastrar um tipo de documento com o campo de nome vazio.
- **🧪 C30-CT04:** O sistema deve permitir alterar os dados cadastrais (como a aplicação) de um tipo de documento já existente.
- **🧪 C30-CT05:** O sistema deve solicitar confirmação via modal ao tentar excluir um tipo de documento e processar a solicitação de remoção.

📎 **Fonte:** `CT_RF30_Gerenciamento de Tipos de Documentos no SIFIT.md`

---

### 🧩 RF31 — Gerenciamento de Atividades no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C31-CT01:** O sistema deve permitir a filtragem das atividades cadastradas por nome ou por código.
- **🧪 C31-CT02:** O sistema deve permitir o cadastro de uma nova atividade por meio do modal "Atividade".
- **🧪 C31-CT04:** O sistema deve permitir a visualização e a atualização das informações de uma atividade existente.
- **🧪 C31-CT05:** O sistema deve permitir a exclusão de uma atividade mediante confirmação do usuário.

📎 **Fonte:** `CT_RF31_Gerenciamento de Atividades no SIFIT.md`

---

### 🧩 RF32 — Gerenciamento de Pontuações no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C32-CT01:** O sistema deve permitir filtrar as pontuações cadastradas por código, nome da pontuação e status (Ativo/Inativo).
- **🧪 C32-CT02:** O sistema deve permitir a criação de uma nova pontuação (campanha) com período, tipo, status e produtos de resgate.
- **🧪 C32-CT04:** O sistema deve permitir vincular atividades a uma pontuação por meio do modal "Atividades da Pontuação".
- **🧪 C32-CT05:** O sistema deve permitir visualizar o ranking de participantes associados a uma pontuação.
- **🧪 C32-CT07:** O sistema deve permitir excluir uma pontuação existente após confirmação do usuário.

📎 **Fonte:** `CT_RF32_Gerenciamento de Pontuações no SIFIT.md`

---

### 🧩 RF33 — Gerenciamento de Produtos no SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C33-CT01:** O sistema deve permitir filtrar a listagem de produtos por Código, Nome, Status (Ativo/Inativo) e Tipo (Venda/Pontuação).
- **🧪 C33-CT02:** O sistema deve permitir cadastrar um novo produto informando Nome, Descrição, Tipo, Pontuação e Imagem.
- **🧪 C33-CT03:** O sistema deve permitir a alteração das informações de um produto previamente cadastrado.
- **🧪 C33-CT04:** O sistema deve solicitar confirmação antes de remover um produto do cadastro.

📎 **Fonte:** `CT_RF33_Gerenciamento de Produtos no SIFIT.md`

---

### 🧩 RF34 — Módulo de Enquetes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C34-CT01:** O sistema deve permitir a filtragem da lista de enquetes pelos campos Código, Nome e Status (Todos/Ativo/Inativo).
- **🧪 C34-CT04:** O sistema deve solicitar confirmação antes da exclusão e reportar a falha caso o registro não possa ser removido.

📎 **Fonte:** `CT_RF34_Filtrar Enquetes por Código, Nome e Status.md`

---

### 🧩 RF35 — Gestão e consulta de leads no módulo Prospecção

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C35-CT01:** O sistema deve permitir a busca e filtragem de leads cadastrados utilizando os campos de texto por nome, e-mail, telefone ou código.
- **🧪 C35-CT02:** O sistema deve permitir o cadastro bem-sucedido de um novo lead preenchendo os dados pessoais, contato, observação e definindo o estágio inicial.
- **🧪 C35-CT03:** O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar um lead sem preencher o campo de nome.
- **🧪 C35-CT04:** O sistema deve permitir visualizar os dados de um lead existente, atualizar informações de contato/observações e alterar seu estágio no funil.
- **🧪 C35-CT05:** O sistema deve solicitar confirmação via modal antes de remover definitivamente um lead cadastrado.

📎 **Fonte:** `CT_RF35_Gestão e consulta de leads no módulo Prospecção.md`

---

### 🧩 RF36 — Gestão e consulta de planos no sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C36-CT01:** O sistema deve filtrar e retornar corretamente o plano correspondente ao utilizar os filtros de código, nome ou status (Ativo/Inativo).
- **🧪 C36-CT02:** O sistema deve permitir o cadastro bem-sucedido de um novo plano definindo dados básicos, valores, períodos de cobrança e regras de equipe/dependentes.
- **🧪 C36-CT03:** O sistema deve permitir a alteração das informações e do status (Ativo/Inativo) de um plano já cadastrado.
- **🧪 C36-CT04:** O sistema deve impedir a exclusão de um plano que possua vínculos ativos e apresentar uma mensagem de erro apropriada.
- **🧪 C36-CT05:** O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar um plano sem preencher os campos essenciais.

📎 **Fonte:** `CT_RF36_Gestão e consulta de planos no sistema SIFIT.md`

---

### 🧩 RF37 — Gestão de Modelos de Contrato no sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C37-CT01:** O sistema deve redirecionar o usuário para a tela de adição ao clicar no botão de novo modelo de contrato.
- **🧪 C37-CT02:** O sistema deve gerar e atualizar a pré-visualização do contrato formatado de acordo com o texto digitado no editor.
- **🧪 C37-CT03:** O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados do aluno no corpo do texto do contrato.
- **🧪 C37-CT04:** O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados do plano contratado no corpo do texto do contrato.
- **🧪 C37-CT05:** O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados da academia no corpo do texto do contrato.
- **🧪 C37-CT06:** O sistema deve permitir a inclusão de tags dinâmicas referentes às informações contratuais específicas no texto do modelo.
- **🧪 C37-CT07:** O sistema deve permitir a expansão e o recolhimento do painel completo de variáveis disponíveis para consulta.

📎 **Fonte:** `CT_RF37_Gestão de Modelos de Contrato no sistema SIFIT.md`

---

### 🧩 RF38 — Gestão de Tipos de Pagamento no Sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C38-CT01:** O sistema deve validar o preenchimento obrigatório dos campos ao tentar cadastrar um novo tipo de pagamento em branco.
- **🧪 C38-CT02:** O sistema deve permitir a busca e filtragem precisa dos tipos de pagamento cadastrados utilizando código, nome ou status.
- **🧪 C38-CT03:** O sistema deve permitir o cadastro de um novo tipo de pagamento definindo corretamente os campos obrigatórios, status, bandeira e integração.
- **🧪 C38-CT04:** O sistema deve permitir a alteração e atualização das configurações de um tipo de pagamento existente.
- **🧪 C38-CT05:** O sistema deve bloquear a remoção de tipos de pagamento vinculados a outras operações e exibir a mensagem de erro adequada.

📎 **Fonte:** `CT_RF38_Gestão de Tipos de Pagamento no sistema SIFIT.md`

---

### 🧩 RF39 — Gestão de Bandeiras de Cartão no Sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C39-CT01:** O sistema deve abrir o modal "Nova Bandeira" com os campos limpos e validar o preenchimento obrigatório ao tentar salvar sem o nome da bandeira.
- **🧪 C39-CT02:** O sistema deve permitir o preenchimento do nome, taxas adicionais, taxa de débito e a adição de regras de parcelamento para uma nova bandeira.
- **🧪 C39-CT03:** O sistema deve executar a consulta e filtragem de bandeiras de cartão cadastradas com base nos parâmetros informados nos campos de busca.

📎 **Fonte:** `CT_RF39_ Abrir modal de cadastro de bandeira de cartão.md`

---

### 🧩 RF40 — Aplicação de Fichas de Anamnese no sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C40-CT03:** O sistema deve permitir a filtragem e consulta de fichas de anamnese cadastradas através do seletor de status e barra de pesquisa na tela principal.

📎 **Fonte:** `CT_RF40_ Aplicação de Fichas de Anamnese no sistema SIFIT.md`

---

### 🧩 RF41 — Gerenciamento de Modelos de Anamnese no Sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C41-CT01:** Validar a exibição do modal de confirmação de exclusão e a remoção definitiva de um modelo de anamnese do sistema.
- **🧪 C41-CT02:** Validar a alteração do status de um modelo de anamnese de "Ativo" para "Inativo" através da tela de edição.
- **🧪 C41-CT03:** Validar a filtragem dos modelos de anamnese na listagem principal utilizando o seletor de status (Ativo, Inativo ou Todos).
- **🧪 C41-CT04:** Validar o fluxo de cadastro de um novo modelo de anamnese preenchendo as informações gerais e definindo seu status inicial.
- **🧪 C41-CT05:** Validar a seleção e adição de perguntas ao modelo através do montador visual, incluindo a marcação de campos obrigatórios.

📎 **Fonte:** `CT_RF41_ Gerenciamento de Modelos de Anamnese no sistema SIFIT.md`

---

### 🧩 RF42 — Gerenciamento de Categorias de Anamnese no sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C42-CT01:** O sistema deve permitir cadastrar uma nova categoria definindo nome, status, ícone e cor visual.
- **🧪 C42-CT02:** O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar uma categoria sem preencher o nome.
- **🧪 C42-CT03:** O sistema deve permitir alterar as informações (como status, nome, ícone ou cor) de uma categoria cadastrada.
- **🧪 C42-CT04:** O sistema deve filtrar o grid de categorias conforme o status selecionado (Ativo/Inativo) e permitir a busca por termos no campo de pesquisa.
- **🧪 C42-CT05:** O sistema deve solicitar confirmação via modal e remover permanentemente uma categoria selecionada.

📎 **Fonte:** `CT_RF42_Gerenciamento de Categorias de Anamnese no sistema SIFIT.md`

---

### 🧩 RF43 — Gestão de Pergunta de Anamnese no Sistema SIFIT

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C43-CT01:** Validar a exibição do modal de confirmação de exclusão e a remoção definitiva de uma pergunta da listagem do sistema.
- **🧪 C43-CT02:** Validar o comportamento do sistema ao tentar alterar o tipo de resposta de uma pergunta cadastrada, exibindo a mensagem de erro correspondente.
- **🧪 C43-CT03:** Validar o fluxo de cadastro de uma nova pergunta de anamnese preenchendo o código, nome, texto da pergunta e selecionando o tipo de resposta.
- **🧪 C43-CT04:** O sistema deve validar o preenchimento obrigatório dos campos ao tentar salvar uma nova pergunta com dados incompletos.
- **🧪 C43-CT05:** Validar a filtragem de perguntas na listagem principal utilizando os campos de busca por código, nome e filtros de status (Ativo/Inativo).

📎 **Fonte:** `CT_RF43_Gestão de Pergunta de Anamnese.md`

---

### 🧩 RF44 — Módulo Inteligência & Automação e Gestão de Clientes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C44-CT01:** Validar o direcionamento para a tela "Inteligência & Automação" e a renderização dos cards de métricas principais, automações ativas e histórico de atividades recentes.
- **🧪 C44-CT02:** Validar a aplicação de filtros por categoria de risco (*Alto risco*, *Médio*, *Baixo risco*) no painel do Relatório de Risco de Evasão.
- **🧪 C44-CT03:** Validar a mensagem de aviso ao tentar acionar manualmente a automação de Aniversariantes.
- **🧪 C44-CT04:** Validar a alteração dos parâmetros de frequência, critérios de análise e sensibilidade na automação de Risco de Evasão, observando o retorno de validação de destinatários obrigatórios.
- **🧪 C44-CT05:** Validar a navegação e ajuste de parâmetros de frequência personalizada na janela de configuração da automação de Aniversariantes.
- **🧪 C44-CT06:** Validar a expansão do painel lateral de detalhes ao selecionar um aluno listado no Relatório de Risco de Evasão.
- **🧪 C44-CT07:** Validar o acionamento das ações rápidas (*Registrar pagamento*, *Agendar avaliação*, *Enviar mensagem*) diretamente da tela do cliente.
- **🧪 C44-CT08:** Validar a expansão e interação com os cards da seção "Automações disponíveis" (*Avaliações vencendo*, *Frequência em queda*, *Financeiro diário*, *Cobranças automáticas*).
- **🧪 C44-CT09:** Validar o preenchimento e finalização do registro de pagamento de uma mensalidade pendente através das Ações Rápidas no perfil do cliente.

📎 **Fonte:** `CT_RF44_ Gestões de inteligência.md`

---

### 🧩 RF45 — Visualização e Filtragem do Dashboard de Resultados da Inteligência

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C45-CT01:** O sistema deve atualizar os indicadores, gráficos e listas do dashboard conforme o período temporal selecionado pelo usuário.

📎 **Fonte:** `CT_RF45_ Visualização e Filtragem do Dashboard de Resultados da Inteligência.md`

---

### 🧩 RF46 — Gestão de configurações

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C46-CT01:** Validar a alteração de parâmetros gerais de acesso e presença na aba "Home" e a mensagem de erro ao tentar persistir as configurações.
- **🧪 C46-CT02:** Validar a navegação para a aba "Biometria", preenchimento de IP, porta e modelo de aparelho de catraca, e o comportamento ao salvar.
- **🧪 C46-CT03:** Validar a alteração de regras de avaliação na aba "Avaliação" (cobrança, tipo de avaliação e dias de validade) e a resposta ao salvar.
- **🧪 C46-CT04:** Validar a habilitação e edição de templates de mensagens de aniversário na aba "Aniversário" (WhatsApp, SMS, E-mail) e a tentativa de salvamento.
- **🧪 C46-CT05:** Validar a alteração de parâmetros de pagamento online e inserção de token de integração na aba "Pagamento".
- **🧪 C46-CT06:** Validar a gestão de integrações de API na aba "Integrações", preenchendo credenciais de conexão do WhatsApp e testando o salvamento.
- **🧪 C46-CT07:** Validar a alteração de cores principais e secundárias, bem como o upload de imagens de logotipo e capa na aba "Design".

📎 **Fonte:** `CT_RF46_ Gestões de configurações.md`

---

### 🧩 RF47 — Gerenciamento de Modelos de Ficha

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C47-CT01:** Validar o comportamento do sistema ao preencher o formulário de cadastro de um novo modelo de ficha e submeter a gravação.
- **🧪 C47-CT02:** Validar a busca e filtragem de registros na listagem de modelos de ficha utilizando os campos de código, título e criador.

📎 **Fonte:** `CT_RF47_Gerenciamento de Modelos de Ficha.md`

---

### 🧩 RF48 — Gerenciamento de Notificações

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C48-CT01:** Validar a abertura e o fechamento do modal "Todas as notificações" e a exibição do estado da seção de Denúncias.
- **🧪 C48-CT02:** Validar o modal "Todas as postagens" e a alternância dos filtros "Ver todas" e "Só pendentes" nas seções de Postagens e Denúncias.
- **🧪 C48-CT03:** Validar a abertura do modal de criação, o preenchimento da mensagem com prévia no celular e o envio do aviso aos alunos.
- **🧪 C48-CT04:** Validar a abertura do painel de notificações pelo ícone de sino e a alternância entre as abas "Tudo" e "Não lidas".
- **🧪 C48-CT05:** Validar a transição do modal "Todas as notificações" para o modal de criação e o bloqueio do envio com a mensagem vazia.
- **🧪 C48-CT06:** Validar a exibição do modal de detalhes de uma notificação já enviada através do ícone de lupa.
- **🧪 C48-CT07:** Validar a exclusão de uma notificação a partir do ícone de lixeira na listagem.

📎 **Fonte:** `CT_RF48_ Gerenciamento de Notificações e Conteúdos do Aplicativo.md`

---

### 🧩 RF49 — Alternância de Tema da Interface (Claro / Escuro)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C49-CT01:** Validar a alteração do tema visual da interface do modo Claro para o modo Escuro.
- **🧪 C49-CT02:** Validar o retorno da interface do modo Escuro para o modo Claro.

📎 **Fonte:** `CT_RF49_Alternância de Tema da Interface.md`

---

## 🛡️ 5. Requisitos Não Funcionais (Propostas de Qualidade)

- **RNF01 — Usabilidade:** A interface deve manter responsividade e acessibilidade em resoluções desktop e mobile, preservando o contraste e a leitura nos modos claro e escuro.
- **RNF02 — Desempenho:** As consultas com filtros complexos (ex.: relatórios e dashboards) devem responder em um tempo médio inferior a 2 segundos.
- **RNF03 — Segurança e Privacidade:** Dados sensíveis (biometria, documentos e registros de saúde da anamnese) devem trafegar criptografados via protocolo HTTPS.
- **RNF04 — Confiabilidade:** O sistema deve tratar falhas de comunicação com gateways de pagamento (ex.: Pagar.me) informando mensagens amigáveis ao usuário sem corromper transações.

> Os RNFs acima são propostas de qualidade para validação com o responsável pelo produto; os cenários atuais não comprovam metas mensuráveis para eles.

---

## ⚠️ 6. Pontos de Atenção Identificados

Falhas, erros de servidor e validações ausentes encontrados durante a execução estão detalhados no `3-Relatorio de Bugs.md` (24 bugs registrados). Esses comportamentos são defeitos observados e **não** devem ser lidos como requisitos de funcionamento correto.

---

## 🔗 7. Rastreabilidade

A numeração RF01–RF49 acompanha a numeração dos 49 arquivos da pasta `Sifit/Cenario de Testes/`. O detalhamento de passos, pré-condições, critérios de aceitação e evidências está no arquivo de origem indicado em cada requisito.

---

## ℹ️ 8. Limitações

- Esta análise foi construída a partir dos arquivos de cenários presentes na pasta (49 cenários, 232 casos). Alguns arquivos contêm apenas parte dos casos originalmente planejados: os casos de teste ligados aos bugs do relatório (por exemplo `C01-CT04`, `C14-CT01` a `C14-CT03`, `C32-CT03`, `C32-CT06`, `C32-CT08`, `C34-CT02`, `C34-CT03`, `C37-CT08`, `C40-CT01` e `C40-CT02`) estão descritos somente no Relatório de Bugs.
- O cenário **Gerenciamento de Aulas do SifitBox** (filtro por período, validação de datas e botão “Gerar aulas”) possui bugs registrados (BUG-002 a BUG-004), mas não tem arquivo na pasta de cenários.
- Requisitos de desempenho, disponibilidade, segurança, acessibilidade e compatibilidade precisam de aprovação e critérios mensuráveis do responsável pelo sistema.
