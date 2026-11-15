# Relatório de Bugs

**Software:** SIFIT

**QA responsável:**

* Arthur Miranda Rodrigues — RA 14538
* Larissa Fernanda O. — RA 14536
* Felype Augusto Dos Santos Silva — RA 14537
* Guilherme Felipe de Morais — RA 5608
* Gabrielle Bonini Barbosa — RA 14506
* Gabriel de Abreu da Silva — RA 14525

**Data:** 29.10.26 (atualizado em 14.11.26)

### 🐞 **Bug 01: Link “Esqueci minha senha” não executa nenhuma ação**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-001 | Ao clicar no link “Esqueci minha senha” na tela de login, nada acontece: o usuário não é levado a nenhuma tela ou modal de recuperação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar a página de login do SIFIT |
| 2. Clicar no link “Esqueci minha senha” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O sistema deve direcionar o usuário para a tela ou modal de recuperação/redefinição de senha. | Nada acontece; o usuário permanece na tela de login. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Login – recuperação de senha | C01-CT04: Acesso à funcionalidade de recuperação de senha |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1UVEJmPtjgyMDTs_6nrJcX1i0ldW5D671/view?usp=sharing) |

---

### 🐞 **Bug 02: Botão “Buscar” não filtra as aulas por período (data digitada ou calendário)**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-002 | Na tela SifitBox – Aulas, tanto digitando as datas manualmente quanto escolhendo-as no calendário, ao clicar em “Buscar” a grade de resultados não é atualizada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar SifitBox > Aulas (/sifitbox/aulas) |
| 2. Informar data inicial e final, digitando ou usando o calendário |
| 3. Clicar em “Buscar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A listagem de aulas deve ser filtrada pelo período informado. | Nada acontece; a grade de aulas permanece inalterada nos dois fluxos. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| SifitBox – filtro de aulas por período | SifitBox-CT01: Busca por período digitando a data<br>SifitBox-CT02: Busca por período pelo calendário (cenário sem arquivo na pasta) |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1ur0S1lqeUewf-7JjUdG8A7UQDedM6fG-/view?usp=sharing) |
| (https://drive.google.com/file/d/1UIIlC-LJzgxh4_FljfFwLVdNQu6s38rs/view?usp=sharing) |

---

### 🐞 **Bug 03: Sistema aceita data final anterior à data inicial sem exibir validação**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-003 | É possível acionar a busca com data final anterior à inicial; não há mensagem de erro e a tela não reage. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar SifitBox > Aulas |
| 2. Informar uma data final anterior à data inicial |
| 3. Clicar em “Buscar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O sistema deve impedir o intervalo ilógico e exibir feedback de validação ao usuário. | Nenhuma validação é exibida e a tela permanece inalterada. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| SifitBox – validação de período | SifitBox-CT03: Validação de data inválida (data final anterior à inicial) |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1nk7_GCZVk_qjFUQzqTWe3PwbjEzkIzDi/view?usp=sharing) |

---

### 🐞 **Bug 04: Botão “Gerar aulas” não executa nenhum fluxo**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-004 | Ao clicar em “Gerar aulas”, o botão é acionado visualmente mas nenhum modal é aberto nem processo é disparado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar SifitBox > Aulas |
| 2. Clicar no botão “Gerar aulas” (canto superior direito) |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O sistema deve executar a geração de aulas ou informar claramente a indisponibilidade da função. | Nada acontece; a grade de aulas continua idêntica e não há feedback. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| SifitBox – geração de aulas | SifitBox-CT04: Acionamento da funcionalidade de gerar aulas |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1eYJda_JSQM0i3tcBcWGAhPR-JWK89ElN/view?usp=sharing) |

---

