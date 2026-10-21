
---
## Cenário 5: Página Inicial (Parte 4)
---
### Caso de Teste 01: Agendamento de Avaliação através de Ações Rápidas no Perfil do Cliente

| ID  | Descrição |
| --- | --- |
| **C05-CT01** | Validar a abertura do modal "Cadastrar Avaliação" a partir do painel de Ações Rápidas, a busca/substituição do aluno, seleção do personal responsável, data e horário, finalizando com o salvamento da avaliação. |

| **Pré-condições** |
| --- |
| Utilizador na tela "Visualizar Cliente" acessada a partir da Página Inicial. |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela "Visualizar Cliente". |
| **E** localiza o painel lateral de "Ações rápidas". |
| **QUANDO** clicar no botão "Agendar avaliação". |
| **E** o modal "Cadastrar Avaliação" for exibido. |
| **E** clicar no ícone de lupa do campo Aluno para abrir o modal "Buscar Aluno", pesquisando por "gabriel" e selecionando o aluno *Lurdes Gabriely*<br> |
| **E** selecionar o personal responsável (*Santiago*), definir a data no calendário (*07/11/2026*) e o horário (*07:30*). |
| **E** clicar no botão "Salvar". |
| **ENTÃO** o sistema deve processar o salvamento exibindo o status "Salvando...", fechar o modal e registrar a nova avaliação com sucesso. |

| **Critérios de aceitação** |
| --- |
| O modal de cadastro deve permitir a busca e seleção de alunos, escolha de personal, definição de data e hora, salvando o agendamento sem erros. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1bOxxxvyWiSd2v98E9CV09kWWGaZcb-uP/view?usp=sharing |
---

### Caso de Teste 02: Envio de Mensagens Rápidas pelo Painel da Inteligência do Cliente

| ID | Descrição |
| --- | --- |
| **C05-CT02** | Validar o envio e troca de templates de mensagem (Falta, Cobrança, Retorno de treino, Aniversário, Avaliação) através das Ações Rápidas do painel "Inteligência Sifit" do cliente. |

| **Pré-condições** |
| --- |
| Utilizador na tela de visualização do cliente com a barra lateral de Inteligência e Ações Rápidas visíveis. |

| **Passos** |
| --- |
| **DADO** que o utilizador acessou os detalhes do cliente no Dashboard/Inteligência Sifit. |
| **QUANDO** clicar no botão "Enviar mensagem". |
| **E** alternar entre as abas de categorias de mensagens (*Falta*, *Cobrança*, *Retorno de treino*, *Aniversário*, *Avaliação*). |
| **ENTÃO** o texto do modelo de mensagem deve atualizar instantaneamente na área de texto conforme a categoria selecionada e disponibilizar os botões "Copiar mensagem" e "Enviar via WhatsApp". |

| **Critérios de aceitação** |
| --- |
| Os modelos pré-configurados de mensagem devem alternar dinamicamente no modal, permitindo a cópia do texto ou o disparo direto via WhatsApp. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1jRyEDLqmFZgFtRKV4gwQtnQP1R16ypIz/view?usp=sharing |

---

### Caso de Teste 03: Edição do Cadastro do Cliente e Alteração de Dados Pessoais / Foto

| ID | Descrição |
| --- | --- |
| **C05-CT03** | Validar a edição completa dos dados de um cliente (RG, foto de perfil, telefones, endereço, biometria e dados adicionais) salvando as alterações. |

| **Pré-condições** |
| --- |
| Utilizador na tela de perfil do cliente acessada via Dashboard. |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela "Visualizar Cliente". |
| **E** clica no botão "Alterar dados". |
| **QUANDO** a tela "Editar Cliente" for carregada. |
| **E** preencher/atualizar os campos de Documentos (RG), Upload de Foto do Cliente, Contato, Endereço, Biometria, Usuário do Aplicativo e Dados do Responsável/Outros Dados. |
| **E** clicar no botão "Salvar Alterações". |
| **ENTÃO** o sistema deve processar o salvamento e retornar o utilizador à listagem/perfil com as informações atualizadas com sucesso. |

| **Critérios de aceitação** |
| --- |
| Todos os campos do formulário de edição do cliente devem aceitar atualização de dados e salvar as modificações sem erros. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18LcPRchqIx72t9JlhbzcHGCt9nOnAEwR/view?usp=sharing |

---

### Caso de Teste 04: Visualização do Cliente a partir da Lista de "Clientes Sem Matrículas"

| ID | Descrição |
| --- | --- |
| **C05-CT04** | Verificar o direcionamento do modal "Clientes Sem Matrículas" (acessado pelos cards do Dashboard) para a tela de visualização do perfil do cliente. |

| **Pré-condições** |
| --- |
| Utilizador no Dashboard principal com o modal "Clientes Sem Matrículas" aberto. |

| **Passos** |
| --- |
| **DADO** que o utilizador está visualizando o modal "Clientes Sem Matrículas". |
| **QUANDO** clicar no botão de ação ("Visualizar cliente" / ícone de olho) na linha do aluno (ex.: *Gabrielli Bononi*). |
| **ENTÃO** o modal deve ser fechado e o sistema deve redirecionar o utilizador diretamente para a tela "Visualizar Cliente" correspondente ao aluno selecionado. |

| **Critérios de aceitação** |
| --- |
| O clique na ação do aluno no modal de Sem Matrículas deve efetuar o redirecionamento correto para o perfil completo do cliente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1SLv5Ko26qSyEh3UmKmzY3BckRuk0L-G0/view?usp=sharing |

---

### Caso de Teste 05: Navegação pelas Ações Recomendadas para a Tela de Avaliações Pendentes

| ID | Descrição |
| --- | --- |
| **C02-CT05** | Garantir o correto direcionamento da ação rápida "Ver avaliações" no card de Ações Recomendadas para a tela de gestão de Avaliações. |

| **Pré-condições** |
| --- |
| Utilizador na Página Inicial posicionado no bloco "Ações recomendadas para hoje". |

| **Passos** |
| --- |
| **DADO** que o utilizador está na Página Inicial do SIFIT. |
| **E** visualiza o card "Avaliações pendentes agendadas para hoje". |
| **QUANDO** clicar no botão "Ver avaliações". |
| **ENTÃO** o sistema deve redirecionar o utilizador para a tela de **Avaliações** (`/avaliacoes`). |
| **E** listar todas as avaliações cadastradas com seus respectivos status (ex.: *PENDENTE*), datas, horários e personais responsáveis. |

| **Critérios de aceitação** |
| --- |
| O atalho "Ver avaliações" deve direcionar o utilizador para a página operacional de Avaliações do sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1yymsYl3R4H5fQGtBD38FZLjatE7A-PDk/view?usp=sharing |
