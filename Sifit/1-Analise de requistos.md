## 📦 **Requisitos Funcionais Detalhados para Testes Manuais**

### 🔐 **RF01 - Login na plataforma**

**Descrição**: O sistema deve permitir o acesso à plataforma SIFIT mediante nome de usuário e senha.

* **Funcionalidades esperadas**:

  * Realizar login com nome de usuário e senha válidos. (C01-CT01)
  * Falhar o login quando o nome de usuário ou a senha forem inválidos. (C01-CT02)
  * Falhar o login quando os campos de usuário e senha estiverem apagados ou em branco. (C01-CT03)

---

### 🏠 **RF02 - Página Inicial (Parte 1)**

**Descrição**: Após o login, a Página Inicial deve exibir cards e atalhos com acesso rápido a consultas de alunos, avaliações, mensalidades e risco de evasão.

* **Funcionalidades esperadas**:

  * Abrir e buscar por nome no modal "Clientes Sem Matrículas". (C02-CT01)
  * Consultar detalhadamente os alunos sumidos/ausentes há mais tempo na academia. (C02-CT02)
  * Redirecionar da Página Inicial para a tela de gestão de Avaliações físicas. (C02-CT03)
  * Exibir o modal de mensalidades pendentes e alternar atalhos por período de atraso. (C02-CT04)
  * Abrir o Radar de Evasão e exibir as regras de pontuação/risco de cancelamento do aluno. (C02-CT05)

---

### 🏠 **RF03 - Página Inicial (Parte 2)**

**Descrição**: A Página Inicial deve permitir abrir modais de detalhamento a partir dos cards do dashboard (financeiro, desistências, matrículas, personais e agenda).

* **Funcionalidades esperadas**:

  * Abrir o modal "Mensalidades pendentes / Financeiro em Aberto" em "Ver detalhes" e filtrar por período de vencimento. (C03-CT01)
  * Exibir o modal "Desistências no Período" e buscar por nome ou código. (C03-CT02)
  * Abrir e pesquisar no modal "Matrículas no Período". (C03-CT03)
  * Abrir pelo card "Personais" a lista de profissionais cadastrados com busca individualizada. (C03-CT04)
  * Expandir o modal "Agenda de hoje" em "Ver agenda", buscar aulas, selecionar unidades e alterar os detalhes ao selecionar aulas (*Turma dos Bodybuilders*, *Teste*, *Horario da manhã*), disponibilizando botões de ações rápidas. (C03-CT05)

---

### 🏠 **RF04 - Página Inicial (Parte 3)**

**Descrição**: A Página Inicial deve oferecer ações recomendadas, aniversariantes, últimas entradas e acesso à Inteligência de Retenção.

* **Funcionalidades esperadas**:

  * Abrir o modal "Falar com inativos" em "Ações recomendadas para hoje", buscar alunos, personalizar a mensagem e selecionar o canal de envio. (C04-CT01)
  * Abrir o modal do card "Cobrar alunos", buscar inadimplentes e personalizar a mensagem de cobrança segura. (C04-CT02)
  * Redirecionar em "Ver todos" de "Aniversariantes do dia" e filtrar por período (7 dias, 33 dias) e navegação mensal no calendário. (C04-CT03)
  * Redirecionar o link "Ver todos" de "Últimas entradas na academia" para a tela de Presenças. (C04-CT04)
  * Direcionar para a "Central de Automações" via "Ver análise completa" da Inteligência de Retenção, com interação com execução de automações e relatórios de risco de evasão. (C04-CT05)

---

### 🏠 **RF05 - Página Inicial (Parte 4)**

**Descrição**: A Página Inicial deve permitir executar ações rápidas sobre avaliações e sobre o cliente (mensagens, edição de dados e navegação).

* **Funcionalidades esperadas**:

  * Abrir o modal "Cadastrar Avaliação" pelas Ações Rápidas, buscar/substituir aluno, selecionar personal, data e horário e salvar. (C05-CT01)
  * Enviar e trocar templates de mensagem (Falta, Cobrança, Retorno de treino, Aniversário, Avaliação) pelo painel "Inteligência Sifit" do cliente. (C05-CT02)
  * Editar os dados completos de um cliente (RG, foto, telefones, endereço, biometria e dados adicionais) e salvar. (C05-CT03)
  * Direcionar do modal "Clientes Sem Matrículas" para a tela de visualização do perfil do cliente. (C05-CT04)
  * Direcionar a ação rápida "Ver avaliações" para a tela de gestão de Avaliações. (C05-CT05)

---