### 🐞 **Bug 05: “Finalizar Anamnese” não conclui a ficha**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-005 | Ao finalizar a anamnese de um aluno, a ficha não é gerada: em um fluxo nada acontece e a listagem continua com “Nenhuma ficha encontrada”; no outro é exibido o pop-up “Erro no servidor”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Fichas de Anamnese e clicar em “Nova Anamnese” |
| 2. Buscar e selecionar o aluno, escolher um modelo e clicar em “Iniciar” |
| 3. Responder as perguntas e, em “Revisar e Finalizar”, clicar em “Finalizar Anamnese” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A ficha deve ser finalizada e aparecer na listagem de fichas. | A ação não conclui (nenhuma resposta ou pop-up “Erro no servidor”) e a listagem mantém “Nenhuma ficha encontrada”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Aplicação de fichas de anamnese | C40-CT01: Buscar aluno e selecionar modelo de anamnese<br>C40-CT02: Finalização com erro no servidor e salvamento de rascunho |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1V7sDdPIEofzjCAJTtkYiNBRupi0qRDVc/view?usp=sharing) |
| (https://drive.google.com/file/d/1TxdKmCaGbufBF7FS42Sx4AtkSjMvqGQ0/view?usp=sharing) |

---

### 🐞 **Bug 06: Grupo muscular é cadastrado sem Nome e sem Tipo Membro**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-006 | Ao salvar o modal com apenas a imagem, o sistema grava o registro mesmo com os campos obrigatórios vazios. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Grupos Musculares e clicar em “+” |
| 2. Selecionar apenas a imagem, deixando Nome e Tipo Membro vazios |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O cadastro deve ser bloqueado com mensagem indicando Nome e Tipo Membro como obrigatórios. | O grupo muscular é cadastrado sem os dados obrigatórios. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de grupos musculares | C17-CT04: Cadastro sem preencher Nome e Tipo Membro |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/16umD_rrlyjFLRKMBB-g0nF2_dc9_e5V8/view?usp=sharing) |

---

### 🐞 **Bug 07: Atividade é cadastrada com todos os campos em branco**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-007 | Ao salvar o modal “Atividade” vazio, o sistema cria a atividade (código 6) sem nome, pontuação e descrição, sem exibir validação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Atividades e clicar em “Nova Atividade” |
| 2. Não preencher Nome, Pontuação nem Descrição |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O cadastro deve ser bloqueado e a obrigatoriedade dos campos indicada. | Atividade criada em branco; “Total de atividades” passou de 5 para 6 e “Sem pontuação” de 0 para 1. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de atividades | C31-CT03: Cadastrar atividade sem preencher os campos |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1wpRtpZh2PcQYruuJJ6-HUbECbztA2b22/view?usp=sharing) |

---

### 🐞 **Bug 08: Produto é cadastrado sem nome e sem valor**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-008 | Ao salvar o modal de produto vazio, o sistema cadastra o produto (código 7, tipo “Venda”, status “Ativo”) sem nenhuma validação. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Produtos e abrir o modal de novo produto |
| 2. Não preencher nenhum campo |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O cadastro deve ser bloqueado com avisos de campos obrigatórios. | Produto criado sem nome e valor; “Total de produtos” passou de 2 para 3 e “Para venda” de 0 para 1. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de produtos | C33-CT05: Cadastrar produto sem preencher os campos |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1Y9xnEYWxzUPnp7z-_3xtDQlSkx0yHOH5/view?usp=sharing) |

---

### 🐞 **Bug 09: Pontuação é cadastrada sem datas (período 0000-00-00)**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-009 | Após informar apenas Nome, Tipo “Mensal” e Status “Ativo”, o sistema cadastra a pontuação sem Data Inicial e Data Final, exibindo o período “0000-00-00 — 0000-00-00”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Pontuação e clicar em “Nova Pontuação” |
| 2. Informar Nome, Tipo “Mensal” e Status “Ativo”, deixando as datas vazias |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O sistema deve exigir as datas (ou tratar o período vazio) antes de gravar. | Pontuação gravada e listada com período “0000-00-00 — 0000-00-00”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de pontuações | C32-CT08: Validar o nome obrigatório ao cadastrar uma pontuação |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1ZherjpC1oDDIsjo2h2qQNwKXn08A0_39/view?usp=sharing) |

---

