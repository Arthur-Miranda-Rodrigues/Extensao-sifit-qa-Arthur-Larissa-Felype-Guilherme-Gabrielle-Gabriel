
---

## Cenário: Gerenciamento de Atividades no SIFIT

### Caso de Teste 01: Buscar atividades por Código ou Nome



| ID | Descrição |
| --- | --- |
| **ATI-CT01** | O sistema deve permitir a filtragem de atividades cadastradas por código ou nome.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela de "Atividades".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de "Atividades"

 |
| **QUANDO** preencher o campo "Código" (ex: "3") e clicar em "Buscar"

 |
| **ENTÃO** o sistema deve listar apenas a atividade correspondente ao código informado

 |
| **E** ao limpar o código, preencher o campo "Nome da atividade" (ex: "Treinar 5x na semana") e clicar em "Buscar"

 |
| **ENTÃO** o sistema deve filtrar a listagem exibindo a atividade pesquisada.

 |

| **Critérios de aceitação** |
| --- |
| A tabela de atividades deve ser atualizada exibindo exclusivamente os registros que correspondem aos filtros inseridos.

 |

---

### Caso de Teste 02: Cadastrar uma nova atividade



| ID | Descrição |
| --- | --- |
| **ATI-CT02** | O sistema deve permitir o cadastro de uma nova atividade via modal "Nova Atividade".

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de "Atividades".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Atividade"

 |
| **E** preenche o campo "Nome" (ex: "Treino de perna")

 |
| **E** preenche a "Pontuação" (ex: "200")

 |
| **E** preenche a "Descrição" (ex: "Postar nas redes sociais")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** a nova atividade deve ser criada e exibida na listagem geral.

 |

| **Critérios de aceitação** |
| --- |
| A nova atividade deve aparecer na tabela e os contadores do topo da tela ("Total de atividades", "Com pontuação", "Com descrição") devem ser incrementados corretamente.

 |

---

### Caso de Teste 03: Visualizar e editar uma atividade



| ID | Descrição |
| --- | --- |
| **ATI-CT03** | O sistema deve permitir a visualização e atualização das informações de uma atividade existente.

 |

| **Pré-condições** |
| --- |
| Deve haver ao menos uma atividade cadastrada na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Visualizar/Editar" (lupa) de uma atividade (ex: Código 2 - "Postar todos os treinos")

 |
| **E** altera o campo "Descrição" (ex: acrescentando "que fizer nas redes sociais")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** o modal deve ser fechado e a descrição atualizada deve refletir na tabela de atividades.

 |

| **Critérios de aceitação** |
| --- |
| As edições realizadas nos campos da atividade devem ser salvas e exibidas imediatamente na listagem.

 |

 https://jam.dev/c/6471ff44-b8aa-437b-b41d-436061366b55
