## Cenário 49: Gerenciamento de Notificações

### Caso de Teste 01: Consulta ao Histórico Completo de Notificações e Seção de Denúncias

| ID | Descrição |
| --- | --- |
| **C49-CT01** | Validar a abertura e o fechamento do modal "Todas as notificações" e a exibição do estado da seção de Denúncias. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela do módulo **Aplicativo** (`/aplicativo`), com notificações já cadastradas. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela do **Aplicativo** e visualiza o bloco de notificações.<br> |
| **QUANDO** clicar no link **"Ver todas as notificações"**.<br> |
| **E** conferir o histórico listado no modal (código, mensagem, data e ações) e clicar em **"Fechar"**.<br> |
| **E** rolar a página até a seção **Denúncias**.<br> |
| **ENTÃO** o modal deve exibir todas as notificações enviadas aos alunos e ser fechado ao acionar "Fechar", e a seção de Denúncias deve exibir a mensagem *"Nenhuma denúncia pendente. Tudo tranquilo por aqui."* |

| **Critérios de Aceitação** |
| --- |
| O modal deve listar todo o histórico de notificações, fechar corretamente e a seção de Denúncias deve apresentar o feedback visual de ausência de registros pendentes. |

| **Evidência** |
| --- |
| Consulta ao Histórico Completo de Notificações e Seção de Denúncias |

---

### Caso de Teste 02: Moderação de Postagens e Alternância de Filtros em Postagens e Denúncias

| ID | Descrição |
| --- | --- |
| **C49-CT02** | Validar o modal "Todas as postagens" e a alternância dos filtros "Ver todas" e "Só pendentes" nas seções de Postagens e Denúncias. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza o card de **Postagens** e a seção de **Denúncias**.<br> |
| **QUANDO** clicar em **"Ver todas as postagens"** e alternar o filtro do modal entre **"Ver todas"** e **"Só pendentes"**.<br> |
| **E** clicar em **"Fechar"** e, na seção **Denúncias**, alternar o filtro entre **"Só pendentes"** e **"Ver todas"**.<br> |
| **ENTÃO** o modal deve exibir *"Nenhuma postagem aguardando aprovação."* no filtro de pendentes e *"Nenhuma postagem cadastrada."* no filtro geral, e a tabela de denúncias deve exibir *"Nenhuma denúncia registrada."* ou *"Nenhuma denúncia pendente. Tudo tranquilo por aqui."* conforme o filtro selecionado. |

| **Critérios de Aceitação** |
| --- |
| Os filtros devem alternar corretamente nas duas seções, atualizando a listagem e a mensagem de estado vazio de acordo com a opção selecionada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KOp5vCjrnrcYtjrX2Zoz64NXW-fY0HXl/view?usp=sharing |

---

### Caso de Teste 03: Criação e Envio de Notificação

| ID | Descrição |
| --- | --- |
| **C49-CT03** | Validar a abertura do modal de criação, o preenchimento da mensagem com prévia no celular e o envio do aviso aos alunos. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela do **Aplicativo**.<br> |
| **QUANDO** clicar no botão **"Criar Notificação"**.<br> |
| **E** preencher o campo de mensagem (ex.: *"Amanhã é feriado então a academia estará fechada"*) e acompanhar a **prévia no celular** sendo atualizada conforme a digitação.<br> |
| **E** clicar em **"Enviar aviso"**.<br> |
| **ENTÃO** o sistema deve fechar o modal e exibir a nova notificação no topo da listagem, com o próximo código sequencial e a data do envio. |

| **Critérios de Aceitação** |
| --- |
| O modal deve permitir redigir a mensagem com contador de caracteres e prévia em tempo real, e o envio deve registrar a notificação na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1OzqcksTnYFwNsUuz_HT1SJLMYPfHgjvh/view?usp=sharing |

---

### Caso de Teste 04: Visualização do Painel de Notificações do Cabeçalho