### 🐞 **Bug 10: Conta a pagar é cadastrada sem Título e sem Local de Pagamento**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-010 | O cadastro da conta #24 foi concluído com o campo Título em branco e Local Pagamento em “— Selecione —”; nenhum dos dois foi exigido. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Contas a Pagar e clicar em “Nova Conta” |
| 2. Selecionar o fornecedor pelo modal Buscar Fornecedor |
| 3. Preencher Tipo Doc., Doc. Fornecedor, Categoria e Valor, deixando Título e Local Pagamento vazios |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O sistema deve validar os campos necessários da conta antes de gravar. | Conta gravada (#24 – Centrion Web – R$ 200,00 – PENDENTE) sem Título e sem Local Pagamento. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de contas a pagar | C14-CT01: Cadastro de conta a pagar com busca de fornecedor |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1zmLTSjJmBhcbql_hep55h1l-ekmKXc3B/view?usp=sharing) |

---

### 🐞 **Bug 11: Erro ao salvar a edição de uma pontuação (alteração válida)**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-011 | Ao alterar o status de “Desafio de Outubro” para “Inativo” e selecionar um produto de resgate, o sistema exibe “Erro ao salvar pontuação” e a alteração não é gravada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Pontuação e abrir (lupa) a pontuação “Desafio de Outubro” |
| 2. Alterar Status para “Inativo” e selecionar um produto em “Produtos de resgate” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A alteração deve ser salva e a listagem atualizada. | Modal “Erro – Erro ao salvar pontuação”; a pontuação continua “Ativa”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de pontuações | C32-CT03: Tratar erro ao salvar a edição de uma pontuação |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/17rlYxRcvmZSKIoensH0pldTBkU3NX06o/view?usp=sharing) |

---

### 🐞 **Bug 12: “Erro no servidor” ao acionar ação da coluna Ações em Pontuação**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-012 | Ao acionar uma ação de uma pontuação na listagem, o sistema exibe “Erro no servidor – Erro interno inesperado” e a ação não é concluída. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Pontuação |
| 2. Acionar uma ação da coluna “Ações” em uma pontuação |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A ação deve ser processada com sucesso. | Modal “Erro no servidor – Erro interno inesperado”; ação não concluída. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Ações da listagem de pontuações | C32-CT06: Tratar erro do servidor ao acionar uma ação da pontuação |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1Ne4ay4CW_VtSYdFDLJzXFM_QZNMIB3yc/view?usp=sharing) |

---

### 🐞 **Bug 13: Cadastro de enquete com dados válidos retorna “Erro ao salvar enquete”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-013 | Mesmo com Nome, Pergunta e quatro respostas preenchidos, o cadastro de uma nova enquete não é concluído. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Enquetes e clicar em “Nova Enquete” |
| 2. Preencher Nome “Músculo” e Pergunta “Qual é a proteína mais indicada?” |
| 3. Adicionar quatro respostas pelo botão “+” |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A enquete deve ser cadastrada e aparecer na listagem. | Modal “Erro – Erro ao salvar enquete”; a enquete não é criada. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de enquetes | C34-CT02: Tratar erro ao cadastrar uma nova enquete |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1RbssKnL6GfKSsI4xUpaL4lWxSkU8wSD8/view?usp=sharing) |

---

### 🐞 **Bug 14: Edição de enquete existente retorna “Erro ao salvar enquete”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-014 | Ao tentar salvar alterações em uma enquete existente (sem pergunta cadastrada), o sistema exibe erro em todas as tentativas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Enquetes e abrir uma enquete existente |
| 2. Alterar os dados (ex.: informar a pergunta) |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| As alterações devem ser gravadas e refletidas na listagem. | Modal “Erro – Erro ao salvar enquete”; a enquete segue “Sem pergunta cadastrada”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de enquetes | C34-CT03: Tratar erro ao editar uma enquete existente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/15PBazaM8Wsb8qpbfW-f0oBQXLwXogc9p/view?usp=sharing) |

---

