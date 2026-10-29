# Relatório de Bugs

**Software:** SIFIT

**QA responsável:** Arthur Miranda Rodrigues (RA 14538)

**Data:** 29.10.26

**Base de análise:** 50 cenários de teste (CT_RF01 a CT_RF50), com o comportamento verificado registrado em cada caso e o vídeo de evidência vinculado

---

## Resumo

Foram registrados **23 bugs** a partir dos casos de teste cujo comportamento obtido divergiu do esperado.

| Severidade | Quantidade |
| :--- | :---: |
| Alta | 10 |
| Média | 10 |
| Baixa | 3 |

| ID | Bug | Módulo | Severidade | Prioridade |
| :--- | --- | --- | :---: | :---: |
| BUG-001 | Link “Esqueci minha senha” não executa nenhuma ação | Login | Média | Média |
| BUG-002 | Botão “Buscar” não filtra as aulas por período (data digitada ou calendário) | SifitBox – Aulas | Alta | Alta |
| BUG-003 | Sistema aceita data final anterior à data inicial sem exibir validação | SifitBox – Aulas | Baixa | Média |
| BUG-004 | Botão “Gerar aulas” não executa nenhum fluxo | SifitBox – Aulas | Alta | Alta |
| BUG-005 | “Finalizar Anamnese” não conclui a ficha | Fichas de Anamnese | Alta | Alta |
| BUG-006 | Grupo muscular é cadastrado sem Nome e sem Tipo Membro | Grupos Musculares | Média | Alta |
| BUG-007 | Atividade é cadastrada com todos os campos em branco | Atividades | Média | Alta |
| BUG-008 | Produto é cadastrado sem nome e sem valor | Produtos | Alta | Alta |
| BUG-009 | Pontuação é cadastrada sem datas (período 0000-00-00) | Pontuação | Média | Média |
| BUG-010 | Conta a pagar é cadastrada sem Título e sem Local de Pagamento | Contas a Pagar | Média | Média |
| BUG-011 | Erro ao salvar a edição de uma pontuação (alteração válida) | Pontuação | Alta | Alta |
| BUG-012 | “Erro no servidor” ao acionar ação da coluna Ações em Pontuação | Pontuação | Média | Média |
| BUG-013 | Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete” | Enquetes | Alta | Alta |
| BUG-014 | Edição de enquete existente retorna “Erro ao salvar enquete” | Enquetes | Alta | Alta |
| BUG-015 | Exclusão de enquete retorna “Erro ao deletar Enquete” | Enquetes | Média | Média |
| BUG-016 | Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha” | Fichas de Treino | Alta | Alta |
| BUG-017 | Cadastro de objetivo de treino retorna “Erro ao salvar objetivo” | Objetivos de Treino | Alta | Alta |
| BUG-018 | Campo Status vazio ao abrir “Editar Turma” | Turmas | Média | Média |
| BUG-019 | Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não | Turmas | Média | Média |
| BUG-020 | Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição | Turmas | Baixa | Baixa |
| BUG-021 | Filtro de status (Pago/Vencido) não é aplicado em Contas a Pagar | Contas a Pagar | Média | Alta |
| BUG-022 | Totais financeiros incorretos na listagem de Contas a Pagar | Contas a Pagar | Alta | Alta |
| BUG-023 | Modal “Visualizar Conta a Pagar” exibe dados sem tratamento | Contas a Pagar | Baixa | Baixa |

---

### 🐞 **Bug 01: Link “Esqueci minha senha” não executa nenhuma ação**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-001 | Ao clicar no link “Esqueci minha senha” na tela de login, nada acontece: o usuário não é levado a nenhuma tela ou modal de recuperação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar a página de login do SIFIT |
| 2. Clicar no link “Esqueci minha senha” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve direcionar o usuário para a tela ou modal de recuperação/redefinição de senha. | Nada acontece; o usuário permanece na tela de login. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Login – recuperação de senha | C01-CT04: Acesso à funcionalidade de recuperação de senha |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1UVEJmPtjgyMDTs_6nrJcX1i0ldW5D671/view?usp=sharing) |

---