### 🏠 **RF06 - Página Inicial (Parte 5)**

**Descrição**: A Página Inicial deve permitir acessar perfis, aplicar anamnese, consultar histórico de presenças e registrar pagamentos a partir dos modais.

* **Funcionalidades esperadas**:

  * Direcionar o modal "Personais" para a tela "Visualizar Cliente". (C06-CT01)
  * Aplicar anamnese ao aluno: selecionar o modelo, preencher o questionário e finalizar. (C06-CT02)
  * Exibir o modal de histórico de presenças a partir do painel de desempenho do cliente. (C06-CT03)
  * Exibir o comportamento do modal "Registrar pagamento" quando o aluno não possui contas pendentes. (C06-CT04)

---

### 📊 **RF07 - Acesso e visualização do Dashboard**

**Descrição**: O sistema deve exibir o Dashboard com painéis, gráficos e indicadores consolidados da academia.

* **Funcionalidades esperadas**:

  * Acessar o "Dashboard" pelo menu lateral, renderizar corretamente os painéis e alternar o tema de cores ao recarregar a página. (C07-CT01)
  * Exibir tooltips ao posicionar o cursor sobre barras e seções dos gráficos. (C07-CT02)
  * Acionar "Ver Inteligência" no card "Inteligência Sifit" e atualizar as métricas ao alternar o filtro de período. (C07-CT03)

---

### ✅ **RF08 - Gerenciamento de Check-ins**

**Descrição**: O sistema deve permitir registrar e consultar entradas dos alunos na academia.

* **Funcionalidades esperadas**:

  * Buscar por código ou nome no campo de pesquisa da listagem de check-ins. (C08-CT01)
  * Confirmar presença pela ação "Registrar entrada" na linha de aluno com status Pendente. (C08-CT02)
  * Usar o painel lateral "Entrada rápida" informando o código do cliente e acionando "Realizar check-in". (C08-CT03)
  * Realizar o fluxo completo do modal "+ Check-in manual": buscar cliente, selecioná-lo e inserir observação opcional. (C08-CT04)

---

### 🗓️ **RF09 - Consulta e Filtragem de Presenças de Clientes**

**Descrição**: O sistema deve permitir consultar e filtrar os registros de presença dos clientes.

* **Funcionalidades esperadas**:

  * Buscar presenças pelo nome ou parte do nome (ex.: "gabrielli bononi", "albetro"), atualizando os cards de resumo e o feedback da listagem. (C09-CT01)
  * Buscar presenças pelo número/código do aluno. (C09-CT02)
  * Preencher automaticamente as datas e atualizar as métricas ao acionar os filtros rápidos "Hoje", "Esta semana" e "Este mês". (C09-CT03)
  * Selecionar datas personalizadas nos campos "DE" e "ATÉ", navegando entre os meses do calendário, e aplicar a busca. (C09-CT04)

---

### 👤 **RF10 - Gestão de Clientes**

**Descrição**: O sistema deve permitir o gerenciamento completo do cadastro de clientes.

* **Funcionalidades esperadas**:

  * Cadastrar novo cliente informando identificação, documentos, foto, contatos, endereço, biometria, credenciais de aplicativo e informações complementares/responsável. (C10-CT01)
  * Impedir a submissão do cadastro com campos obrigatórios em branco. (C10-CT02)
  * Atualizar o cadastro de um cliente existente (endereço, biometria, aplicativo e dados complementares). (C10-CT03)
  * Acionar a exclusão de um cliente na listagem, tratando falhas de servidor (*Erro no servidor*). (C10-CT04)
  * Consultar clientes combinando filtros de código e nome na listagem. (C10-CT05)

---

### 📝 **RF11 - Gerenciamento de Matrículas**

**Descrição**: O sistema deve permitir consultar, cadastrar, editar, cancelar e excluir matrículas.

* **Funcionalidades esperadas**:

  * Filtrar a listagem por nome (ex.: "Rafaela Andrade") e por código numérico (ex.: "232"). (C11-CT01)
  * Bloquear a gravação e exibir aviso ao cadastrar matrícula sem cliente associado. (C11-CT02)
  * Abrir os detalhes de uma matrícula, habilitar a edição, alterar a observação e persistir. (C11-CT03)
  * Cancelar uma matrícula ativa pela ação específica da listagem. (C11-CT04)
  * Acionar a exclusão de uma matrícula, tratando falhas de servidor (*Erro no servidor*). (C11-CT05)

---

### 📏 **RF12 - Gerenciamento de Avaliações Físicas**

