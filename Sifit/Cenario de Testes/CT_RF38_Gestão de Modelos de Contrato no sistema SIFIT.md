
---

# Cenário 38: Gestão de Modelos de Contrato no sistema SIFIT

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo de **Configurações > Modelos de Contrato** do sistema **SiFit**. O objetivo é validar o acesso à tela de cadastro, a inserção de variáveis dinâmicas (como dados do aluno, do plano, da academia e do contrato) no editor de texto, a atualização da pré-visualização (preview) do contrato, a alteração de status e o salvamento de novos modelos na plataforma.

---

## 2. Cenários de Teste

### Caso de Teste 01: Acesso ao Formulário de Criação de Modelo de Contrato

| ID | Descrição |
| --- | --- |
| **C38-CT01** | O sistema deve redirecionar o usuário para a tela de adição ao clicar no botão de novo modelo de contrato. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema e na página de **Modelos Contrato**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Modelos Contrato" |
| **QUANDO** clica no botão **Adicionar Modelo Contrato**<br> |
| **ENTÃO** o sistema deve carregar o formulário com os campos de título, status, editor de texto, painel de variáveis e seção de pré-visualização. |

| **Critérios de Aceitação** |
| --- |
| * A tela deve exibir todos os componentes necessários para a estruturação do modelo de contrato. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1T8Su4PXZIUOFRYDhW1_8acvl-zpqHe8Z/view?usp=sharing |

---

### Caso de Teste 02: Atualização e Validação da Pré-visualização do Contrato

| ID | Descrição |
| --- | --- |
| **C38-CT02** | O sistema deve gerar e atualizar a pré-visualização do contrato formatado de acordo com o texto digitado no editor. |

| **Pré-condições** |
| --- |
| O usuário deve estar preenchendo o campo "Texto do contrato".|

| **Passos** |
| --- |
| **DADO** que o usuário inseriu ou alterou a minuta contratual no editor de texto |
| **QUANDO** clica no botão **Atualizar preview** na seção de pré-visualização |
| **ENTÃO** o quadro inferior deve carregar o documento formatado com as cláusulas e formatações aplicadas. |

| **Critérios de Aceitação** |
| --- |
| * O preview deve refletir com exatidão a estrutura inserida no editor. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1mK1LHuqrF-s37bemLrq491z6i_Sjx1eW/view?usp=sharing |

---

### Caso de Teste 03: Inserção de Variáveis de Aluno no Contrato

| ID | Descrição |
| --- | --- |
| **C38-CT03** | O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados do aluno no corpo do texto do contrato. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de cadastro de **Modelos de Contrato**. |

| **Passos** |
| --- |
| **DADO** que o usuário está posicionado no editor "Texto do contrato" |
| **QUANDO** seleciona uma variável no painel lateral em "Dados do aluno" (ex: `{nome_aluno}` ou `{cpf_aluno}`) |
| **ENTÃO** a tag correspondente deve ser inserida exatamente no ponto onde se encontra o cursor. |

| **Critérios de Aceitação** |
| --- |
| * As variáveis do aluno devem ser adicionadas corretamente para a futura substituição automatizada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1swPgbfqXEscutWsMQ0jfb7ZMKhIVyAMK/view?usp=sharing |

---

### Caso de Teste 04: Inserção de Variáveis de Plano no Contrato

| ID | Descrição |
| --- | --- |
| **C38-CT04** | O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados do plano contratado no corpo do texto do contrato. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de cadastro de **Modelos de Contrato**. |

| **Passos** |
| --- |
| **DADO** que o usuário está posicionado no editor de texto |
| **QUANDO** seleciona uma variável no painel lateral em "Dados do plano" (ex: `{nome_plano}` ou `{valor_plano}`) |
| **ENTÃO** a tag de plano correspondente deve ser inserida no ponto onde está o cursor. |

| **Critérios de Aceitação** |
| --- |
| * As tags informativas do plano devem ser inseridas de forma correta no editor. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1xsGtiMSBAESn-da13sfPzkuYsPLjrVcX/view?usp=sharing |

---

### Caso de Teste 05: Inserção de Variáveis da Academia no Contrato

| ID | Descrição |
| --- | --- |
| **C38-CT05** | O sistema deve permitir a inclusão de tags dinâmicas referentes aos dados da academia no corpo do texto do contrato. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de cadastro de **Modelos de Contrato**. |

| **Passos** |
| --- |
| **DADO** que o usuário está posicionado no editor de texto |
| **QUANDO** seleciona uma variável no painel lateral em "Dados da academia" (ex: `{nome_academia}` ou `{cnpj_academia}`) |
| **ENTÃO** a tag correspondente deve ser integrada ao texto no local do cursor. |

| **Critérios de Aceitação** |
| --- |
| * As tags da academia devem ser adicionadas de forma íntegra no documento. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/15Yb3mw80T7yzpr_3ypQEAioW1c_tI241/view?usp=sharing |

---

### Caso de Teste 06: Inserção de Variáveis de Contrato no Documento

| ID | Descrição |
| --- | --- |
| **C38-CT06** | O sistema deve permitir a inclusão de tags dinâmicas referentes às informações contratuais específicas no texto do modelo. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de cadastro de **Modelos de Contrato**. |

| **Passos** |
| --- |
| **DADO** que o usuário foca no editor de texto do contrato |
| **QUANDO** clica em uma das variáveis do grupo "Dados do contrato" |
| **ENTÃO** a tag dinâmica correspondente deve ser inserida na posição do cursor. |

| **Critérios de Aceitação** |
| --- |
| * As variáveis relativas ao contrato devem ser injetadas corretamente no editor. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1zNV6DtqVGQMLwmpVZXq3kEXEackE0sh3/view?usp=sharing |

---

### Caso de Teste 07: Visualização e Fechamento do Painel de Todas as Variáveis

| ID | Descrição |
| --- | --- |
| **C38-CT07** | O sistema deve permitir a expansão e o recolhimento do painel completo de variáveis disponíveis para consulta. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de modelos de contrato. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza o painel lateral de variáveis |
| **QUANDO** interage com o botão "Ver todas as variáveis" para expandir e recolher a listagem completa |
| **ENTÃO** o painel deve alternar a exibição dos grupos de variáveis dinâmicas de forma responsiva. |

| **Critérios de Aceitação** |
| --- |
| * A interface deve apresentar e ocultar o painel completo de variáveis de acordo com a ação do usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1VYqXn2Gvn6XOrhzlMQVCdLzgTDKtu3_B/view?usp=sharing |

---

### Caso de Teste 08: Salvamento de Novo Modelo de Contrato com Sucesso

| ID | Descrição |
| --- | --- |
| **C38-CT08** | O sistema deve permitir salvar o modelo de contrato preenchido (com título, status ativo e texto) e retornar à listagem principal. |

| **Pré-condições** |
| --- |
| O usuário deve ter preenchido os campos obrigatórios do modelo de contrato. |

| **Passos** |
| --- |
| **DADO** que o usuário preenche o "Título do modelo", define o status como "Ativo" e redige o conteúdo contratual |
| **QUANDO** clica no botão **Salvar modelo**<br> |
| **ENTÃO** o sistema grava os dados e redireciona o usuário para a tela principal de listagem de **Modelos Contrato**. |

| **Critérios de Aceitação** |
| --- |
| * O contrato cadastrado deve ser armazenado com sucesso, atualizando a listagem geral da aplicação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/12P2uS8dl4YBUixY1DvnlzWbtJkUEMj_d/view?usp=sharing |
