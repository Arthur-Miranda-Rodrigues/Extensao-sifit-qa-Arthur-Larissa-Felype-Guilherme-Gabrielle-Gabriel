# 📋 **Análise de Requisitos — SIFIT**

🏋️ **Projeto:** SIFIT — Sistema de gestão para academia/box  
📄 **Documento:** Análise de Requisitos Funcionais e Não Funcionais  
🧪 **Base de elaboração:** 49 arquivos de cenários de teste fornecidos no projeto de QA do SIFIT  
👨‍💻 **Responsável pelo trabalho:** Arthur Miranda Rodrigues, Larissa Fernanda O., Felype Augusto Dos Santos Silva, Guilherme Felipe de Morais, Gabrielle Bonini Barbosa, Gabriel de Abreu da Silva  
🔖 **Versão:** 2.0  
📅 **Data:** 23/10/2026  

---

## 🎯 1. Objetivo

Este documento consolida os requisitos funcionais identificados nos 49 cenários de teste do SIFIT. Cada requisito foi detalhado e correlacionado diretamente a partir do objetivo dos casos de teste existentes, preservando a rastreabilidade, os módulos, os fluxos e os comportamentos observados nos arquivos de origem.

---

## 🧭 2. Escopo

A análise contempla autenticação, página inicial e dashboard, check-ins e presenças, aulas do SifitBox, clientes, matrículas, avaliações físicas, contas a receber, contas a pagar, fichas de treino, exercícios, grupos musculares, objetivos de treino, grupos financeiro/administrativos, turmas, categorias CrossFit, turmas do box, caixas e fechamentos, integração Pagar.me, despesas fixas, relatórios operacionais e financeiros, colaboradores, funções e permissões, fornecedores, tipos de documentos, atividades, pontuações e programas de fidelidade, produtos, enquetes, prospecção e leads, planos, modelos de contrato, tipos de pagamento, bandeiras de cartão, fichas/modelos/categorias/perguntas de anamnese, inteligência e retenção, configurações gerais, modelos de ficha, notificações/conteúdos do aplicativo e alternância de temas.

---

## 📝 3. Convenções

- **RFxx:** Requisito Funcional associado ao cenário de teste correspondente.
- **CT:** Referência ao caso de teste específico descrito no arquivo de origem (ex.: `C01-CT01`).
- **Comportamento observado no teste:** Registros onde o teste evidencia validação de erros de preenchimento, limitações de interface ou falhas tratadas pelo sistema.

---

## 📦 4. Requisitos Funcionais

---

### 🧩 RF01 — Login na plataforma

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C01-CT01:** O login será realizado com um nome de usuário e uma senha válidos na plataforma SIFIT.
- **🧪 C01-CT02:** O login falhará quando o nome de usuário ou a senha forem inválidos.
- **🧪 C01-CT03:** O login falhará quando os campos de login e senha forem apagados ou mantidos em branco.
- **🧪 C01-CT04:** O sistema deve redirecionar o usuário para a interface de recuperação/redefinição de senha ao acionar o link correspondente na tela de login.

📎 **Fonte:** `CT_RF01_Login na plataforma.md`

---

### 🧩 RF02 — Acesso à Página Inicial (Parte 1)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C02-CT01:** Validar a abertura e a busca por nome de alunos no modal de "Clientes Sem Matrículas" a partir da Página Inicial.
- **🧪 C02-CT02:** Validar a consulta detalhada de alunos sumidos ou ausentes há mais tempo na academia.
- **🧪 C02-CT03:** Validar o redirecionamento direto da Página Inicial para a tela de gestão de Avaliações físicas.
- **🧪 C02-CT04:** Validar a exibição do modal de mensalidades pendentes e a alternância de atalhos por período de atraso.
- **🧪 C02-CT05:** Validar a abertura do Radar de Evasão e a visualização das regras de pontuação/risco de cancelamento do aluno.

📎 **Fonte:** `CT_RF02_Acesso A Pagina Inicial Parte 1.md`

---

### 🧩 RF03 — Acesso à Página Inicial (Parte 2)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C03-CT01:** Verificar se o modal/painel de "Mensalidades pendentes / Financeiro em Aberto" abre corretamente ao clicar em "Ver detalhes" e se os filtros por período de vencimento funcionam adequadamente.
- **🧪 C03-CT02:** Validar a exibição do modal de "Desistências no Período" ao clicar no card correspondente e testar a busca por nome ou código.
- **🧪 C03-CT03:** Validar a abertura e o funcionamento da pesquisa no modal "Matrículas no Período" a partir do card do Dashboard.
- **🧪 C03-CT04:** Verificar se a modalidade/card de "Personais" abre a lista de profissionais cadastrados e permite a busca individualizada.
- **🧪 C03-CT05:** Validar a expansão do modal "Agenda de hoje" ao clicar em "Ver agenda", a busca por aulas, a seleção de unidades e a alteração dinâmica de detalhes ao selecionar aulas como *Turma dos Bodybuilders*, *Teste* e *Horario da manhã*, disponibilizando os botões de ações rápidas.

📎 **Fonte:** `CT_RF03_Acesso A Pagina Inicial Parte 2.md`

---