### 🐞 **Bug 02: Botão “Buscar” não filtra as aulas por período (data digitada ou calendário)**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-002 | Na tela SifitBox – Aulas, tanto digitando as datas manualmente quanto escolhendo-as no calendário, ao clicar em “Buscar” a grade de resultados não é atualizada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar SifitBox > Aulas (/sifitbox/aulas) |
| 2. Informar data inicial e final, digitando ou usando o calendário |
| 3. Clicar em “Buscar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A listagem de aulas deve ser filtrada pelo período informado. | Nada acontece; a grade de aulas permanece inalterada nos dois fluxos. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| SifitBox – filtro de aulas por período | C10-CT01: Busca por período digitando a data<br>C10-CT02: Busca por período pelo calendário |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1ur0S1lqeUewf-7JjUdG8A7UQDedM6fG-/view?usp=sharing) |
| (https://drive.google.com/file/d/1UIIlC-LJzgxh4_FljfFwLVdNQu6s38rs/view?usp=sharing) |

---

### 🐞 **Bug 03: Sistema aceita data final anterior à data inicial sem exibir validação**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-003 | É possível acionar a busca com data final anterior à inicial; não há mensagem de erro e a tela não reage. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar SifitBox > Aulas |
| 2. Informar uma data final anterior à data inicial |
| 3. Clicar em “Buscar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve impedir o intervalo ilógico e exibir feedback de validação ao usuário. | Nenhuma validação é exibida e a tela permanece inalterada. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| SifitBox – validação de período | C10-CT03: Validação de data inválida (data final anterior à inicial) |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1nk7_GCZVk_qjFUQzqTWe3PwbjEzkIzDi/view?usp=sharing) |

---

### 🐞 **Bug 04: Botão “Gerar aulas” não executa nenhum fluxo**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-004 | Ao clicar em “Gerar aulas”, o botão é acionado visualmente mas nenhum modal é aberto nem processo é disparado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar SifitBox > Aulas |
| 2. Clicar no botão “Gerar aulas” (canto superior direito) |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve executar a geração de aulas ou informar claramente a indisponibilidade da função. | Nada acontece; a grade de aulas continua idêntica e não há feedback. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| SifitBox – geração de aulas | C10-CT04: Acionamento da funcionalidade de gerar aulas |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1eYJda_JSQM0i3tcBcWGAhPR-JWK89ElN/view?usp=sharing) |

---

### 🐞 **Bug 05: “Finalizar Anamnese” não conclui a ficha**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-005 | Ao finalizar a anamnese de um aluno, a ficha não é gerada: em um fluxo nada acontece e a listagem continua com “Nenhuma ficha encontrada”; no outro é exibido o pop-up “Erro no servidor”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Fichas de Anamnese e clicar em “Nova Anamnese” |
| 2. Buscar e selecionar o aluno, escolher um modelo e clicar em “Iniciar” |
| 3. Responder as perguntas e, em “Revisar e Finalizar”, clicar em “Finalizar Anamnese” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A ficha deve ser finalizada e aparecer na listagem de fichas. | A ação não conclui (nenhuma resposta ou pop-up “Erro no servidor”) e a listagem mantém “Nenhuma ficha encontrada”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Aplicação de fichas de anamnese | C41-CT01: Buscar aluno e selecionar modelo de anamnese<br>C41-CT02: Finalização com erro no servidor e salvamento de rascunho |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1V7sDdPIEofzjCAJTtkYiNBRupi0qRDVc/view?usp=sharing) |
| (https://drive.google.com/file/d/1TxdKmCaGbufBF7FS42Sx4AtkSjMvqGQ0/view?usp=sharing) |

---

### 🐞 **Bug 06: Grupo muscular é cadastrado sem Nome e sem Tipo Membro**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-006 | Ao salvar o modal com apenas a imagem, o sistema grava o registro mesmo com os campos obrigatórios vazios. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Grupos Musculares e clicar em “+” |
| 2. Selecionar apenas a imagem, deixando Nome e Tipo Membro vazios |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O cadastro deve ser bloqueado com mensagem indicando Nome e Tipo Membro como obrigatórios. | O grupo muscular é cadastrado sem os dados obrigatórios. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de grupos musculares | C18-CT04: Cadastro sem preencher Nome e Tipo Membro |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/16umD_rrlyjFLRKMBB-g0nF2_dc9_e5V8/view?usp=sharing) |

---