| ID | Descrição |
| --- | --- |
| **C49-CT04** | Validar a abertura do painel de notificações pelo ícone de sino e a alternância entre as abas "Tudo" e "Não lidas". |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela do **Aplicativo**.<br> |
| **QUANDO** clicar no ícone de **sino** no cabeçalho.<br> |
| **E** alternar entre as abas **"Tudo"** e **"Não lidas"** e clicar em **"Marcar como lidas"**.<br> |
| **ENTÃO** o painel deve exibir a mensagem *"Nada pendente por aqui. Você está em dia."* e ser fechado ao clicar fora dele. |

| **Critérios de Aceitação** |
| --- |
| O painel deve abrir pelo sino, permitir a alternância entre as abas, acionar "Marcar como lidas" sem erros e exibir o estado vazio quando não houver pendências. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11IwpgJbtiSGN97QXuVEOEyXB4dnfIWbS/view?usp=sharing |

---

### Caso de Teste 05: Acesso à Criação de Notificação pelo Modal do Histórico e Validação do Campo Vazio

| ID | Descrição |
| --- | --- |
| **C49-CT05** | Validar a transição do modal "Todas as notificações" para o modal de criação e o bloqueio do envio com a mensagem vazia. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**, com notificações cadastradas. |

| **Passos** |
| --- |
| **DADO** que o usuário abre o modal **"Todas as notificações"** pelo link "Ver todas as notificações".<br> |
| **QUANDO** clicar no botão **"Criar Notificação"** dentro do modal.<br> |
| **E** manter o campo de mensagem vazio.<br> |
| **ENTÃO** o sistema deve abrir o modal de criação com o campo em branco, contador em 0 caracteres, prévia exibindo *"Sua mensagem aparece aqui..."* e o botão **"Enviar aviso"** desabilitado. |

| **Critérios de Aceitação** |
| --- |
| A transição entre os modais deve ocorrer de forma fluida e o sistema não deve permitir o envio de uma notificação sem mensagem. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1cZB0kMcVyF7cDdNhkY66v9awtQ_jgiLj/view?usp=sharing |

---

### Caso de Teste 06: Visualização de Detalhes da Notificação

| ID | Descrição |
| --- | --- |
| **C49-CT06** | Validar a exibição do modal de detalhes de uma notificação já enviada através do ícone de lupa. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**, com notificações cadastradas na tabela. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a tabela de notificações.<br> |
| **QUANDO** clicar no ícone de **lupa** na linha de uma notificação.<br> |
| **E** conferir os dados exibidos e clicar em **"Fechar"**.<br> |
| **ENTÃO** o sistema deve abrir o modal **"Notificação"** (*"Aviso já enviado para os alunos"*) com o destinatário, o texto completo da mensagem e a prévia no celular, e fechá-lo ao acionar "Fechar". |

| **Critérios de Aceitação** |
| --- |
| O modal deve exibir corretamente o conteúdo da notificação enviada e retornar à listagem ao ser fechado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/196vHk2LtyhfqtUpLCnQ_bSpQxG_pKR97/view?usp=sharing |

---

### Caso de Teste 07: Exclusão de Notificação

| ID | Descrição |
| --- | --- |
| **C49-CT07** | Validar a exclusão de uma notificação a partir do ícone de lixeira na listagem. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do módulo **Aplicativo**, com notificações cadastradas na tabela. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a tabela de notificações.<br> |
| **QUANDO** clicar no ícone de **lixeira** na linha de uma notificação e confirmar a exclusão no alerta exibido.<br> |
| **ENTÃO** o sistema deve remover a notificação da listagem, mantendo os demais registros. |

| **Critérios de Aceitação** |
| --- |
| A exclusão deve ser concluída somente após a confirmação do operador e a tabela deve ser atualizada sem o registro removido. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DxvLcf9S527O5rrTHgmMDRtrtMCSxJvc/view?usp=sharing |