### 🧩 RF04 — Acesso à Página Inicial (Parte 3)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C04-CT01:** Validar a abertura do modal "Falar com inativos" a partir da seção "Ações recomendadas para hoje", a busca por alunos, personalização de mensagem e seleção do canal de envio.
- **🧪 C04-CT02:** Verificar a funcionalidade do card "Cobrar alunos", validando a abertura do modal de cobrança, busca por alunos inadimplentes e personalização da mensagem de cobrança segura.
- **🧪 C04-CT03:** Validar o redirecionamento ao clicar em "Ver todos" na seção "Aniversariantes do dia" e a filtragem no modal por período (7 dias, 33 dias) e navegação mensal no calendário.
- **🧪 C04-CT04:** Garantir que o link "Ver todos" no bloco "Últimas entradas na academia" redireciona o utilizador para a tela operacional de Presenças.
- **🧪 C04-CT05:** Validar o direcionamento para a "Central de Automações" através do link "Ver análise completa" na seção de Inteligência de Retenção e a interação com a execução de automações e relatórios de risco de evasão.

📎 **Fonte:** `CT_RF04_Acesso A Pagina Inicial Parte 3.md`

---

### 🧩 RF05 — Acesso à Página Inicial (Parte 4)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C05-CT01:** Validar a abertura do modal "Cadastrar Avaliação" a partir do painel de Ações Rápidas, a busca/substituição do aluno, seleção do personal responsável, data e horário, finalizando com o salvamento da avaliação.
- **🧪 C05-CT02:** Validar o envio e troca de templates de mensagem (Falta, Cobrança, Retorno de treino, Aniversário, Avaliação) através das Ações Rápidas do painel "Inteligência Sifit" do cliente.
- **🧪 C05-CT03:** Validar a edição completa dos dados de um cliente (RG, foto de perfil, telefones, endereço, biometria e dados adicionais) salvando as alterações.
- **🧪 C05-CT04:** Verificar o direcionamento do modal "Clientes Sem Matrículas" (acessado pelos cards do Dashboard) para a tela de visualização do perfil do cliente.
- **🧪 C05-CT05:** Garantir o correto direcionamento da ação rápida "Ver avaliações" no card de Ações Recomendadas para a tela de gestão de Avaliações.

📎 **Fonte:** `CT_RF05_Acesso A Pagina Inicial Parte 4.md`

---

### 🧩 RF06 — Acesso à Página Inicial (Parte 5)

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C06-CT01:** Validar o direcionamento do modal "Personais" para a tela "Visualizar Cliente" ao clicar na ação correspondente do profissional cadastrado.
- **🧪 C06-CT02:** Validar o fluxo de aplicação de anamnese para o aluno, selecionando o modelo disponível, preenchendo o questionário e finalizando o processo.
- **🧪 C06-CT03:** Garantir a visualização do modal de histórico de presenças a partir do painel de desempenho do cliente.
- **🧪 C06-CT04:** Validar o comportamento do modal "Registrar pagamento" através das Ações Rápidas do cliente quando o aluno não possui contas pendentes.

📎 **Fonte:** `CT_RF06_Acesso A Pagina  Inicial Parte 5.md`

---

### 🧩 RF07 — Acesso e Visualização do Dashboard

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C07-CT01:** Verificar o direcionamento para a tela "Dashboard" pelo menu lateral, a correta renderização dos painéis e o comportamento de alternância/mudança de tema de cores ao recarregar a página.
- **🧪 C07-CT02:** Validar a interatividade dos gráficos do Dashboard ao posicionar o cursor sobre as barras e seções, conferindo a exibição das etiquetas informativas (*tooltips*).
- **🧪 C07-CT03:** Validar o acionamento do botão "Ver Inteligência" no card "Inteligência Sifit" e a atualização das métricas ao alternar os filtros de período temporal.

📎 **Fonte:** `CT_RF07_ Acesso e visualiza o do Dashboard.md`

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

- **🧪 C09-CT01:** Validar a busca por nome de cliente ou código diretamente na tabela de histórico de presenças.
- **🧪 C09-CT02:** Validar a filtragem de presenças aplicando o intervalo de datas (Data Inicial e Data Final).
- **🧪 C09-CT03:** Confirmar a atualização dos dados ao acionar os atalhos de período temporal (*Hoje*, *Últimos 7 dias*, *Este mês*).
- **🧪 C09-CT04:** Validar a exportação ou visualização detalhada das informações de presença registradas.

📎 **Fonte:** `CT_RF09_Consulta e Filtragem de Presen as de Clientes.md`

---

### 🧩 RF10 — Gerenciamento de Aulas do SifitBox

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C10-CT01:** Validar a tentativa de filtragem de aulas inserindo o intervalo de datas de forma manual nos campos correspondentes.
- **🧪 C10-CT02:** Validar a tentativa de filtragem de aulas utilizando o componente de calendário interativo para escolha das datas.
- **🧪 C10-CT03:** Validar o comportamento do sistema ao definir incorretamente a data final como um período cronologicamente anterior à data inicial.
- **🧪 C10-CT04:** Validar o acionamento do botão "Gerar aulas" localizado no canto superior direito da tela.

📎 **Fonte:** `CT_RF10_ Gest o de clientes.md` *(Arquivado na suíte sob CT_RF10)*

---

### 🧩 RF11 — Gestão de Clientes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C11-CT01:** Validar o fluxo de cadastro de um novo cliente informando identificação, documentos, foto, contatos, endereço, dados biométricos, credenciais de aplicativo e informações complementares/responsável.
- **🧪 C11-CT02:** Validar o comportamento do sistema ao tentar submeter o formulário de cadastro de cliente deixando campos obrigatórios em branco.
- **🧪 C11-CT03:** Validar a atualização cadastral de um cliente existente a partir de seu perfil, alterando dados de endereço, biometria, aplicativo e dados complementares.
- **🧪 C11-CT04:** Validar o comportamento do sistema ao acionar a exclusão de um registro de cliente na listagem, tratando eventuais falhas de servidor.
- **🧪 C11-CT05:** Validar a consulta de clientes combinando filtros de código e nome diretamente nos campos de busca da listagem principal.