**Descrição**: O sistema deve permitir agendar, lançar, comparar, emitir e excluir avaliações físicas dos alunos.

* **Funcionalidades esperadas**:

  * Filtrar por Código, Nome e Status (Todos/Pendente/Realizado) e exibir os indicadores no topo da tela "Avaliações". (C12-CT01)
  * Cadastrar avaliação no modal "Cadastrar Avaliação": buscar aluno por código/nome, selecionar personal, data e hora. (C12-CT02)
  * Exibir avisos ao salvar a avaliação sem aluno, sem personal ou sem hora. (C12-CT03)
  * Lançar medidas em centímetros e milímetros e exibir automaticamente a aba "Composição". (C12-CT04)
  * Alterar data/hora de uma avaliação Pendente no modal "Alterar Data / Hora da avaliação". (C12-CT05)
  * Preencher a aba "IMC" (idade, altura e peso) e mudar o status ao salvar. (C12-CT06)
  * Comparar uma avaliação antiga com uma nova do mesmo aluno no modal "Comparar Avaliação". (C12-CT07)
  * Exibir a página "Sua Avaliação Física" com dados pessoais, nível de gordura, composição corporal, índices e gráficos. (C12-CT08)
  * Gerar e baixar o relatório "avaliação completa" em PDF pelo botão verde da linha. (C12-CT09)
  * Exibir o relatório "Avaliação Física" (Dados Básicos, Circunferências, Dobras Subcutâneas e Composição Corporal) pela ação de impressão. (C12-CT10)
  * Excluir uma avaliação mediante confirmação no modal. (C12-CT11)

---

### 💰 **RF13 - Registro e Gestão de Contas a Receber**

**Descrição**: O sistema deve permitir registrar, consultar, editar e remover contas a receber.

* **Funcionalidades esperadas**:

  * Filtrar por Código, Nome do cliente, Tipo de Data (Vencimento/Recebimento), Data Inicial/Final e Status. (C13-CT01)
  * Cadastrar conta pelo botão **Nova Conta**: buscar cliente, parametrizar cópias, preencher os dados do recebimento e validar campos obrigatórios. (C13-CT02)
  * Exibir restrições e alertas ao salvar com campos obrigatórios em branco (cliente, valor a receber, tipo de pagamento, local de recebimento e caixa fechado). (C13-CT03)
  * Atualizar datas, grid e cards pelos atalhos de período (*Hoje*, *Ontem*, *Últimos 7 dias*, *Este mês*). (C13-CT04)
  * Visualizar os detalhes de uma conta recebida e editar valores com o aviso de **Ajuste Administrativo**. (C13-CT05)
  * Remover um lançamento mediante confirmação. (C13-CT06)

---

### 💸 **RF14 - Registro de Contas a Pagar**

**Descrição**: O sistema deve permitir o gerenciamento das contas a pagar da academia.

* **Funcionalidades esperadas**:

  * Excluir uma conta a pagar na listagem mediante confirmação no modal. (C14-CT04)

---

### 🏋️ **RF15 - Gerenciamento de Fichas de Treino**

**Descrição**: O sistema deve permitir consultar as fichas de treino dos alunos.

* **Funcionalidades esperadas**:

  * Filtrar a listagem por código de ficha (ex.: "236") e por Status (Ativo, Inativo, Cancelado, Finalizado). No teste, a filtragem por status ou código isolado não retornou registros correspondentes. (C15-CT01)

---

### 💪 **RF16 - Gerenciamento de Exercícios**

**Descrição**: O sistema deve manter a biblioteca de exercícios vinculados a grupos musculares.

* **Funcionalidades esperadas**:

  * Criar exercício vinculado a um grupo muscular, preenchendo o nome e anexando imagens e vídeos demonstrativos. (C16-CT01)
  * Visualizar e alterar um exercício cadastrado (nome ou dados complementares). (C16-CT02)
  * Remover um exercício vinculado a um grupo muscular pelo botão de exclusão com confirmação no modal. (C16-CT03)

---

### 🦵 **RF17 - Gestão de Grupos Musculares**

**Descrição**: O sistema deve permitir o gerenciamento dos grupos musculares.

* **Funcionalidades esperadas**:

  * Filtrar por Código, Nome e Tipo Membro e limpar os filtros. (C17-CT01)
  * Incluir grupo muscular com Nome, Tipo Membro e imagem. (C17-CT02)
  * Alterar o nome e a imagem de um grupo cadastrado. (C17-CT03)
  * Excluir grupo muscular pela listagem, com confirmação. (C17-CT05)

---

### 🎯 **RF18 - Gerenciamento de Objetivos Treino**

