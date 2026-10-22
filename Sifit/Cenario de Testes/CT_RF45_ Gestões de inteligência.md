## Cenário 45: Módulo Inteligência & Automação e Gestão de Clientes

### Caso de Teste 01: Acesso e Visualização da Central de Automações

| ID | Descrição |
| --- | --- |
| **C45-CT01** | Validar o direcionamento para a tela "Inteligência & Automação" e a renderização dos cards de métricas principais, automações ativas e histórico de atividades recentes. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SIFIT. |

| **Passos** |
| --- |
| **DADO** que o usuário navega pelo menu principal e seleciona a opção "Inteligência & Automação".<br> |
| **QUANDO** a página for carregada.<br> |
| **ENTÃO** o sistema deve exibir a "Central de Automações" com os indicadores superiores, os painéis de "Automações ativas" (*Risco de Evasão* e *Aniversariantes*) e a barra de "Atividade recente". |

| **Critérios de Aceitação** |
| --- |
| A tela deve carregar sem falhas de layout, apresentando as métricas consolidadas e os controles de acionamento das automações. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ROln9z52cwGh8n1Qy_PVnQzSZL8B3s7Z/view?usp=sharing |

---

### Caso de Teste 02: Filtragem por Nível de Risco no Relatório de Evasão

| ID | Descrição |
| --- | --- |
| **C45-CT02** | Validar a aplicação de filtros por categoria de risco (*Alto risco*, *Médio*, *Baixo risco*) no painel do Relatório de Risco de Evasão. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Inteligência & Automação" com o painel "Relatório de Risco de Evasão" expandido. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza o "Relatório de Risco de Evasão" expandido.<br>|
| **QUANDO** alternar entre os filtros de nível de risco (ex.: selecionar "Médio" e depois "Baixo risco").<br>|
| **ENTÃO** a tabela deve atualizar em tempo real, listando apenas os alunos enquadrados no nível de risco selecionado ou exibindo a indicação "Nenhum aluno neste nível". |

| **Critérios de Aceitação** |
| --- |
| Os filtros de categoria de risco devem restruturar os registros da tabela de acordo com o parâmetro selecionado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1idkgipBOyzUUpeztEEord6VmjKoZ_Mly/view?usp=sharing |

---

### Caso de Teste 03: Tentativa de Execução Manual da Automação de Aniversariantes

| ID | Descrição |
| --- | --- |
| **C45-CT03** | Validar a mensagem de aviso ao tentar acionar manualmente a automação de Aniversariantes. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o card da automação "Aniversariantes".<br> |
| **QUANDO** clicar no botão "Executar agora".<br> |
| **ENTÃO** o sistema deve exibir um modal de alerta informando a indisponibilidade de execução manual para este tipo de rotina. |

| **Critérios de Aceitação** |
| --- |
| O sistema deve bloquear a execução direta e exibir o aviso informativo correspondente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1m5z3xBQjvrpwxnd8JzFDKnMZK-bHQPph/view?usp=sharing |

---

### Caso de Teste 04: Configuração da Automação de Risco de Evasão e Validação de Destinatários

| ID | Descrição |
| --- | --- |
| **C45-CT04** | Validar a alteração dos parâmetros de frequência, critérios de análise e sensibilidade na automação de Risco de Evasão, observando o retorno de validação de destinatários obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário clica em "Configurar" no card da automação "Risco de Evasão".<br> |
| **QUANDO** alterar a frequência (ex.: *Semanal*), definir o dia e horário, marcar critérios e alterar o nível de Sensibilidade (ex.: *Alta*).<br> |
| **E** clicar em "Salvar configuração".<br>|
| **ENTÃO** o sistema deve validar os destinatários selecionados e exibir mensagem de erro caso existam regras incompletas ou pendentes de definição. |

| **Critérios de Aceitação** |
| --- |
| O formulário de configuração deve permitir a personalização dos parâmetros e aplicar as regras de validação ao tentar salvar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18t1j896JZY1sLMCKO9wrI-jAcnLY6lpx/view?usp=sharing |

---

### Caso de Teste 05: Configuração e Ajuste de Frequência na Automação de Aniversariantes

| ID | Descrição |
| --- | --- |
| **C45-CT05** | Validar a navegação e ajuste de parâmetros de frequência personalizada na janela de configuração da automação de Aniversariantes. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Configurar" da automação "Aniversariantes".<br> |
| **QUANDO** alternar os tipos de frequência (ex.: *Personalizado*), definir o intervalo em dias e ajustar a sensibilidade do relatório.<br> |
| **E** acionar o botão "Salvar configuração".<br> |
| **ENTÃO** o sistema deve processar os dados informados e retornar a resposta do servidor referente ao salvamento. |