📎 **Fonte:** `CT_RF11_ Gerenciamento de Matriculas.md` *(Corresponde à Gestão de Clientes na estrutura de arquivos)*

---

### 🧩 RF12 — Gerenciamento de Matrículas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C12-CT01:** Validar a filtragem da listagem de matrículas utilizando os campos de busca por nome e por código numérico.
- **🧪 C12-CT02:** Garantir que o sistema bloqueie a gravação e exiba aviso quando o utilizador tentar cadastrar uma matrícula sem selecionar um cliente associado.
- **🧪 C12-CT03:** Verificar se é possível abrir os detalhes de uma matrícula existente, habilitar a edição, alterar o campo de observação e persistir as modificações.
- **🧪 C12-CT04:** Validar o fluxo de cancelamento de uma matrícula ativa através da ação específica na listagem de registros.
- **🧪 C12-CT05:** Validar o comportamento do sistema ao acionar a exclusão de um registro de matrícula na listagem.

📎 **Fonte:** `CT_RF12_ Gestao de avalia es.md` *(Mapeamento do CT_RF12)*

---

### 🧩 RF13 — Gerenciamento de Avaliações Físicas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C13-CT01:** Validar os filtros por Código, Nome e Status (Todos / Pendente / Realizado) e a exibição dos indicadores no topo da tela "Avaliações".
- **🧪 C13-CT02:** Validar o fluxo do modal "Cadastrar Avaliação": busca do aluno por código ou nome, seleção do personal responsável, data e hora.
- **🧪 C13-CT03:** Verificar as mensagens de aviso ao tentar salvar a avaliação sem aluno, sem personal ou sem hora.
- **🧪 C13-CT04:** Validar o lançamento das medidas em centímetros e milímetros e a exibição automática da aba "Composição" na avaliação de um aluno.
- **🧪 C13-CT05:** Validar o modal "Alterar Data / Hora da avaliação" para uma avaliação com status Pendente.
- **🧪 C13-CT06:** Validar o preenchimento da aba "IMC" (idade, altura e peso) em uma avaliação pendente e a mudança de status ao salvar.
- **🧪 C13-CT07:** Validar o modal "Comparar Avaliação" entre uma avaliação antiga e uma nova do mesmo aluno.
- **🧪 C13-CT08:** Validar a página "Sua Avaliação Física" com dados pessoais, nível de gordura, composição corporal, índices e gráficos.
- **🧪 C13-CT09:** Validar a geração e o download do relatório "Avaliação completa" em PDF pelo botão correspondente na linha.
- **🧪 C13-CT10:** Validar o relatório "Avaliação Física" (Dados Básicos, Circunferências, Dobras Subcutâneas e Composição Corporal) aberto pela ação de impressão.
- **🧪 C13-CT11:** Validar a exclusão de uma avaliação mediante confirmação no modal.

📎 **Fonte:** `CT_RF13_ Registro de contas a receber.md` *(Mapeamento do CT_RF13)*

---

### 🧩 RF14 — Registro e Gestão de Contas a Receber

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C14-CT01:** Validar os filtros da listagem de Contas a Receber: Código, Nome do cliente, Tipo de Data (Vencimento/Recebimento), Data Inicial/Final e Status.
- **🧪 C14-CT02:** Validar o cadastro de uma conta a receber pelo botão Nova Conta, incluindo a busca de cliente, a parametrização de cópias, o preenchimento dos dados do recebimento e a validação de campos obrigatórios.
- **🧪 C14-CT03:** Validar as restrições e mensagens de alerta emitidas pelo sistema ao tentar salvar uma nova conta a receber com campos obrigatórios em branco.
- **🧪 C14-CT04:** Validar os botões de atalho de período (*Hoje*, *Ontem*, *Últimos 7 dias* e *Este mês*) na atualização das datas, da grid e dos cards.
- **🧪 C14-CT05:** Validar a visualização dos detalhes de uma conta recebida e a edição dos valores com o aviso de Ajuste Administrativo.
- **🧪 C14-CT06:** Validar a remoção de um lançamento na listagem de Contas a Receber mediante confirmação.

📎 **Fonte:** `CT_RF14_ Registro de contas a pagar.md` *(Mapeamento do CT_RF14)*

---

### 🧩 RF15 — Registro de Contas a Pagar

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C15-CT01:** Validar o registro de uma nova conta a pagar por meio do botão Nova Conta, utilizando o modal Buscar Fornecedor e o preenchimento dos dados da conta e do documento.
- **🧪 C15-CT02:** Validar o funcionamento dos filtros por nome (fornecedor ou colaborador), tipo de data (Vencimento/Pagamento), período (Data Inicial/Final) e status na listagem de Contas a Pagar.
- **🧪 C15-CT03:** Confirmar se os dados do registro são apresentados de forma íntegra no modal Visualizar Conta a Pagar.
- **🧪 C15-CT04:** Validar a exclusão de uma conta a pagar na listagem mediante confirmação no modal.

📎 **Fonte:** `CT_RF15_ Consulta de ficha de treino.md` *(Mapeamento do CT_RF15)*

---