**Descrição**: O sistema deve permitir consultar os objetivos de treino cadastrados.

* **Funcionalidades esperadas**:

  * Buscar e filtrar pelo campo **Nome** na listagem de Objetivos de Treino. (C18-CT02)

---

### 🗂️ **RF19 - Gestão de Grupos**

**Descrição**: O sistema deve permitir o gerenciamento de grupos (financeiro/administrativos).

* **Funcionalidades esperadas**:

  * Filtrar por Código, Nome, Status e Tipo de Caixa. (C19-CT01)
  * Registrar novo grupo preenchendo os campos obrigatórios e definindo o status como inativo. (C19-CT02)
  * Exigir o preenchimento dos campos essenciais ao salvar um grupo. (C19-CT03)
  * Alterar código, descrição, tipo de caixa e status de grupos cadastrados. (C19-CT04)
  * Validar a integridade referencial ao excluir um grupo com vínculos ativos. (C19-CT05)

---

### 🧑‍🤝‍🧑 **RF20 - Gestão de Turmas**

**Descrição**: O sistema deve permitir o gerenciamento das turmas da academia.

* **Funcionalidades esperadas**:

  * Filtrar por Nome da Turma, Código e Status e limpar filtros. (C20-CT01)
  * Cadastrar turma com nome, plano, aula experimental, tempo, horários, personal e dias da semana. (C20-CT02)
  * Exibir validações ao salvar sem preencher nome, plano, dia da semana e personal. (C20-CT03)
  * Remover uma turma do sistema. (C20-CT05)

---

### 🥋 **RF21 - Gestão de Categorias Crossfit**

**Descrição**: O sistema deve permitir o gerenciamento das categorias de CrossFit.

* **Funcionalidades esperadas**:

  * Filtrar pelo campo de busca por Código. (C21-CT01)
  * Cadastrar nova categoria preenchendo o nome. (C21-CT02)
  * Emitir aviso de campo obrigatório ao salvar sem o nome. (C21-CT03)
  * Manter a consistência da listagem após a inclusão de novas categorias. (C21-CT04)
  * Alterar o nome de uma categoria pelo modal de edição. (C21-CT05)
  * Tratar o erro ao excluir uma categoria com dependências/vínculos. (C21-CT06)

---

### 🏢 **RF22 - Gestão de Box (Turmas e Modalidades)**

**Descrição**: O sistema deve permitir o gerenciamento de modalidades e turmas recorrentes do Box.

* **Funcionalidades esperadas**:

  * Cadastrar modalidade preenchendo o nome no painel de Modalidades. (C22-CT01)
  * Cadastrar turma recorrente vinculada a uma modalidade, com horário e vagas. (C22-CT02)
  * Editar nome e status de uma modalidade. (C22-CT03)
  * Editar dados de uma turma recorrente (nome, modalidade, horários, vagas, dias da semana e status). (C22-CT04)
  * Excluir modalidade na tabela de modalidades. (C22-CT05)
  * Remover turma recorrente na listagem de turmas do Box. (C22-CT06)

---

### 🧮 **RF23 - Gerenciamento e Filtro de Caixas no Módulo Financeiro**

**Descrição**: O sistema deve permitir abrir, consultar e fechar caixas no módulo financeiro.

* **Funcionalidades esperadas**:

  * Abrir novo caixa selecionando um local de contas válido. (C23-CT01)
  * Filtrar caixas por status ("Aberto"/"Fechado") e intervalo de datas. (C23-CT02)
  * Visualizar as entradas na aba **Ver Entradas** do painel de fechamento. (C23-CT03)
  * Visualizar as saídas/despesas na aba **Ver Saídas** do painel de fechamento. (C23-CT04)
  * Obrigar o preenchimento do campo **"Motivo"** ao registrar divergência na conferência física do caixa. (C23-CT05)
  * Tratar a busca de contas com parâmetros ou locais que gerem conflito na janela de fechamento. (C23-CT06)
  * Gerar e imprimir o relatório oficial de fechamento de caixa em PDF. (C23-CT07)

---

### 💳 **RF24 - Gestão Financeira e Cobranças via Pagar.me**

**Descrição**: O sistema deve integrar-se ao Pagar.me para consulta de valores, recebíveis, saques, assinaturas e cobranças.