### 🐞 **Bug 15: Exclusão de enquete retorna “Erro ao deletar Enquete”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-015 | Após confirmar a exclusão, a enquete não é removida e o sistema exibe erro; o total permanece em 26. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Enquetes |
| 2. Clicar na ação de exclusão de uma enquete |
| 3. Confirmar no modal de segurança |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A enquete deve ser removida (ou o sistema deve explicar o motivo do bloqueio). | Modal “Erro – Erro ao deletar Enquete”; o total de enquetes continua 26. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Exclusão de enquetes | C34-CT04: Tratar erro ao excluir uma enquete com confirmação |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1T5NkHzsYMznhO__HtoEpzEC5YpYpzEyW/view?usp=sharing) |

---

### 🐞 **Bug 16: Cadastro de ficha de treino com dados válidos retorna “Erro ao salvar ficha”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-016 | Com aluno, personal, período, objetivo e observação preenchidos, “Criar Nova Ficha” não grava o registro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Fichas de Treino e clicar em “Cadastrar Ficha” |
| 2. Selecionar aluno e personal, definir o período, objetivo e observação |
| 3. Clicar em “Criar Nova Ficha” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A ficha deve ser criada e listada. | Modal “Erro: Erro ao salvar ficha”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de fichas de treino | C15-CT02: Cadastro de nova ficha de treino e tratamento de erro |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1LALWrCOEkAcFrakPxBBUhDb7UygDZnAY/view?usp=sharing) |

---

### 🐞 **Bug 17: Cadastro de objetivo de treino retorna “Erro ao salvar objetivo”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-017 | Ao cadastrar o objetivo “Perder Peso” com nome e descrição, o sistema exibe falha ao salvar. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Objetivos Treino e clicar em “+ Novo Objetivo” |
| 2. Preencher Nome e Descrição com “Perder Peso” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O objetivo deve ser salvo e listado. | Modal “Erro: Erro ao salvar objetivo”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de objetivos de treino | C18-CT01: Validação de erro no cadastro de novo objetivo |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1tYtIn2lU4Xf79VkMmJ1bmJ-wGZJWbfy3/view?usp=sharing) |

---

### 🐞 **Bug 18: Campo Status vazio ao abrir “Editar Turma”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-018 | O modal Editar Turma exibe o campo Status sem valor, embora a turma esteja “Ativo”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Turmas |
| 2. Clicar no ícone de edição (lápis) da turma “Teste” (código 1) |
| 3. Observar o campo Status |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O Status atual (“Ativo”) deve vir preenchido. | O campo Status é exibido vazio. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de turmas | C20-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 19: Erro “Erro ao salvar turma” ao editar com “Tem Personal” = Não**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-019 | Ao editar uma turma e alterar “Tem Personal” para “Não”, o salvamento falha com modal de erro, impedindo uma edição que deveria ser válida. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Abrir Editar Turma da turma código 1 |
| 2. Alterar o Nome e definir “Tem Personal” como “Não” |
| 3. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A turma deve ser salva sem personal. | Modal “Erro – Erro ao salvar turma.” |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de turmas | C20-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 20: Modal “Cadastrar Turma” vazio aparece brevemente após salvar a edição**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-020 | Após salvar com sucesso, o modal exibe por instantes a tela “Cadastrar Turma” em branco antes de voltar à listagem. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |            Baixa           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Editar a turma código 1 com dados válidos |
| 2. Clicar em “Salvar” |
| 3. Observar o modal até o retorno à listagem |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O modal deve fechar direto, retornando à listagem. | Tela “Cadastrar Turma” vazia é exibida momentaneamente. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de turmas | C20-CT04: Edição e atualização de turma existente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1niaHnjS3nIgZb3nC8leo1kYPb05Dd_o_/view?usp=sharing) |

---

### 🐞 **Bug 21: Modal “Visualizar Conta a Pagar” exibe dados sem tratamento**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-021 | O modal mostra valores técnicos e crus: Tipo “DESPESA_FORNECEDOR”, data “2025-10-01”, Categoria “13”, Tipo do documento “1”, campos Código e Doc. Fornecedor vazios e rótulos “Informacoes”/“Observacao” sem acento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |            Baixa           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Contas a Pagar |
| 2. Abrir o modal de visualização de uma conta |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| Dados formatados e legíveis (descrições no lugar de códigos, datas no padrão brasileiro, rótulos acentuados). | Códigos internos, data em formato ISO e rótulos sem acentuação. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Visualização de contas a pagar | C14-CT03: Dados do registro no modal Visualizar Conta a Pagar |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1KiWx9QYxlleZDS9Ns09cYcaOk2zXi1lg/view?usp=sharing) |