### 🧩 RF16 — Gerenciamento de Fichas de Treino

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C16-CT01:** Validar o comportamento da listagem ao aplicar filtros por código de ficha e diferentes opções de Status (Ativo, Inativo, Cancelado, Finalizado).
- **🧪 C16-CT02:** Validar o fluxo de abertura do formulário de cadastro de ficha, preenchimento dos dados (aluno, personal, datas, objetivo e observação) e o tratamento de validações do registro.

📎 **Fonte:** `CT_RF16_ Gerenciamento de Exerc cios.md` *(Mapeamento do CT_RF16)*

---

### 🧩 RF17 — Gerenciamento de Exercícios

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C17-CT01:** Validar a criação de um novo exercício e sua vinculação a um grupo muscular específico preenchendo o nome e anexando imagens e vídeos demonstrativos.
- **🧪 C17-CT02:** Validar a visualização e alteração de um exercício já cadastrado na biblioteca, atualizando seu nome ou dados complementares.
- **🧪 C17-CT03:** Validar a remoção de um exercício vinculado a um grupo muscular por meio do botão de exclusão e confirmação no modal.

📎 **Fonte:** `CT_RF17_ Gest o de grupos musculares.md` *(Mapeamento do CT_RF17)*

---

### 🧩 RF18 — Gestão de Grupos Musculares

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C18-CT01:** Validar o funcionamento dos filtros por Código, Nome e Tipo Membro na listagem de Grupos Musculares, e a limpeza dos filtros.
- **🧪 C18-CT02:** Validar a inclusão de um novo grupo muscular com preenchimento de Nome, Tipo Membro e anexo de imagem.
- **🧪 C18-CT03:** Validar a alteração do nome e da imagem de um grupo muscular já cadastrado.
- **🧪 C18-CT04:** Validar o tratamento de campos obrigatórios ao cadastrar um grupo muscular informando apenas a imagem.
- **🧪 C18-CT05:** Validar a exclusão de um grupo muscular pela listagem, com confirmação.

📎 **Fonte:** `CT_RF18_ Gerenciamento de objetivos treino.md` *(Mapeamento do CT_RF18)*

---

### 🧩 RF19 — Gerenciamento de Objetivos de Treino

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C19-CT01:** Verificar o comportamento do sistema ao tentar cadastrar um novo objetivo de treino e tratar validações de salvamento.
- **🧪 C19-CT02:** Validar o funcionamento da ferramenta de busca e filtragem utilizando o campo Nome na listagem de Objetivos de Treino.

📎 **Fonte:** `CT_RF19_ Gest o de grupos.md` *(Mapeamento do CT_RF19)*

---

### 🧩 RF20 — Gestão de Grupos Financeiros/Administrativos

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C20-CT01:** Validar o funcionamento dos filtros por Código, Nome, Status e Tipo de Caixa na listagem de grupos.
- **🧪 C20-CT02:** Validar o registro de um novo grupo preenchendo os campos obrigatórios e definindo o status como inativo.
- **🧪 C20-CT03:** Validar a obrigatoriedade de preenchimento dos campos essenciais ao tentar salvar um novo grupo sem as informações necessárias.
- **🧪 C20-CT04:** Verificar a alteração das configurações de código, descrição, tipo de caixa e status em grupos cadastrados.
- **🧪 C20-CT05:** Verificar a validação de integridade referencial do sistema ao tentar excluir um grupo que possui vínculos ativos.

📎 **Fonte:** `CT_RF20_ Gest o de turmas.md` *(Mapeamento do CT_RF20)*

---

### 🧩 RF21 — Gestão de Turmas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C21-CT01:** Validar o funcionamento dos filtros por Nome da Turma, Código e Status, e do botão de limpar filtros, na listagem de turmas.
- **🧪 C21-CT02:** Validar o cadastro de uma nova turma preenchendo nome, plano, aula experimental, tempo, horários, personal e dias da semana.
- **🧪 C21-CT03:** Verificar as mensagens de validação exibidas ao tentar salvar uma turma sem preencher os campos obrigatórios.
- **🧪 C21-CT04:** Verificar a alteração do nome e das configurações de personal de uma turma já cadastrada no sistema.
- **🧪 C21-CT05:** Verificar a funcionalidade de remoção de uma turma do sistema.

📎 **Fonte:** `CT_RF21_Gest o de Categorias Crossfit.md` *(Mapeamento do CT_RF21)*

---

### 🧩 RF22 — Gestão de Categorias CrossFit

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C22-CT01:** Validar a filtragem de registros na listagem utilizando o campo de busca por Código.
- **🧪 C22-CT02:** Validar o cadastramento bem-sucedido de uma nova categoria preenchendo o campo nome.
- **🧪 C22-CT03:** Validar a emissão de aviso de campo obrigatório ao tentar salvar uma categoria sem preencher o nome.
- **🧪 C22-CT04:** Validar a consistência da listagem principal após a inclusão de novas categorias.
- **🧪 C22-CT05:** Validar a alteração do nome de uma categoria existente através do modal de edição.
- **🧪 C22-CT06:** Validar o tratamento de erro do sistema ao tentar excluir uma categoria que possui dependências/vínculos.

📎 **Fonte:** `CT_RF22_Gest o de Box - Turmas.md` *(Mapeamento do CT_RF22)*

---

