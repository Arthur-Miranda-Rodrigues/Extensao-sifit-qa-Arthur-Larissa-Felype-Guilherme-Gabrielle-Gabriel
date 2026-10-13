
---

## Cenário de teste: Gerenciamento de Notificações e Conteúdos do Aplicativo

### Caso de Teste 01: Criar e enviar nova notificação para os alunos

| ID | Descrição |
| --- | --- |
| **CT-01** | Validar a criação e envio de uma notificação push para os usuários do aplicativo. |

| **Pré-condições** |
| --- |
| Usuário autenticado com acesso ao módulo **Aplicativo**. |

| **Passos** |
| --- |
| **DADO** que o usuário está no painel do **Aplicativo** |
| **E** clica no botão **Criar Notificação** |
| **QUANDO** selecionar o público-alvo no campo "Para" (ex: "Todos os alunos") |
| **E** preencher o campo "Mensagem" com o texto desejado |
| **E** clicar no botão **Enviar agora** |
| **ENTÃO** a notificação deve ser disparada e listada na tabela de notificações com o código, mensagem, data e opções de ação. |

| **Critérios de Aceitação** |
| --- |
| * A notificação criada deve aparecer imediatamente na listagem da dashboard do aplicativo. |
| * O contador de notificações deve atualizar conforme os registros cadastrados. |

---

### Caso de Teste 02: Visualizar detalhes e prévia de uma notificação

| ID | Descrição |
| --- | --- |
| **CT-02** | Validar a visualização dos detalhes e da prévia em tela de celular de uma notificação enviada. |

| **Pré-condições** |
| --- |
| Existir ao menos uma notificação cadastrada na listagem de notificações. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de notificações |
| **QUANDO** clicar no ícone de visualização (lupa) na coluna de ações de uma notificação |
| **ENTÃO** o sistema deve exibir um modal com as informações completas da mensagem e a "Prévia no Celular" simulando a exibição no dispositivo do aluno. |

---

### Caso de Teste 03: Excluir uma notificação

| ID | Descrição |
| --- | --- |
| **CT-03** | Validar a exclusão de uma notificação cadastrada. |

| **Pré-condições** |
| --- |
| Existir ao menos uma notificação cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de notificações |
| **QUANDO** clicar no ícone de lixeira referente à notificação que deseja remover |
| **ENTÃO** a notificação deve ser removida da listagem e o registro excluído do sistema. |

---

### Caso de Teste 04: Aprovar ou recusar postagens dos alunos

| ID | Descrição |
| --- | --- |
| **CT-04** | Validar a moderação de postagens enviadas por alunos no aplicativo. |

| **Pré-condições** |
| --- |
| Existir postagens pendentes ou aprovadas na seção de **Postagens**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a seção de **Postagens** ou a visualização em modal "Todas as postagens" |
| **E** clica na ação de detalhes/moderação de uma postagem |
| **QUANDO** analisar o conteúdo e clicar na ação de aprovar ou no botão **Recusar** |
| **ENTÃO** o status da postagem deve ser atualizado e refletir a decisão no aplicativo dos alunos. |

| **Critérios de Aceitação** |
| --- |
| * Ao recusar uma postagem, ela deve deixar de ser exibida na listagem pública do app. |
| * É possível alternar os filtros de visualização entre todas as postagens e apenas as pendentes ("Só pendentes"). |

https://jam.dev/c/a66417b7-b444-4398-80fe-5d796e569db8
