## Cenário 47: Gestão de configurações

### Caso de Teste 01: Configurações Gerais do Sistema (Aba Home)

| ID | Descrição |
| --- | --- |
| **C47-CT01** | Validar a alteração de parâmetros gerais de acesso e presença na aba "Home" e a mensagem de erro ao tentar persistir as configurações. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado no menu **Configurações > Home**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa as configurações na aba "Home".<br> |
| **QUANDO** alterar campos como plano, controle de presença, cobrança de multa ou regras de dias de tolerância.<br> |
| **E** clicar no botão **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve tentar processar a solicitação e exibir o modal com a mensagem de erro *"Erro ao salvar configurações"*. |

| **Critérios de Aceitação** |
| --- |
| Os campos devem aceitar alteração de valores na interface, mas registrar a falha padrão de salvamento do servidor ao submeter. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Ue_F9SKo6he9NbKaP6uEFCGlV0Dm25ND/view?usp=sharing |

---

### Caso de Teste 02: Configuração de Biometria e Integração com Catraca

| ID | Descrição |
| --- | --- |
| **C47-CT02** | Validar a navegação para a aba "Biometria", preenchimento de IP, porta e modelo de aparelho de catraca, e o comportamento ao salvar. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Biometria**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica na aba "Biometria".<br> |
| **QUANDO** configurar os dados de integração com catraca (ex.: marca, modelo *idFace Max*, IP e porta).<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve disparar a rotina de salvamento e retornar o aviso de erro de comunicação/servidor. |

| **Critérios de Aceitação> ** |
| --- |
| A interface deve permitir o preenchimento dos parâmetros de hardware de biometria, exibindo a mensagem de erro padrão ao persistir. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1FTSpetaE1hofI9WHcqO7lcsqxgcHWNcy/view?usp=sharing |

---

### Caso de Teste 03: Configurações de Parâmetros de Avaliação Física

| ID | Descrição |
| --- | --- |
| **C47-CT03** | Validar a alteração de regras de avaliação na aba "Avaliação" (cobrança, tipo de avaliação e dias de validade) e a resposta ao salvar. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Avaliação**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a aba "Avaliação".<br> |
| **QUANDO** alterar os parâmetros de cobrança, tipo de avaliação (ex.: *Bioimpedância* ou *Dobras*) e a duração em dias.<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve tentar persistir as alterações e exibir o pop-up de erro ao salvar. |

| **Critérios de Aceitação** |
| --- |
| Os seletores da aba de avaliação devem atualizar os estados visuais corretamente, culminando na mensagem de erro do sistema ao salvar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/199mT6aQqWizaHXdiT_lDbr3ZqQiqLvn4/view?usp=sharing |

---

### Caso de Teste 04: Configuração de Mensagens Automáticas de Aniversário

| ID | Descrição |
| --- | --- |
| **C47-CT04** | Validar a habilitação e edição de templates de mensagens de aniversário na aba "Aniversário" (WhatsApp, SMS, E-mail) e a tentativa de salvamento. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Aniversário**. |

| **Passos** |
| --- |
| **DADO** que o usuário seleciona a aba "Aniversário".<br> |
| **QUANDO** habilitar o envio automático e editar os textos dos templates de WhatsApp, SMS e E-mail utilizando as variáveis disponíveis.<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve acionar o salvamento e retornar a mensagem de erro padrão. |

| **Critérios de Aceitação** |
| --- |
| O editor de templates e os seletores de canal devem funcionar interativamente, registrando falha no servidor ao salvar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1-DIIr04YSAVkigvUP-oXod3RlCyPaS5G/view?usp=sharing |

---

### Caso de Teste 05: Configuração de Pagamento Online e Integração de Gateway

| ID | Descrição |
| --- | --- |
| **C47-CT05** | Validar a alteração de parâmetros de pagamento online e inserção de token de integração na aba "Pagamento". |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Pagamento**. |

| **Passos** |
| --- |
| **DADO** que o usuário navega até a aba "Pagamento".<br> |
| **QUANDO** habilitar o pagamento online e preencher o token de integração (ex.: *adsatas*).<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve tentar submeter as credenciais financeiras e exibir o aviso de erro ao salvar. |

| **Critérios de Aceitação** |
| --- |
| O campo de token e o status de pagamento online devem aceitar entradas, exibindo o pop-up de erro ao tentar concluir a ação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1cFCj1YBRS4qtsM2I_Wja83Zb1VfPq8Vp/view?usp=sharing |

---

### Caso de Teste 06: Configuração e Conexão de Integrações (WhatsApp Business)

| ID | Descrição |
| --- | --- |
| **C47-CT06** | Validar a gestão de integrações de API na aba "Integrações", preenchendo credenciais de conexão do WhatsApp e testando o salvamento. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Integrações**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a aba "Integrações".<br> |
| **QUANDO** preencher os dados de conexão do provedor de API (ex.: URL do servidor, ID da instância e Token) e marcar a opção de uso nas automações.<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve processar a tentativa de registro, exibindo avisos de erro de conectividade/servidor. |

| **Critérios de Aceitação** |
| --- |
| Os campos de configuração da API de mensagens devem ser editáveis, registrando falha ao submeter os dados de integração. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1NeCFnDQ5YYrpI1d3yEE-cyz7FGKlhkAJ/view?usp=sharing |

---

### Caso de Teste 07: Personalização de Identidade Visual e Design da Academia

| ID | Descrição |
| --- | --- |
| **C47-CT07** | Validar a alteração de cores principais e secundárias, bem como o upload de imagens de logotipo e capa na aba "Design". |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Configurações > Design**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica na aba "Design".<br> |
| **QUANDO** alterar os códigos de cores da paleta, realizar o upload de arquivos de imagem para Logo e Capa.<br> |
| **E** clicar em **"Salvar Configurações"**.<br> |
| **ENTÃO** o sistema deve carregar os arquivos na interface, mas apresentar o erro de salvamento ao concluir. |

| **Critérios de Aceitação** |
| --- |
| A interface de design deve permitir a seleção de cores e envio de arquivos visuais, disparando o erro padrão ao tentar salvar as modificações. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1XW5h-qeF8quwLCDUrDHTUFCgZvMHwzlW/view?usp=sharing |