---

### 🐞 **Bug 22: Baixo contraste nos títulos e informações dos gráficos do Dashboard**

**Data:** 18/10/2026

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-022 | Ao acessar o Dashboard do SIFIT, alguns títulos e textos dos gráficos apresentam cores muito próximas às do fundo, dificultando a leitura e a interpretação das informações gerenciais da academia. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Média           |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar a página de login do SIFIT |
| 2. Informar credenciais válidas e realizar a autenticação |
| 3. Na página inicial, localizar o menu lateral |
| 4. Clicar na opção "Dashboard" |
| 5. Observar os títulos e as informações apresentados nos gráficos de clientes e matrículas |
| 6. Identificar os textos com baixo contraste em relação ao fundo dos gráficos |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| Os títulos, legendas e informações dos gráficos devem possuir contraste adequado em relação ao fundo, permitindo que o usuário visualize e interprete os indicadores gerenciais com facilidade. | Os gráficos são carregados, porém alguns títulos e informações aparecem com cores muito próximas às do fundo, comprometendo a legibilidade e dificultando a interpretação dos dados. |

| **Ambiente** |
| ------------ |
| Sistema: SIFIT — Gestão de Academias |
| Ambiente: Sistema web |
| Dispositivo: Desktop |
| Página afetada: Dashboard |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Dashboard / Visualização de indicadores e gráficos | C07-CT04: Acesso ao Dashboard após login bem-sucedido |

| **Evidência(s)** |
| :--------------: |
| (https://jam.dev/c/97986eeb-3c8c-4cfe-bf54-7b1155e95f28) |

---

### 🐞 **Bug 23: Erro ao salvar modelo de contrato (aba/listagem permanece em branco)**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-023 | Ao preencher o formulário de cadastro de modelo de contrato e clicar em "Salvar modelo", o sistema redireciona para a tela de Modelos Contrato, porém a listagem fica inteiramente em branco. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|          Alta         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar o módulo de Modelos de Contrato |
| 2. Preencher o Título do Modelo, selecionar o Status e redigir o corpo do contrato no editor |
| 3. Clicar no botão **Salvar modelo** |
| 4. Observar a tela de retorno da aplicação |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O contrato deve ser salvo e listado corretamente na tabela principal de Modelos de Contrato. | O sistema redireciona para a página `/modelos-contrato`, mas a listagem/tabela é exibida completamente vazia/em branco. |

| **Ambiente** |
| ------------ |
| Ambiente Web de Testes do SIFIT. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Comercial – Modelos de Contrato | C37-CT08: Salvamento de modelo de contrato |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/12P2uS8dl4YBUixY1DvnlzWbtJkUEMj_d/view?usp=sharing) |

---