### 🧩 RF23 — Gestão de Box - Turmas e Modalidades

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C23-CT01:** Validar o cadastro de uma nova modalidade preenchendo o nome correspondente no painel de Modalidades.
- **🧪 C23-CT02:** Validar o cadastro de uma nova turma recorrente vinculada a uma modalidade com configuração de horário e vagas.
- **🧪 C23-CT03:** Validar a edição do nome e do status de uma modalidade existente.
- **🧪 C23-CT04:** Validar a edição dos dados de uma turma recorrente existente (nome, modalidade vinculada, horários, vagas, dias da semana e status).
- **🧪 C23-CT05:** Validar a funcionalidade de exclusão de uma modalidade cadastrada na tabela de modalidades.
- **🧪 C23-CT06:** Testar a remoção de uma turma recorrente cadastrada na listagem de turmas do Box.

📎 **Fonte:** `CT_RF23_ Gerenciamento e Filtro de Caixas .md` *(Mapeamento do CT_RF23)*

---

### 🧩 RF24 — Gerenciamento e Filtro de Caixas no Módulo Financeiro

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C24-CT01:** Validar a abertura de um novo caixa selecionando um local de contas válido no sistema.
- **🧪 C24-CT02:** Validar a filtragem dos caixas na tabela com base no status ("Aberto" ou "Fechado") e intervalo de datas.
- **🧪 C24-CT03:** Validar a visualização detalhada das entradas financeiras ao acessar a aba "Ver Entradas" no painel de fechamento do caixa.
- **🧪 C24-CT04:** Validar a visualização detalhada das saídas/despesas ao acessar a aba "Ver Saídas" no painel de fechamento do caixa.
- **🧪 C24-CT05:** Validar que o sistema obriga o preenchimento do campo "Motivo" ao registrar uma divergência na conferência física do caixa.
- **🧪 C24-CT06:** Validar o comportamento do sistema ao tentar buscar contas com parâmetros ou locais que gerem conflito na janela de fechamento de caixa.
- **🧪 C24-CT07:** Validar a funcionalidade de geração e impressão do relatório oficial de fechamento de caixa em formato PDF.

📎 **Fonte:** `CT_RF24_Gest o Financeira e Cobran as via Pagar.me.md` *(Mapeamento do CT_RF24)*

---

### 🧩 RF25 — Gestão Financeira e Cobranças via Pagar.me

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C25-CT01:** Validar a abertura do modal de consulta de valores "Em processamento" e visualização de prazos de liberação no Pagar.me.
- **🧪 C25-CT02:** Validar a consulta de Recebíveis Futuros e a listagem ou mensagem de retorno na modal correspondente.
- **🧪 C25-CT03:** Validar o fluxo de preenchimento e solicitação de saque de valores disponíveis na conta Pagar.me.
- **🧪 C25-CT04:** Validar a abertura e exibição do Relatório — Assinaturas Ativas a partir do painel financeiro.
- **🧪 C25-CT05:** Validar a alteração do período de visualização no gráfico de Recebimentos (alternando entre 7, 30 e 90 dias).
- **🧪 C25-CT06:** Validar a consulta detalhada do Extrato de Transações através do atalho na listagem de transações recentes.
- **🧪 C25-CT07:** Validar o registro e geração de uma nova cobrança avulsa preenchendo descrição, valor e selecionando o método de pagamento.
- **🧪 C25-CT08:** Validar o redirecionamento e a navegação para o painel de Configurações gerais de integração do sistema.
- **🧪 C25-CT09:** Validar a verificação de registros no extrato de transações utilizando o botão de listagem completa na tabela de repasses/transações.
- **🧪 C25-CT10:** Validar a visualização dos indicadores de Repasses, Assinaturas e Chargebacks na visão geral do Pagar.me.

📎 **Fonte:** `CT_RF25_Gerenciamento e Cadastro de Despesas Fixas.md` *(Mapeamento do CT_RF25)*

---

### 🧩 RF26 — Gerenciamento e Cadastro de Despesas Fixas

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C26-CT01:** O sistema deve permitir a busca e filtragem de despesas fixas utilizando os filtros de nome e recorrência na interface.
- **🧪 C26-CT02:** O sistema deve permitir o cadastro de uma nova despesa fixa preenchendo todos os campos obrigatórios no modal correspondente.
- **🧪 C26-CT03:** O sistema deve permitir editar os parâmetros (como valor, status ou recorrência) de uma despesa fixa já existente.
- **🧪 C26-CT04:** O sistema deve permitir a remoção definitiva de uma despesa fixa mediante confirmação em modal.
- **🧪 C26-CT05:** O sistema deve validar o preenchimento dos campos obrigatórios e exibir mensagens de erro/alerta caso o usuário tente salvar uma nova despesa com campos vazios.

📎 **Fonte:** `CT_RF26_Gera o e Filtragem de Relat rios Operacionais e Financeiros.md` *(Mapeamento do CT_RF26)*

---

### 🧩 RF27 — Geração e Filtragem de Relatórios Operacionais e Financeiros

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C27-CT01:** O sistema deve exibir o painel central de relatórios com as opções de modelos disponíveis para seleção.
- **🧪 C27-CT02:** O sistema deve permitir a emissão do relatório de "Avaliações" filtrando por um intervalo de datas específico.
- **🧪 C27-CT03:** O sistema deve permitir a emissão do relatório de "Clientes" com base no período selecionado.
- **🧪 C27-CT04:** O sistema deve permitir a emissão de relatórios referentes aos colaboradores da academia por período.
- **🧪 C27-CT05:** O sistema deve permitir a emissão do relatório de "Matrículas" aplicando filtros por planos específicos e período.
- **🧪 C27-CT06:** O sistema deve permitir a emissão do relatório de "Contas a Receber" com filtros avançados de status, forma de pagamento e formato detalhado.
- **🧪 C27-CT07:** O sistema deve permitir a emissão do relatório de "Contas a Pagar" filtrando por período de vencimento ou pagamento.
- **🧪 C27-CT08:** O sistema deve permitir a emissão do relatório de "Caixas" alternando o formato de visualização entre "Normal" e "Detalhado".