### 🐞 **Bug 07: Atividade é cadastrada com todos os campos em branco**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-007 | Ao salvar o modal “Atividade” vazio, o sistema cria a atividade (código 6) sem nome, pontuação e descrição, sem exibir validação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Atividades e clicar em “Nova Atividade” |
| 2. Não preencher Nome, Pontuação nem Descrição |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O cadastro deve ser bloqueado e a obrigatoriedade dos campos indicada. | Atividade criada em branco; “Total de atividades” passou de 5 para 6 e “Sem pontuação” de 0 para 1. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de atividades | C32-CT03: Cadastrar atividade sem preencher os campos |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1wpRtpZh2PcQYruuJJ6-HUbECbztA2b22/view?usp=sharing) |

---

### 🐞 **Bug 08: Produto é cadastrado sem nome e sem valor**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-008 | Ao salvar o modal de produto vazio, o sistema cadastra o produto (código 7, tipo “Venda”, status “Ativo”) sem nenhuma validação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Produtos e abrir o modal de novo produto |
| 2. Não preencher nenhum campo |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O cadastro deve ser bloqueado com avisos de campos obrigatórios. | Produto criado sem nome e valor; “Total de produtos” passou de 2 para 3 e “Para venda” de 0 para 1. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de produtos | C34-CT05: Cadastrar produto sem preencher os campos |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1Y9xnEYWxzUPnp7z-_3xtDQlSkx0yHOH5/view?usp=sharing) |

---

### 🐞 **Bug 09: Pontuação é cadastrada sem datas (período 0000-00-00)**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-009 | Após informar apenas Nome, Tipo “Mensal” e Status “Ativo”, o sistema cadastra a pontuação sem Data Inicial e Data Final, exibindo o período “0000-00-00 — 0000-00-00”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Pontuação e clicar em “Nova Pontuação” |
| 2. Informar Nome, Tipo “Mensal” e Status “Ativo”, deixando as datas vazias |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve exigir as datas (ou tratar o período vazio) antes de gravar. | Pontuação gravada e listada com período “0000-00-00 — 0000-00-00”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de pontuações | C33-CT08: Validar o nome obrigatório ao cadastrar uma pontuação |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1ZherjpC1oDDIsjo2h2qQNwKXn08A0_39/view?usp=sharing) |

---

### 🐞 **Bug 10: Conta a pagar é cadastrada sem Título e sem Local de Pagamento**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-010 | O cadastro da conta #24 foi concluído com o campo Título em branco e Local Pagamento em “— Selecione —”; nenhum dos dois foi exigido. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Contas a Pagar e clicar em “Nova Conta” |
| 2. Selecionar o fornecedor pelo modal Buscar Fornecedor |
| 3. Preencher Tipo Doc., Doc. Fornecedor, Categoria e Valor, deixando Título e Local Pagamento vazios |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O sistema deve validar os campos necessários da conta antes de gravar. | Conta gravada (#24 – Centrion Web – R$ 200,00 – PENDENTE) sem Título e sem Local Pagamento. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de contas a pagar | C15-CT01: Cadastro de conta a pagar com busca de fornecedor |

| **Evidência(s)** |
| :---: |
| Evidência não registrada no cenário |

---

### 🐞 **Bug 11: Erro ao salvar a edição de uma pontuação (alteração válida)**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-011 | Ao alterar o status de “Desafio de Outubro” para “Inativo” e selecionar um produto de resgate, o sistema exibe “Erro ao salvar pontuação” e a alteração não é gravada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Pontuação e abrir (lupa) a pontuação “Desafio de Outubro” |
| 2. Alterar Status para “Inativo” e selecionar um produto em “Produtos de resgate” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A alteração deve ser salva e a listagem atualizada. | Modal “Erro – Erro ao salvar pontuação”; a pontuação continua “Ativa”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Edição de pontuações | C33-CT03: Tratar erro ao salvar a edição de uma pontuação |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/17rlYxRcvmZSKIoensH0pldTBkU3NX06o/view?usp=sharing) |

---

### 🐞 **Bug 12: “Erro no servidor” ao acionar ação da coluna Ações em Pontuação**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-012 | Ao acionar uma ação de uma pontuação na listagem, o sistema exibe “Erro no servidor – Erro interno inesperado” e a ação não é concluída. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Pontuação |
| 2. Acionar uma ação da coluna “Ações” em uma pontuação |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A ação deve ser processada com sucesso. | Modal “Erro no servidor – Erro interno inesperado”; ação não concluída. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Ações da listagem de pontuações | C33-CT06: Tratar erro do servidor ao acionar uma ação da pontuação |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1Ne4ay4CW_VtSYdFDLJzXFM_QZNMIB3yc/view?usp=sharing) |