### 🐞 **Bug 24: Filtro de status (Vencido/Pago) não é aplicado em Contas a Pagar**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-024 | Na tela Contas a Pagar, ao selecionar o status “Vencido” (ou “Pago”) e clicar em “Buscar”, o filtro de status não é aplicado: a grade continua listando as mesmas 5 contas, com status PAGO e PENDENTE, e o indicador “Contas Atrasadas” permanece em 0. O resultado não muda ao alternar o Tipo de Data entre Pagamento e Vencimento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Contas a Pagar |
| 2. Informar o nome “centrion” e o período de 14/10/2026 a 30/11/2026 |
| 3. Selecionar o status “Vencido” |
| 4. Alternar o Tipo de Data entre “Pagamento” e “Vencimento” |
| 5. Clicar em “Buscar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A listagem deve exibir somente as contas com o status selecionado (ou a mensagem de lista vazia, se não houver nenhuma). | A grade continua exibindo as 5 contas (#28 e #27 PAGO; #25, #24 e #20 PENDENTE), sem aplicar o filtro de status. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Filtros de contas a pagar | C14-CT02: Filtros e consultas na listagem |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1Up4ktSX250_G9l6ig_TXmISv9kXwxdMa/view?usp=sharing) |

---

### 🐞 **Bug 25: Exclusão de cliente retorna “Erro no servidor – Erro interno inesperado”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-025 | Ao confirmar a exclusão de um cliente na listagem, a exclusão não é concluída e o sistema exibe o modal “Erro no servidor – Erro interno inesperado”, sem explicar a causa. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Clientes |
| 2. Localizar um cliente na tabela de listagem |
| 3. Clicar no ícone de exclusão (lixeira) na linha do cliente |
| 4. Confirmar a ação no modal de segurança |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O cliente deve ser removido da listagem (ou o sistema deve informar claramente o motivo do bloqueio, como vínculos existentes). | Modal “Erro no servidor – Erro interno inesperado” com o botão Fechar; a exclusão não é concluída. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Exclusão de clientes | C10-CT04: Tratamento de exceção em tentativa de exclusão de cliente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1dB9oVQTKlkFWpnpEquTj4H1j7zWHehcK/view?usp=sharing) |

---

### 🐞 **Bug 26: Exclusão de matrícula retorna “Erro no servidor – Erro interno inesperado”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-026 | Ao confirmar a exclusão de uma matrícula na listagem, a exclusão não é concluída e o sistema exibe o modal “Erro no servidor – Erro interno inesperado”, sem explicar a causa. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Matrículas |
| 2. Localizar um registro na tabela de matrículas |
| 3. Clicar no ícone de exclusão (lixeira) |
| 4. Confirmar a ação no modal de aviso (“Confirmar”) |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A matrícula deve ser removida da listagem (ou o sistema deve informar claramente o motivo do bloqueio, como vínculos existentes). | Modal “Erro no servidor – Erro interno inesperado” com o botão Fechar; a exclusão não é concluída. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Exclusão de matrículas | C11-CT05: Tratamento de exceção na exclusão de matrícula |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1X9xK6XSKGRbmEC3EHtsq96WgOTXHjnoK/view?usp=sharing) |

---

### 🐞 **Bug 27: Busca de contas no fechamento de caixa retorna “Erro ao buscar contas”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-027 | Na janela de fechamento de caixa, ao ajustar os parâmetros de data ou selecionar um local de contas de teste e clicar em “Buscar Contas”, o sistema exibe “Erro: Erro ao buscar contas”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Caixas (módulo Financeiro) e abrir o painel de fechamento do caixa |
| 2. Ajustar os parâmetros de data ou selecionar um local de contas de teste |
| 3. Clicar no botão “Buscar Contas” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| As contas devem ser listadas conforme os parâmetros informados (ou o sistema deve orientar claramente o ajuste dos parâmetros). | Modal “Erro: Erro ao buscar contas”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Fechamento de caixa – busca de contas | C23-CT06: Tratamento de erro na busca de contas com parâmetros inválidos |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1vyBD4X36a7QDvDsLktQFzKYjN7vO15yb/view?usp=sharing) |

---

### 🐞 **Bug 28: Cadastro de bandeira de cartão não salva e a listagem continua vazia**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-028 | Ao preencher nome, taxas e regra de parcelamento de uma nova bandeira e clicar em “Salvar”, nada acontece e a listagem continua com “Nenhuma bandeira encontrada.” |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Bandeiras de Cartão e clicar em “Nova Bandeira” |
| 2. Preencher Nome (ex.: “Bandeira Azul”), Taxa Adicional (ex.: 20,00) e Taxa Débito (ex.: 10,00) |
| 3. Clicar em “+ Adicionar Parcela”, informar o número da parcela e a taxa e confirmar com o ícone de check |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A nova bandeira, com suas taxas e parcelas, deve ser gravada e exibida na listagem. | Nada acontece ao salvar; a listagem continua vazia com a mensagem “Nenhuma bandeira encontrada.” |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de bandeiras de cartão | C39-CT02: Cadastro de nova bandeira com taxas e regras de parcelamento |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1C8jVC7gSKOwovdkp4g04xzEWm9ywy1Vp/view?usp=sharing) |