📎 **Fonte:** `CT_RF27_ Gest o de colaboradores via sistema SIFIT.md` *(Mapeamento do CT_RF27)*

---

### 🧩 RF28 — Gestão de Colaboradores

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C28-CT01:** O sistema deve filtrar e retornar corretamente o colaborador pesquisado através dos filtros de código ou nome.
- **🧪 C28-CT02:** O sistema deve permitir o cadastro bem-sucedido de um novo colaborador com o preenchimento de todos os dados válidos.
- **🧪 C28-CT03:** O sistema deve permitir alterar os dados cadastrais e o status de um colaborador já existente.
- **🧪 C28-CT04:** O sistema deve permitir gerenciar, vincular ou adicionar novas funções (ex.: "Treinador da academia", "Personal") a um colaborador.
- **🧪 C28-CT05:** O sistema deve exibir uma tela de perfil detalhado com todas as informações e métricas consolidadas ao selecionar um colaborador.
- **🧪 C28-CT06:** O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar um colaborador com campos obrigatórios vazios.
- **🧪 C28-CT07:** O sistema deve permitir a remoção definitiva de um colaborador cadastrado mediante confirmação em modal.

📎 **Fonte:** `CT_RF28_Gest o de Fun es.md` *(Mapeamento do CT_RF28)*

---

### 🧩 RF29 — Gestão de Funções

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C29-CT01:** O sistema deve filtrar e retornar corretamente a listagem de funções com base nos critérios de nome, código e tipo (interno ou externo).
- **🧪 C29-CT02:** O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar uma nova função deixando campos obrigatórios em branco.
- **🧪 C29-CT03:** O sistema deve permitir o cadastro de uma nova função preenchendo corretamente os campos de nome, tipo de funcionário e parâmetros relacionados.
- **🧪 C29-CT04:** O sistema deve permitir visualizar e alterar as permissões de acesso liberadas para uma determinada função.
- **🧪 C29-CT05:** O sistema deve exibir o modal com os dados detalhados de uma função ao acionar a opção de visualização.

📎 **Fonte:** `CT_RF29_Gerenciamento de Fornecedores no SIFIT.md` *(Mapeamento do CT_RF29)*

---

### 🧩 RF30 — Gerenciamento de Fornecedores

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C30-CT01:** O sistema deve permitir a busca e filtragem de fornecedores cadastrados utilizando os campos de código ou nome.
- **🧪 C30-CT02:** O sistema deve permitir o cadastro de um novo fornecedor preenchendo corretamente os campos obrigatórios e complementares no modal "Novo Fornecedor".
- **🧪 C30-CT03:** O sistema deve impedir o cadastro e emitir mensagens de alerta caso o usuário tente salvar um fornecedor sem preencher os campos obrigatórios.
- **🧪 C30-CT04:** O sistema deve exibir todas as informações consolidadas de um fornecedor ao acionar a opção de visualização de cadastro.
- **🧪 C30-CT05:** O sistema deve exigir confirmação em modal ao solicitar a exclusão de um fornecedor e processar a requisição de remoção.

📎 **Fonte:** `CT_RF30_Gerenciamento de Tipos de Documentos no SIFIT.md` *(Mapeamento do CT_RF30)*

---

### 🧩 RF31 — Gerenciamento de Tipos de Documentos

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C31-CT01:** O sistema deve permitir a filtragem de tipos de documentos cadastrados utilizando os campos de código, nome ou o filtro de aplicação.
- **🧪 C31-CT02:** O sistema deve permitir a criação bem-sucedida de um novo tipo de documento definindo seu nome e a respectiva aplicação.
- **🧪 C31-CT03:** O sistema deve impedir o salvamento e emitir um aviso caso o usuário tente cadastrar um tipo de documento com o campo de nome vazio.
- **🧪 C31-CT04:** O sistema deve permitir alterar os dados cadastrais (como a aplicação) de um tipo de documento já existente.
- **🧪 C31-CT05:** O sistema deve solicitar confirmação via modal ao tentar excluir um tipo de documento e processar a solicitação de remoção.

📎 **Fonte:** `CT_RF31_Gerenciamento de Atividades no SIFIT.md` *(Mapeamento do CT_RF31)*

---

### 🧩 RF32 — Gerenciamento de Atividades

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C32-CT01:** O sistema deve permitir a filtragem das atividades cadastradas por nome ou por código.
- **🧪 C32-CT02:** O sistema deve permitir o cadastro de uma nova atividade por meio do modal "Atividade".
- **🧪 C32-CT03:** O sistema deve impedir o cadastro de uma atividade quando os campos do modal "Atividade" estiverem em branco.
- **🧪 C32-CT04:** O sistema deve permitir a visualização e a atualização das informações de uma atividade existente.
- **🧪 C32-CT05:** O sistema deve permitir a exclusão de uma atividade mediante confirmação do usuário.

📎 **Fonte:** `CT_RF32_Gerenciamento de Pontua es no SIFIT.md` *(Mapeamento do CT_RF32)*

---