* **Funcionalidades esperadas**:

  * Abrir o modal de valores **Em processamento** com prazos de liberação. (C24-CT01)
  * Consultar **Recebíveis Futuros** e exibir listagem ou mensagem de retorno. (C24-CT02)
  * Preencher e solicitar saque de valores disponíveis. (C24-CT03)
  * Abrir o **Relatório — Assinaturas Ativas** a partir do painel financeiro. (C24-CT04)
  * Alterar o período do gráfico de **Recebimentos** (7, 30 e 90 dias). (C24-CT05)
  * Consultar o **Extrato de Transações** pelo atalho nas transações recentes. (C24-CT06)
  * Gerar cobrança avulsa com descrição, valor e método de pagamento. (C24-CT07)
  * Redirecionar para as **Configurações** gerais de integração. (C24-CT08)
  * Verificar registros no extrato pelo botão de listagem completa de repasses/transações. (C24-CT09)
  * Visualizar indicadores de **Repasses**, **Assinaturas** e **Chargebacks** na visão geral. (C24-CT10)

---

### 🧾 **RF25 - Gerenciamento e Cadastro de Despesas Fixas**

**Descrição**: O sistema deve permitir o gerenciamento das despesas fixas da academia.

* **Funcionalidades esperadas**:

  * Buscar e filtrar despesas fixas por nome e recorrência. (C25-CT01)
  * Cadastrar despesa fixa com todos os campos obrigatórios no modal. (C25-CT02)
  * Editar valor, status ou recorrência de uma despesa existente. (C25-CT03)
  * Remover definitivamente uma despesa fixa mediante confirmação em modal. (C25-CT04)
  * Exibir erros/alertas ao salvar despesa com campos vazios. (C25-CT05)

---

### 📈 **RF26 - Geração e Filtragem de Relatórios Operacionais e Financeiros**

**Descrição**: O sistema deve permitir a geração de relatórios diversos com filtros personalizados.

* **Funcionalidades esperadas**:

  * Exibir o painel central de relatórios com os modelos disponíveis. (C26-CT01)
  * Emitir o relatório de "Avaliações" por intervalo de datas. (C26-CT02)
  * Emitir o relatório de "Clientes" por período. (C26-CT03)
  * Emitir relatórios dos colaboradores por período. (C26-CT04)
  * Emitir o relatório de "Matrículas" filtrando por planos e período. (C26-CT05)
  * Emitir o relatório de "Contas a Receber" com filtros de status, forma de pagamento e formato detalhado. (C26-CT06)
  * Emitir o relatório de "Contas a Pagar" por período de vencimento ou pagamento. (C26-CT07)
  * Emitir o relatório de "Caixas" alternando entre formato "Normal" e "Detalhado". (C26-CT08)

---

### 🧑‍💼 **RF27 - Gestão de Colaboradores**

**Descrição**: O sistema deve permitir o gerenciamento completo de colaboradores.

* **Funcionalidades esperadas**:

  * Filtrar e retornar o colaborador pesquisado por código ou nome. (C27-CT01)
  * Cadastrar novo colaborador com dados válidos. (C27-CT02)
  * Alterar dados cadastrais e status de um colaborador existente. (C27-CT03)
  * Gerenciar, vincular ou adicionar funções (ex.: "Treinador da academia", "Personal"). (C27-CT04)
  * Exibir perfil detalhado com informações e métricas consolidadas. (C27-CT05)
  * Impedir o cadastro e sinalizar a obrigatoriedade com campos obrigatórios vazios. (C27-CT06)
  * Remover definitivamente um colaborador mediante confirmação em modal. (C27-CT07)

---

### 🛡️ **RF28 - Gestão de Funções**

**Descrição**: O sistema deve permitir gerenciar funções e as permissões de acesso associadas.

* **Funcionalidades esperadas**:

  * Filtrar funções por nome, código e tipo (interno ou externo). (C28-CT01)
  * Impedir o cadastro e sinalizar a obrigatoriedade com campos em branco. (C28-CT02)
  * Cadastrar função com nome, tipo de funcionário e parâmetros relacionados. (C28-CT03)
  * Visualizar e alterar as permissões de acesso de uma função. (C28-CT04)
  * Exibir o modal com os dados detalhados de uma função. (C28-CT05)

---

### 🚚 **RF29 - Gerenciamento de Fornecedores**

**Descrição**: O sistema deve permitir o gerenciamento dos fornecedores cadastrados.

* **Funcionalidades esperadas**:

  * Buscar e filtrar por código ou nome. (C29-CT01)
  * Cadastrar fornecedor no modal "Novo Fornecedor" com campos obrigatórios e complementares. (C29-CT02)
  * Impedir o cadastro e emitir alertas com campos obrigatórios vazios. (C29-CT03)
  * Exibir as informações consolidadas do fornecedor na visualização de cadastro. (C29-CT04)
  * Exigir confirmação em modal ao excluir e processar a remoção. (C29-CT05)