---

### 🐞 **Bug 29: Edição do tipo de resposta de pergunta de anamnese retorna “Erro ao salvar pergunta”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-029 | Ao alterar o Tipo Resposta de uma pergunta de anamnese cadastrada e clicar em “Salvar”, a alteração não é gravada e o sistema exibe o modal “Erro ao salvar pergunta”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Perguntas de Anamnese |
| 2. Clicar no ícone de edição de uma pergunta (ex.: código 4) |
| 3. Alterar o Tipo Resposta (ex.: de “Sim e Não” para “Sim, Não e Não Sei”) |
| 4. Clicar em “Salvar” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A alteração deve ser gravada e refletida na listagem. | O indicador de salvamento aparece e em seguida o modal “Erro ao salvar pergunta”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Edição de perguntas de anamnese | C43-CT02: Validação de erro ao tentar editar pergunta existente |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1YFPpJy7qa9TTkabG3R07Z8GTdehrgKVb/view?usp=sharing) |

---

### 🐞 **Bug 30: Erro ao salvar configurações gerais na aba Home**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-030 | Ao alterar parâmetros de acesso e presença na aba “Home” das Configurações e clicar em “Salvar Configurações”, as alterações não são gravadas e o sistema exibe “Erro ao salvar configurações”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações, aba “Home” |
| 2. Alterar campos como plano, controle de presença, cobrança de multa ou regras de dias de tolerância |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| As configurações devem ser salvas, com confirmação ao usuário. | Modal “Erro ao salvar configurações”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Home | C46-CT01: Configurações gerais do sistema (aba Home) |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1Ue_F9SKo6he9NbKaP6uEFCGlV0Dm25ND/view?usp=sharing) |

---

### 🐞 **Bug 31: Erro ao salvar configurações de biometria e catraca**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-031 | Ao informar marca, modelo, IP e porta da catraca na aba “Biometria” e clicar em “Salvar Configurações”, o sistema retorna aviso de erro de comunicação/servidor e as configurações não são gravadas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e clicar na aba “Biometria” |
| 2. Configurar os dados da catraca (ex.: marca, modelo “idFace Max”, IP e porta) |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| As configurações de biometria devem ser salvas, com confirmação ao usuário. | Aviso de erro de comunicação/servidor ao salvar. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Biometria | C46-CT02: Configuração de biometria e integração com catraca |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1FTSpetaE1hofI9WHcqO7lcsqxgcHWNcy/view?usp=sharing) |

---

### 🐞 **Bug 32: Erro ao salvar parâmetros de avaliação física nas configurações**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-032 | Ao alterar cobrança, tipo de avaliação e dias de validade na aba “Avaliação” e clicar em “Salvar Configurações”, o sistema exibe pop-up de erro e as alterações não são gravadas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e clicar na aba “Avaliação” |
| 2. Alterar os parâmetros de cobrança, o tipo de avaliação (ex.: “Bioimpedância” ou “Dobras”) e a duração em dias |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| Os parâmetros de avaliação devem ser salvos, com confirmação ao usuário. | Pop-up de erro ao salvar. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Avaliação | C46-CT03: Configurações de parâmetros de avaliação física |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/199mT6aQqWizaHXdiT_lDbr3ZqQiqLvn4/view?usp=sharing) |

---

### 🐞 **Bug 33: Erro ao salvar mensagens automáticas de aniversário nas configurações**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-033 | Ao habilitar o envio automático e editar os templates de WhatsApp, SMS e E-mail na aba “Aniversário” e clicar em “Salvar Configurações”, o sistema retorna mensagem de erro e as alterações não são gravadas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e selecionar a aba “Aniversário” |
| 2. Habilitar o envio automático e editar os textos dos templates de WhatsApp, SMS e E-mail usando as variáveis disponíveis |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| Os templates e a habilitação do envio devem ser salvos, com confirmação ao usuário. | Mensagem de erro padrão ao salvar. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Aniversário | C46-CT04: Configuração de mensagens automáticas de aniversário |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1-DIIr04YSAVkigvUP-oXod3RlCyPaS5G/view?usp=sharing) |