### 🧩 RF33 — Gerenciamento de Pontuações

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C33-CT01:** O sistema deve permitir filtrar as pontuações cadastradas por código, nome da pontuação e status (Ativo/Inativo).
- **🧪 C33-CT02:** O sistema deve permitir a criação de uma nova pontuação (campanha) com período, tipo, status e produtos de resgate.
- **🧪 C33-CT03:** O sistema deve apresentar uma mensagem de erro ao falhar ao salvar as alterações de uma pontuação existente, sem quebrar a interface.
- **🧪 C33-CT04:** O sistema deve permitir vincular atividades a uma pontuação por meio do modal "Atividades da Pontuação".
- **🧪 C33-CT05:** O sistema deve permitir visualizar o ranking de participantes associados a uma pontuação.
- **🧪 C33-CT06:** O sistema deve apresentar mensagem de erro ao falhar o processamento de uma ação da coluna "Ações", sem quebrar a interface.
- **🧪 C33-CT07:** O sistema deve permitir excluir uma pontuação existente após confirmação do usuário.
- **🧪 C33-CT08:** O sistema deve impedir o cadastro de uma pontuação sem nome e exibir um aviso solicitando o preenchimento do campo.

📎 **Fonte:** `CT_RF33_Gerenciamento de Produtos no SIFIT.md` *(Mapeamento do CT_RF33)*

---

### 🧩 RF34 — Gerenciamento de Produtos

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C34-CT01:** O sistema deve permitir filtrar a listagem de produtos por Código, Nome, Status (Ativo/Inativo) e Tipo (Venda/Pontuação).
- **🧪 C34-CT02:** O sistema deve permitir cadastrar um novo produto informando Nome, Descrição, Tipo, Pontuação e Imagem.
- **🧪 C34-CT03:** O sistema deve permitir a alteração das informações de um produto previamente cadastrado.
- **🧪 C34-CT04:** O sistema deve solicitar confirmação do usuário antes de realizar a exclusão de um produto.

📎 **Fonte:** `CT_RF34_Filtrar Enquetes por C digo, Nome e Status.md` *(Mapeamento do CT_RF34)*

---

### 🧩 RF35 — Gestão e Filtragem de Enquetes

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C35-CT01:** O sistema deve permitir a filtragem de enquetes cadastradas por Código, Nome da enquete e Status.
- **🧪 C35-CT02:** O sistema deve permitir a criação e publicação de novas enquetes direcionadas aos alunos.
- **🧪 C35-CT03:** O sistema deve permitir visualizar o resultado e a apuração das respostas dos alunos às enquetes.

📎 **Fonte:** `CT_RF35_Gest o e consulta de leads no m dulo Prospec o.md` *(Mapeamento do CT_RF35)*

---

### 🧩 RF36 — Gestão e Consulta de Leads no Módulo Prospecção

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C36-CT01:** O sistema deve permitir buscar e filtrar leads por Nome, Telefone, Status da Negociação e Origem.
- **🧪 C36-CT02:** O sistema deve permitir o cadastro de novos prospectos/leads indicando dados de contato e interesse.
- **🧪 C36-CT03:** O sistema deve permitir a atualização do funil de vendas e alteração de status de acompanhamento do lead.

📎 **Fonte:** `CT_RF36_Gest o e consulta de planos no sistema SIFIT.md` *(Mapeamento do CT_RF36)*

---

### 🧩 RF37 — Gestão e Consulta de Planos

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C37-CT01:** O sistema deve permitir a consulta e filtragem de planos de assinatura por Nome, Valor, Periodicidade e Status.
- **🧪 C37-CT02:** O sistema deve permitir o cadastramento de novos planos definindo modalidades inclusas, regras de renovação e valores.
- **🧪 C37-CT03:** O sistema deve permitir a edição de parâmetros e inativação de planos cadastrados.

📎 **Fonte:** `CT_RF37_Gest o de Modelos de Contrato no sistema SIFIT.md` *(Mapeamento do CT_RF37)*

---

### 🧩 RF38 — Gestão de Modelos de Contrato

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C38-CT01:** O sistema deve permitir consultar e filtrar modelos de contrato cadastrados na plataforma.
- **🧪 C38-CT02:** O sistema deve permitir a criação de modelos de contrato com cláusulas personalizadas e variáveis dinâmicas.
- **🧪 C38-CT03:** O sistema deve permitir editar e atualizar a minuta de modelos de contrato existentes.

📎 **Fonte:** `CT_RF38_Gest o de Tipos de Pagamento no sistema SIFIT.md` *(Mapeamento do CT_RF38)*

---

### 🧩 RF39 — Gestão de Tipos de Pagamento

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C39-CT01:** O sistema deve permitir visualizar e filtrar os tipos de pagamento aceitos pelo estabelecimento (ex.: Dinheiro, PIX, Cartão).
- **🧪 C39-CT02:** O sistema deve permitir o cadastro e habilitação de novos métodos ou condições de pagamento.

📎 **Fonte:** `CT_RF39_ Abrir modal de cadastro de bandeira de cart o.md` *(Mapeamento do CT_RF39)*

---

### 🧩 RF40 — Gestão de Bandeiras de Cartão

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C40-CT01:** O sistema deve disponibilizar um modal para cadastro e vinculação de novas bandeiras de cartão aceitas nas maquininhas/gateway.
- **🧪 C40-CT02:** O sistema deve validar os dados preenchidos ao cadastrar uma nova bandeira exigindo nome e taxa associada.