| **Critérios de Aceitação** |
| --- |
| As opções do modal de configuração de aniversariantes devem responder adequadamente aos comandos de edição do usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/10o5FnQgCB9GXpWGXt5QO9KYy6fMwnsv7/view?usp=sharing |

---

### Caso de Teste 06: Consulta de Detalhes do Aluno no Painel Lateral do Relatório de Evasão

| ID | Descrição |
| --- | --- |
| **C45-CT06** | Validar a expansão do painel lateral de detalhes ao selecionar um aluno listado no Relatório de Risco de Evasão. |

| **Pré-condições** |
| --- |
| O usuário estar com o "Relatório de Risco de Evasão" aberto contendo alunos listados. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a lista do Relatório de Risco de Evasão.<br>|
| **QUANDO** clicar sobre a linha de um aluno (ex.: *Jerome Lionel*).<br>|
| **ENTÃO** o sistema deve abrir o painel lateral exibindo o Score de Risco, Motivos, Informações Complementares (*Último Check-in*, *Dias sem treinar*, *Status Financeiro*) e a caixa de Recomendações com ações rápidas. |

| **Critérios de Aceitação** |
| --- |
| As informações detalhadas e o histórico do aluno devem ser apresentados com precisão na gaveta lateral de consulta. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11tJSuASkUfxH93tSD63bOuW_ZlCOLZS3/view?usp=sharing |

---

### Caso de Teste 07: Navegação pelas Ações Rápidas do Cliente no Perfil de Atendimento

| ID | Descrição |
| --- | --- |
| **C45-CT07** | Validar o acionamento das ações rápidas (*Registrar pagamento*, *Agendar avaliação*, *Enviar mensagem*) diretamente da tela do cliente. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Visualizar Cliente". |

| **Passos** |
| --- |
| **DADO** que o usuário estar na tela "Visualizar Cliente".<br>|
| **QUANDO** interagir com os botões do painel "Ações rápidas" (ex.: clicar em *Registrar pagamento*, *Agendar avaliação* ou *Enviar mensagem*).<br>|
| **ENTÃO** o sistema deve abrir o respectivo modal operacional correspondente à ação selecionada. |

| **Critérios de Aceitação** |
| --- |
| Cada botão do bloco de Ações Rápidas deve abrir o modal correto sem gerar inconsistências na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1k649IbcINO0HMubvNySOVseUji9-I1le/view?usp=sharing |

---

### Caso de Teste 08: Interação com Cards de Automações Disponíveis na Central

| ID | Descrição |
| --- | --- |
| **C45-CT08** | Validar a expansão e interação com os cards da seção "Automações disponíveis" (*Avaliações vencendo*, *Frequência em queda*, *Financeiro diário*, *Cobranças automáticas*). |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário navega até a seção "Automações disponíveis".<br>|
| **QUANDO** clicar nos botões de ação dos cards (ex.: *Verificar agora*, *Ver lista*, *Ver resumo*, *Configurar e ver prévia*).<br> |
| **ENTÃO** o sistema deve expandir os painéis correspondentes na parte inferior da tela com os dados sumarizados da automação. |

| **Critérios de Aceitação** |
| --- |
| As automações disponíveis devem expandir seus painéis explicativos e tabelas auxiliares ao serem acionadas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1D4sJkcLr9TF51DAP6254JmAVuUMBrTgn/view?usp=sharing |

---

### Caso de Teste 09: Registro de Pagamento de Mensalidade Pendente no Perfil do Cliente

| ID | Descrição |
| --- | --- |
| **C45-CT09** | Validar o preenchimento e finalização do registro de pagamento de uma mensalidade pendente através das Ações Rápidas no perfil do cliente. |

| **Pré-condições** |
| --- |
| O usuário estar na tela "Visualizar Cliente" de um aluno que possui mensalidades pendentes em aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Visualizar Cliente" e clica em **"Registrar pagamento"** no painel lateral de Ações Rápidas.<br> |
| **QUANDO** o modal "Registrar pagamento" carregar os dados da conta em aberto (ex.: *Conta #1504*, valor *R$ 200,00*).<br> |
| **E** preencher o valor recebido, a data do pagamento, selecionar o **Tipo de pagamento** (ex.: *Dinheiro*) e o **Local de recebimento** (ex.: *Caixa Muay Thai*). <br> |
| **E** inserir observações opcionais e clicar no botão **"Salvar pagamento"**. <br> |
| **ENTÃO** o sistema deve processar a transação e atualizar o status financeiro do aluno no perfil. |

| **Critérios de Aceitação** |
| --- |
| O modal de pagamento deve carregar os títulos em aberto, permitir o preenchimento dos campos obrigatórios de baixa e registrar a quitação com sucesso.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1fPRDkApKS27qKP7vJJHzLtyEwmmzmy27/view?usp=sharing |