---

### 🐞 **Bug 34: Erro ao salvar pagamento online e token de integração nas configurações**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-034 | Ao habilitar o pagamento online e informar o token de integração na aba “Pagamento” e clicar em “Salvar Configurações”, o sistema exibe aviso de erro e as credenciais não são gravadas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e navegar até a aba “Pagamento” |
| 2. Habilitar o pagamento online e preencher o token de integração (ex.: “adsatas”) |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| Os parâmetros de pagamento online e o token devem ser salvos, com confirmação ao usuário. | Aviso de erro ao salvar. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Pagamento | C46-CT05: Configuração de pagamento online e integração de gateway |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1cFCj1YBRS4qtsM2I_Wja83Zb1VfPq8Vp/view?usp=sharing) |

---

### 🐞 **Bug 35: Erro de conectividade/servidor ao salvar integração com WhatsApp nas configurações**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-035 | Ao preencher URL do servidor, ID da instância e Token na aba “Integrações” e clicar em “Salvar Configurações”, o sistema exibe avisos de erro de conectividade/servidor e a integração não é registrada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e a aba “Integrações” |
| 2. Preencher os dados de conexão do provedor de API (URL do servidor, ID da instância e Token) e marcar a opção de uso nas automações |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| A integração deve ser registrada com sucesso, com confirmação ao usuário. | Avisos de erro de conectividade/servidor ao salvar. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Integrações | C46-CT06: Configuração e conexão de integrações (WhatsApp Business) |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1NeCFnDQ5YYrpI1d3yEE-cyz7FGKlhkAJ/view?usp=sharing) |

---

### 🐞 **Bug 36: Erro ao salvar identidade visual (cores, logotipo e capa) nas configurações**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-036 | Ao alterar as cores e enviar as imagens de logotipo e capa na aba “Design”, os arquivos são carregados na interface, mas ao clicar em “Salvar Configurações” o sistema exibe erro de salvamento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Configurações e clicar na aba “Design” |
| 2. Alterar os códigos de cores da paleta e fazer o upload das imagens de Logo e Capa |
| 3. Clicar em “Salvar Configurações” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| As cores e imagens devem ser salvas e aplicadas à identidade visual da academia. | Os arquivos são carregados na interface, mas ocorre erro de salvamento ao concluir. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Configurações – aba Design | C46-CT07: Personalização de identidade visual e design da academia |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1XW5h-qeF8quwLCDUrDHTUFCgZvMHwzlW/view?usp=sharing) |

---

### 🐞 **Bug 37: Cadastro de modelo de ficha retorna “Erro ao salvar modelo”**

| **ID**  | **Descrição** |
| ------- | ------------- |
| BUG-037 | Ao preencher o nome do modelo e selecionar o personal e clicar em “Criar Modelo”, o modelo não é gravado e o sistema exibe o modal “Erro ao salvar modelo”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ------------------------------------ |
| 1. Acessar Modelos de Ficha e clicar no botão de adicionar (+) |
| 2. Preencher o campo “Nome do Modelo” (ex.: “Hipertorfia”) e selecionar um personal (ex.: “Gabriella”) |
| 3. Clicar em “Criar Modelo” |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :------------------------: | :----------------------: |
| O modelo de ficha deve ser criado e exibido na listagem. | Modal de alerta “Erro ao salvar modelo”. |

| **Ambiente** |
| ------------ |
| Ambiente de testes do SIFIT (aplicação web). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :------------------------: | :---------------------------: |
| Cadastro de modelos de ficha | C47-CT01: Criação de novo modelo de ficha e tratamento de erro na gravação |

| **Evidência(s)** |
| :--------------: |
| (https://drive.google.com/file/d/1oDvPksSC7n5nHmVQXFQ5rCnqqPbTm7zS/view?usp=sharing) |