📎 **Fonte:** `CT_RF40_ Aplica o de Fichas de Anamnese no sistema SIFIT.md` *(Mapeamento do CT_RF40)*

---

### 🧩 RF41 — Aplicação de Fichas de Anamnese

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C41-CT01:** O sistema deve permitir selecionar um aluno e aplicar um questionário de anamnese com base em modelos pré-definidos.
- **🧪 C41-CT02:** O sistema deve registrar os dados informados, calculando alertas ou restrições de saúde indicadas na anamnese.

📎 **Fonte:** `CT_RF41_ Gerenciamento de Modelos de Anamnese no sistema SIFIT.md` *(Mapeamento do CT_RF41)*

---

### 🧩 RF42 — Gerenciamento de Modelos de Anamnese

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C42-CT01:** O sistema deve permitir listar, filtrar e consultar modelos de fichas de anamnese cadastrados.
- **🧪 C42-CT02:** O sistema deve permitir a criação de novos modelos estruturados de anamnese agregando perguntas e categorias.

📎 **Fonte:** `CT_RF42_Gerenciamento de Categorias de Anamnese no sistema SIFIT.md` *(Mapeamento do CT_RF42)*

---

### 🧩 RF43 — Gerenciamento de Categorias de Anamnese

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C43-CT01:** O sistema deve permitir a criação e manutenção de categorias para organização de perguntas de anamnese (ex.: Cardíaco, Muscular, Histórico Familiar).
- **🧪 C43-CT02:** O sistema deve permitir filtrar e ordenar categorias de anamnese cadastradas.

📎 **Fonte:** `CT_RF43_Gest o de Pergunta de Anamnese.md` *(Mapeamento do CT_RF43)*

---

### 🧩 RF44 — Gestão de Perguntas de Anamnese

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C44-CT01:** O sistema deve permitir o cadastro de perguntas individuais para anamnese definindo o tipo de resposta (texto, múltipla escolha, sim/não).
- **🧪 C44-CT02:** O sistema deve permitir associar perguntas a categorias específicas de anamnese.

📎 **Fonte:** `CT_RF44_ Gest es de intelig ncia.md` *(Mapeamento do CT_RF44)*

---

### 🧩 RF45 — Gestões de Inteligência e Automação

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C45-CT01:** O sistema deve disponibilizar um painel de inteligência operacional identificando padrões de frequência e risco de cancelamento dos alunos.
- **🧪 C45-CT02:** O sistema deve permitir a configuração e disparo de automações de retenção baseadas no comportamento do cliente.

📎 **Fonte:** `CT_RF45_ Visualiza o e Filtragem do Dashboard de Resultados da Intelig ncia.md` *(Mapeamento do CT_RF45)*

---

### 🧩 RF46 — Visualização e Filtragem do Dashboard da Inteligência

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C46-CT01:** O sistema deve permitir a filtragem por período e segmento dos dados consolidados no Dashboard de Inteligência.
- **🧪 C46-CT02:** O sistema deve permitir exportar ou detalhar os indicadores de risco de evasão e projeções.

📎 **Fonte:** `CT_RF46_ Gest es de configura es.md` *(Mapeamento do CT_RF46)*

---

### 🧩 RF47 — Gestão de Configurações Gerais

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C47-CT01:** O sistema deve permitir a atualização das configurações gerais da unidade, como dados institucionais, regras de funcionamento e integrações.
- **🧪 C47-CT02:** O sistema deve validar a persistência das configurações alteradas após a confirmação.

📎 **Fonte:** `CT_RF47_Gerenciamento de Modelos de Ficha.md` *(Mapeamento do CT_RF47)*

---

### 🧩 RF48 — Gerenciamento de Modelos de Ficha de Treino

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C48-CT01:** O sistema deve permitir criar e organizar modelos padrão de fichas de treino (ex.: Treino A/B/C, Iniciante, Hipertrofia).
- **🧪 C48-CT02:** O sistema deve permitir a edição de exercícios e séries vinculados a um modelo de ficha pré-cadastrado.

📎 **Fonte:** `CT_RF48_ Gerenciamento de Notifica es e Conte dos do Aplicativo.md` *(Mapeamento do CT_RF48)*

---

### 🧩 RF49 — Gerenciamento de Notificações, Conteúdos e Tema

🔎 **Comportamentos cobertos pelos casos de teste:**

- **🧪 C49-CT01:** O sistema deve permitir o cadastro e envio de notificações *push* e avisos para os aplicativos dos alunos.
- **🧪 C49-CT02:** O sistema deve permitir a alternância de temas da interface (modo claro/escuro) com atualização imediata do layout visual.

📎 **Fonte:** `CT_RF49_Altern ncia de Tema da Interface.md`

---

## 🛡️ 5. Requisitos Não Funcionais (Propostas de Qualidade)

- **RNF01 — Usabilidade:** A interface deve manter responsividade e acessibilidade em resoluções desktop e mobile, preservando o contraste e a leitura nos modos claro e escuro.
- **RNF02 — Desempenho:** As consultas com filtros complexos (ex.: relatórios e dashboards) devem responder em um tempo médio inferior a 2 segundos.
- **RNF03 — Segurança e Privacidade:** Dados sensíveis (biometria, documentos e registros de saúde da anamnese) devem trafegar criptografados via protocolo HTTPS.
- **RNF04 — Confiabilidade:** O sistema deve tratar falhas de comunicação com gateways de pagamento (ex.: Pagar.me) informando mensagens amigáveis ao usuário sem corromper transações.