---

### 📄 **RF30 - Gerenciamento de Tipos de Documentos**

**Descrição**: O sistema deve permitir o gerenciamento dos tipos de documentos e suas aplicações.

* **Funcionalidades esperadas**:

  * Filtrar por código, nome ou aplicação. (C30-CT01)
  * Criar tipo de documento definindo nome e aplicação. (C30-CT02)
  * Impedir o salvamento e avisar quando o nome estiver vazio. (C30-CT03)
  * Alterar dados (como a aplicação) de um tipo existente. (C30-CT04)
  * Solicitar confirmação via modal ao excluir e processar a remoção. (C30-CT05)

---

### 🏃 **RF31 - Gerenciamento de Atividades**

**Descrição**: O sistema deve permitir o gerenciamento das atividades da academia.

* **Funcionalidades esperadas**:

  * Filtrar atividades por nome ou código. (C31-CT01)
  * Cadastrar atividade pelo modal "Atividade". (C31-CT02)
  * Visualizar e atualizar as informações de uma atividade. (C31-CT04)
  * Excluir atividade mediante confirmação. (C31-CT05)

---

### 🏆 **RF32 - Gerenciamento de Pontuações**

**Descrição**: O sistema deve permitir gerenciar campanhas de pontuação, suas atividades e o ranking de participantes.

* **Funcionalidades esperadas**:

  * Filtrar por código, nome da pontuação e status (Ativo/Inativo). (C32-CT01)
  * Criar pontuação (campanha) com período, tipo, status e produtos de resgate. (C32-CT02)
  * Vincular atividades pelo modal "Atividades da Pontuação". (C32-CT04)
  * Visualizar o ranking de participantes de uma pontuação. (C32-CT05)
  * Excluir pontuação após confirmação. (C32-CT07)

---

### 🛍️ **RF33 - Gerenciamento de Produtos**

**Descrição**: O sistema deve permitir o gerenciamento de produtos de venda e de pontuação.

* **Funcionalidades esperadas**:

  * Filtrar por Código, Nome, Status (Ativo/Inativo) e Tipo (Venda/Pontuação). (C33-CT01)
  * Cadastrar produto com Nome, Descrição, Tipo, Pontuação e Imagem. (C33-CT02)
  * Alterar as informações de um produto cadastrado. (C33-CT03)
  * Solicitar confirmação antes de remover um produto. (C33-CT04)

---

### 🗳️ **RF34 - Módulo de Enquetes**

**Descrição**: O sistema deve permitir consultar e excluir enquetes.

* **Funcionalidades esperadas**:

  * Filtrar enquetes por Código, Nome e Status (Todos/Ativo/Inativo). (C34-CT01)
  * Solicitar confirmação antes da exclusão e reportar a falha caso o registro não possa ser removido. (C34-CT04)

---

### 📣 **RF35 - Gestão e Consulta de Leads (Prospecção)**

**Descrição**: O sistema deve permitir gerenciar leads e seu estágio no funil de prospecção.

* **Funcionalidades esperadas**:

  * Buscar e filtrar leads por nome, e-mail, telefone ou código. (C35-CT01)
  * Cadastrar lead com dados pessoais, contato, observação e estágio inicial. (C35-CT02)
  * Impedir o salvamento e sinalizar a obrigatoriedade sem o nome. (C35-CT03)
  * Visualizar lead, atualizar contato/observações e alterar o estágio no funil. (C35-CT04)
  * Solicitar confirmação via modal antes de remover definitivamente. (C35-CT05)

---

### 📋 **RF36 - Gestão e Consulta de Planos**

**Descrição**: O sistema deve permitir o gerenciamento dos planos oferecidos pela academia.

* **Funcionalidades esperadas**:

  * Filtrar por código, nome ou status (Ativo/Inativo). (C36-CT01)
  * Cadastrar plano com dados básicos, valores, períodos de cobrança e regras de equipe/dependentes. (C36-CT02)
  * Alterar informações e status de um plano. (C36-CT03)
  * Impedir a exclusão de plano com vínculos ativos, exibindo mensagem de erro. (C36-CT04)
  * Impedir o salvamento e sinalizar a obrigatoriedade sem os campos essenciais. (C36-CT05)

---

### 📑 **RF37 - Gestão de Modelos de Contrato**

**Descrição**: O sistema deve permitir criar modelos de contrato com tags dinâmicas e pré-visualização.