---

### 🐞 **Bug 13: Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-013 | Mesmo com Nome, Pergunta e quatro respostas preenchidos, o cadastro de uma nova enquete não é concluído. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Enquetes e clicar em “Nova Enquete” |
| 2. Preencher Nome “Músculo” e Pergunta “Qual é a proteína mais indicada?” |
| 3. Adicionar quatro respostas pelo botão “+” |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A enquete deve ser cadastrada e aparecer na listagem. | Modal “Erro – Erro ao salvar enquete”; a enquete não é criada. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de enquetes | C35-CT02: Tratar erro ao cadastrar uma nova enquete |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1RbssKnL6GfKSsI4xUpaL4lWxSkU8wSD8/view?usp=sharing) |

---

### 🐞 **Bug 14: Edição de enquete existente retorna “Erro ao salvar enquete”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-014 | Ao tentar salvar alterações em uma enquete existente (sem pergunta cadastrada), o sistema exibe erro em todas as tentativas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Enquetes e abrir uma enquete existente |
| 2. Alterar os dados (ex.: informar a pergunta) |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| As alterações devem ser gravadas e refletidas na listagem. | Modal “Erro – Erro ao salvar enquete”; a enquete segue “Sem pergunta cadastrada”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Edição de enquetes | C35-CT03: Tratar erro ao editar uma enquete existente |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/15PBazaM8Wsb8qpbfW-f0oBQXLwXogc9p/view?usp=sharing) |

---

### 🐞 **Bug 15: Exclusão de enquete retorna “Erro ao deletar Enquete”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-015 | Após confirmar a exclusão, a enquete não é removida e o sistema exibe erro; o total permanece em 26. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Enquetes |
| 2. Clicar na ação de exclusão de uma enquete |
| 3. Confirmar no modal de segurança |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A enquete deve ser removida (ou o sistema deve explicar o motivo do bloqueio). | Modal “Erro – Erro ao deletar Enquete”; o total de enquetes continua 26. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Exclusão de enquetes | C35-CT04: Tratar erro ao excluir uma enquete com confirmação |

| **Evidência(s)** |
| :---: |
| (https://drive.google.com/file/d/1T5NkHzsYMznhO__HtoEpzEC5YpYpzEyW/view?usp=sharing) |

---

### 🐞 **Bug 16: Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-016 | Com aluno, personal, período, objetivo e observação preenchidos, “Criar Nova Ficha” não grava o registro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Fichas de Treino e clicar em “Cadastrar Ficha” |
| 2. Selecionar aluno e personal, definir o período, objetivo e observação |
| 3. Clicar em “Criar Nova Ficha” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A ficha deve ser criada e listada. | Modal “Erro: Erro ao salvar ficha”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de fichas de treino | C16-CT02: Cadastro de nova ficha de treino e tratamento de erro |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1LALWrCOEkAcFrakPxBBUhDb7UygDZnAY/view?usp=sharing) |

---

### 🐞 **Bug 17: Cadastro de objetivo de treino retorna “Erro ao salvar objetivo”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-017 | Ao cadastrar o objetivo “Perder Peso” com nome e descrição, o sistema exibe falha ao salvar. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Objetivos Treino e clicar em “+ Novo Objetivo” |
| 2. Preencher Nome e Descrição com “Perder Peso” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O objetivo deve ser salvo e listado. | Modal “Erro: Erro ao salvar objetivo”. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Cadastro de objetivos de treino | C19-CT01: Validação de erro no cadastro de novo objetivo |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1tYtIn2lU4Xf79VkMmJ1bmJ-wGZJWbfy3/view?usp=sharing) |

---