* **Funcionalidades esperadas**:

  * Redirecionar para a tela de adição ao clicar em novo modelo de contrato. (C37-CT01)
  * Gerar e atualizar a pré-visualização conforme o texto digitado no editor. (C37-CT02)
  * Incluir tags dinâmicas de dados do aluno. (C37-CT03)
  * Incluir tags dinâmicas de dados do plano contratado. (C37-CT04)
  * Incluir tags dinâmicas de dados da academia. (C37-CT05)
  * Incluir tags dinâmicas de informações contratuais específicas. (C37-CT06)
  * Expandir e recolher o painel completo de variáveis disponíveis. (C37-CT07)

---

### 💵 **RF38 - Gestão de Tipos de Pagamento**

**Descrição**: O sistema deve permitir o gerenciamento dos tipos de pagamento aceitos.

* **Funcionalidades esperadas**:

  * Validar o preenchimento obrigatório ao cadastrar tipo de pagamento em branco. (C38-CT01)
  * Buscar e filtrar por código, nome ou status. (C38-CT02)
  * Cadastrar tipo de pagamento com campos obrigatórios, status, bandeira e integração. (C38-CT03)
  * Alterar as configurações de um tipo existente. (C38-CT04)
  * Bloquear a remoção de tipos vinculados a outras operações, com mensagem de erro adequada. (C38-CT05)

---

### 💳 **RF39 - Gestão de Bandeiras de Cartão**

**Descrição**: O sistema deve permitir cadastrar e consultar bandeiras de cartão com suas taxas e regras de parcelamento.

* **Funcionalidades esperadas**:

  * Abrir o modal "Nova Bandeira" com campos limpos e validar o nome obrigatório ao salvar. (C39-CT01)
  * Preencher nome, taxas adicionais, taxa de débito e adicionar regras de parcelamento. (C39-CT02)
  * Consultar e filtrar bandeiras cadastradas pelos campos de busca. (C39-CT03)

---

### 🩺 **RF40 - Aplicação de Fichas de Anamnese**

**Descrição**: O sistema deve permitir consultar as fichas de anamnese aplicadas.

* **Funcionalidades esperadas**:

  * Filtrar e consultar fichas pelo seletor de status e pela barra de pesquisa na tela principal. (C40-CT03)

---

### 🩺 **RF41 - Gerenciamento de Modelos de Anamnese**

**Descrição**: O sistema deve permitir gerenciar os modelos de anamnese e suas perguntas.

* **Funcionalidades esperadas**:

  * Exibir o modal de confirmação e remover definitivamente um modelo. (C41-CT01)
  * Alterar o status de um modelo de "Ativo" para "Inativo" na tela de edição. (C41-CT02)
  * Filtrar modelos por status (Ativo, Inativo ou Todos). (C41-CT03)
  * Cadastrar novo modelo com informações gerais e status inicial. (C41-CT04)
  * Adicionar perguntas ao modelo pelo montador visual, com marcação de campos obrigatórios. (C41-CT05)

---

### 🩺 **RF42 - Gerenciamento de Categorias de Anamnese**

**Descrição**: O sistema deve permitir gerenciar as categorias de anamnese.

* **Funcionalidades esperadas**:

  * Cadastrar categoria com nome, status, ícone e cor visual. (C42-CT01)
  * Impedir o salvamento e sinalizar a obrigatoriedade sem o nome. (C42-CT02)
  * Alterar status, nome, ícone ou cor de uma categoria. (C42-CT03)
  * Filtrar o grid por status (Ativo/Inativo) e buscar por termos. (C42-CT04)
  * Solicitar confirmação via modal e remover permanentemente uma categoria. (C42-CT05)

---

### 🩺 **RF43 - Gestão de Perguntas de Anamnese**

**Descrição**: O sistema deve permitir gerenciar as perguntas utilizadas nas fichas de anamnese.

* **Funcionalidades esperadas**:

  * Exibir o modal de confirmação e remover definitivamente uma pergunta. (C43-CT01)
  * Exibir a mensagem de erro correspondente ao tentar alterar o tipo de resposta de uma pergunta cadastrada. (C43-CT02)
  * Cadastrar pergunta com código, nome, texto e tipo de resposta. (C43-CT03)
  * Validar o preenchimento obrigatório ao salvar com dados incompletos. (C43-CT04)
  * Filtrar por código, nome e status (Ativo/Inativo). (C43-CT05)

---

### 🤖 **RF44 - Módulo Inteligência & Automação e Gestão de Clientes**

**Descrição**: O sistema deve oferecer análise de risco de evasão, automações e ações rápidas sobre o cliente.