### 🐞 **Bug 18: Campo Status vazio ao abrir “Editar Turma”**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-018 | O modal Editar Turma exibe o campo Status sem valor, embora a turma esteja “Ativo”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Turmas |
| 2. Clicar no ícone de edição (lápis) da turma “Teste” (código 1) |
| 3. Observar o campo Status |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O Status atual (“Ativo”) deve vir preenchido. | O campo Status é exibido vazio. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Edição de turmas | C21-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 19: Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-019 | Ao editar uma turma e alterar “Tem Personal” para “Não”, o salvamento falha com modal de erro, impedindo uma edição que deveria ser válida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Abrir Editar Turma da turma código 1 |
| 2. Alterar o Nome e definir “Tem Personal” como “Não” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A turma deve ser salva sem personal. | Modal “Erro – Erro ao salvar turma.” |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Edição de turmas | C21-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 20: Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-020 | Após salvar com sucesso, o modal exibe por instantes a tela “Cadastrar Turma” em branco antes de voltar à listagem. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Editar a turma código 1 com dados válidos |
| 2. Clicar em “Salvar” |
| 3. Observar o modal até o retorno à listagem |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| O modal deve fechar direto, retornando à listagem. | Tela “Cadastrar Turma” vazia é exibida momentaneamente. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Edição de turmas | C21-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 21: Filtro de status (Pago/Vencido) não é aplicado em Contas a Pagar**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-021 | Ao filtrar por status “Pago” ou “Vencido”, a grade continua mostrando apenas contas PENDENTE. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Contas a Pagar |
| 2. Selecionar o status “Pago” (e depois “Vencido”) |
| 3. Clicar em buscar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| A listagem deve exibir somente contas do status escolhido. | A grade segue exibindo apenas contas PENDENTE. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Filtros de contas a pagar | C15-CT02: Filtros e consultas na listagem |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1pe00FBa5cAaZT2N24IScniBUCc-O-urr/view?usp=sharing) |

---

### 🐞 **Bug 22: Totais financeiros incorretos na listagem de Contas a Pagar**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-022 | Os cards “Total a Pagar” e “Valor Restante” permanecem em R$ 0 com contas de R$ 170,00 listadas, e contas PENDENTE exibem “Valor Pago” de R$ 170,00. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Contas a Pagar com contas de R$ 170,00 listadas |
| 2. Observar os cards Total a Pagar e Valor Restante |
| 3. Observar a coluna Valor Pago das contas PENDENTE |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Os cards devem refletir os valores listados e contas pendentes devem ter Valor Pago zerado. | Cards zerados e Valor Pago de R$ 170,00 em contas PENDENTE. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Indicadores financeiros de contas a pagar | C15-CT02: Filtros e consultas na listagem |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1pe00FBa5cAaZT2N24IScniBUCc-O-urr/view?usp=sharing) |

---

### 🐞 **Bug 23: Modal “Visualizar Conta a Pagar” exibe dados sem tratamento**

| **ID** | **Descrição** |
| ------ | ------------- |
| BUG-023 | O modal mostra valores técnicos e crus: Tipo “DESPESA_FORNECEDOR”, data “2025-10-01”, Categoria “13”, Tipo do documento “1”, campos Código e Doc. Fornecedor vazios e rótulos “Informacoes”/“Observacao” sem acento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| --- |
| 1. Acessar Contas a Pagar |
| 2. Abrir o modal de visualização de uma conta |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Dados formatados e legíveis (descrições no lugar de códigos, datas no padrão brasileiro, rótulos acentuados). | Códigos internos, data em formato ISO e rótulos sem acentuação. |

| **Ambiente** |
| --- |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Visualização de contas a pagar | C15-CT03: Dados do registro no modal Visualizar Conta a Pagar |

| **Evidência(s)** |
| :---: |
| [Vídeo 1](https://drive.google.com/file/d/1KiWx9QYxlleZDS9Ns09cYcaOk2zXi1lg/view?usp=sharing) |

---

## Pontos a confirmar

Casos em que o sistema exibiu erro, mas a causa pode ser uma regra de negócio esperada (por exemplo, registro com vínculos). Não foram classificados como bug até a confirmação:

| Caso de Teste | Comportamento observado | O que confirmar |
| --- | --- | --- |
| C11-CT04: Exclusão de cliente | Modal “Erro no servidor – Erro interno inesperado” | Se o cliente testado possuía vínculos (matrículas, cobranças) que justifiquem o bloqueio |
| C12-CT05: Exclusão de matrícula | Modal “Erro no servidor – Erro interno inesperado” | Se a matrícula possuía vínculos que justifiquem o bloqueio |
| C24-CT06: Busca de contas no fechamento de caixa | Modal “Erro ao buscar contas” com parâmetros/local de teste | Se o erro ocorre também com parâmetros válidos |