* **Funcionalidades esperadas**:

  * Direcionar para "Inteligência & Automação" e renderizar cards de métricas, automações ativas e histórico de atividades. (C44-CT01)
  * Filtrar o Relatório de Risco de Evasão por categoria (*Alto risco*, *Médio*, *Baixo risco*). (C44-CT02)
  * Exibir aviso ao acionar manualmente a automação de Aniversariantes. (C44-CT03)
  * Alterar frequência, critérios de análise e sensibilidade da automação de Risco de Evasão, com validação de destinatários obrigatórios. (C44-CT04)
  * Ajustar a frequência personalizada na configuração da automação de Aniversariantes. (C44-CT05)
  * Expandir o painel lateral de detalhes ao selecionar um aluno do Relatório de Risco de Evasão. (C44-CT06)
  * Acionar as ações rápidas (*Registrar pagamento*, *Agendar avaliação*, *Enviar mensagem*) na tela do cliente. (C44-CT07)
  * Expandir e interagir com os cards de "Automações disponíveis" (*Avaliações vencendo*, *Frequência em queda*, *Financeiro diário*, *Cobranças automáticas*). (C44-CT08)
  * Registrar e finalizar o pagamento de mensalidade pendente pelas Ações Rápidas do perfil do cliente. (C44-CT09)

---

### 📉 **RF45 - Visualização e Filtragem do Dashboard de Resultados da Inteligência**

**Descrição**: O sistema deve exibir os resultados da Inteligência em dashboard filtrável por período.

* **Funcionalidades esperadas**:

  * Atualizar indicadores, gráficos e listas conforme o período temporal selecionado. (C45-CT01)

---

### ⚙️ **RF46 - Gestão de Configurações**

**Descrição**: O sistema deve permitir configurar parâmetros gerais, integrações e identidade visual.

* **Funcionalidades esperadas**:

  * Alterar parâmetros de acesso e presença na aba "Home", com a mensagem de erro ao persistir. (C46-CT01)
  * Preencher IP, porta e modelo da catraca na aba "Biometria" e salvar. (C46-CT02)
  * Alterar regras de avaliação (cobrança, tipo e dias de validade) na aba "Avaliação". (C46-CT03)
  * Habilitar e editar templates de aniversário (WhatsApp, SMS, E-mail) na aba "Aniversário". (C46-CT04)
  * Alterar parâmetros de pagamento online e inserir token de integração na aba "Pagamento". (C46-CT05)
  * Gerir integrações de API na aba "Integrações", preenchendo credenciais do WhatsApp. (C46-CT06)
  * Alterar cores principais/secundárias e enviar logotipo e capa na aba "Design". (C46-CT07)

---

### 🧩 **RF47 - Gerenciamento de Modelos de Ficha**

**Descrição**: O sistema deve permitir cadastrar e consultar modelos de ficha de treino.

* **Funcionalidades esperadas**:

  * Preencher o formulário de um novo modelo de ficha e submeter a gravação. (C47-CT01)
  * Buscar e filtrar a listagem por código, título e criador. (C47-CT02)

---

### 🔔 **RF48 - Gerenciamento de Notificações**

**Descrição**: O sistema deve permitir consultar, criar, enviar e excluir notificações e conteúdos do aplicativo.

* **Funcionalidades esperadas**:

  * Abrir e fechar o modal "Todas as notificações" e exibir o estado da seção de Denúncias. (C48-CT01)
  * Abrir o modal "Todas as postagens" e alternar "Ver todas" e "Só pendentes" em Postagens e Denúncias. (C48-CT02)
  * Abrir o modal de criação, preencher a mensagem com prévia no celular e enviar o aviso aos alunos. (C48-CT03)
  * Abrir o painel de notificações pelo ícone de sino e alternar entre "Tudo" e "Não lidas". (C48-CT04)
  * Transitar do modal "Todas as notificações" para o de criação e bloquear o envio com mensagem vazia. (C48-CT05)
  * Exibir os detalhes de uma notificação enviada pelo ícone de lupa. (C48-CT06)
  * Excluir notificação pelo ícone de lixeira na listagem. (C48-CT07)

---

### 🌗 **RF49 - Alternância de Tema da Interface (Claro / Escuro)**

**Descrição**: O sistema deve permitir alternar o tema visual da interface.

* **Funcionalidades esperadas**:

  * Alterar o tema do modo Claro para o modo Escuro. (C49-CT01)
  * Retornar o tema do modo Escuro para o modo Claro. (C49-CT02)


