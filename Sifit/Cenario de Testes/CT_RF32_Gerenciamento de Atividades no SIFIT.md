## Cenário 32: Gerenciamento de Atividades no SIFIT

### Caso de Teste 01: Buscar atividades por Nome e por Código

| ID | Descrição |
| --- | --- |
| **C32-CT01** | O sistema deve permitir a filtragem das atividades cadastradas por nome ou por código. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela "Atividades", com atividades cadastradas (ex.: "Treinar 5x na semana", código 1, e "Treino de perna", código 4). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Atividades" |
| **QUANDO** preencher o campo "Nome" com "Treinar 5x na semana" e clicar em "Buscar" |
| **ENTÃO** o sistema deve listar apenas a atividade correspondente (1 registro) |
| **E** ao limpar o campo "Nome", preencher o campo "Código" com "4" e clicar em "Buscar" |
| **ENTÃO** o sistema deve listar apenas a atividade "Treino de perna" (1 registro) |
| **E** ao limpar os filtros, a listagem completa deve ser exibida novamente. |

| **Critérios de Aceitação** |
| --- |
| A tabela de atividades deve ser atualizada exibindo exclusivamente os registros que correspondem aos filtros informados. |
| O rodapé da tabela deve refletir a quantidade de registros exibidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nnuRc1dknHmmV5r0KSnz61Gm5VjONScY/view?usp=sharing |

---

### Caso de Teste 02: Cadastrar uma nova atividade

| ID | Descrição |
| --- | --- |
| **C32-CT02** | O sistema deve permitir o cadastro de uma nova atividade por meio do modal "Atividade". |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Atividades". |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Atividade" |
| **E** preenche o campo "Nome" com "Treino de Peito" |
| **E** preenche o campo "Pontuação" com "300" |
| **E** preenche o campo "Descrição" com "Treino de peito" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** a nova atividade deve ser criada |
| **E** exibida na listagem geral com o código gerado automaticamente. |

| **Critérios de Aceitação** |
| --- |
| A nova atividade deve aparecer na tabela com nome, descrição e pontuação informados. |
| Os indicadores do topo ("Total de atividades", "Com pontuação" e "Com descrição") devem ser incrementados corretamente (ex.: de 4 para 5, de 4 para 5 e de 3 para 4). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1cjPQn3QQwd7uplj6jeCF9XEYbClfpl2x/view?usp=sharing |

---

### Caso de Teste 03: Tentar cadastrar uma atividade sem preencher os campos

| ID | Descrição |
| --- | --- |
| **C32-CT03** | O sistema deve impedir o cadastro de uma atividade quando os campos do modal "Atividade" estiverem em branco. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Atividades". |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Atividade" |
| **E** não preenche nenhum dos campos (Nome, Pontuação e Descrição) |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o sistema não deve cadastrar a atividade |
| **E** deve indicar a obrigatoriedade do preenchimento dos campos. |

| **Critérios de Aceitação** |
| --- |
| Nenhum registro deve ser criado com os campos em branco. |
| Os indicadores do topo da tela não devem ser alterados. |

| **Observação (comportamento verificado na gravação)** |
| --- |
| Ao clicar em "Salvar" com o modal vazio, o sistema **cadastrou** uma atividade sem nome, sem pontuação e sem descrição (código 6): o "Total de atividades" passou de 5 para 6 e "Sem pontuação" passou de 0 para 1. Nenhuma mensagem de validação foi exibida. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wpRtpZh2PcQYruuJJ6-HUbECbztA2b22/view?usp=sharing |

---

### Caso de Teste 04: Visualizar e editar uma atividade

| ID | Descrição |
| --- | --- |
| **C32-CT04** | O sistema deve permitir a visualização e a atualização das informações de uma atividade existente. |

| **Pré-condições** |
| --- |
| Deve haver ao menos uma atividade cadastrada na listagem (ex.: código 1, "Treinar 5x na semana", com pontuação 10). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de visualizar/editar (lupa) da atividade "Treinar 5x na semana" |
| **E** altera o campo "Pontuação" de "10" para "100" no modal "Atividade" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o modal deve ser fechado |
| **E** a pontuação atualizada deve ser refletida na tabela de atividades. |

| **Critérios de Aceitação** |
| --- |
| As edições realizadas nos campos da atividade devem ser salvas e exibidas imediatamente na listagem. |
| Os indicadores do topo da tela devem permanecer consistentes após a edição. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18XhUQdRLAzJ0N4qyJ3zbueWATgxqklu-/view?usp=sharing |

---

### Caso de Teste 05: Excluir uma atividade

| ID | Descrição |
| --- | --- |
| **C32-CT05** | O sistema deve permitir a exclusão de uma atividade mediante confirmação do usuário. |

| **Pré-condições** |
| --- |
| Deve haver ao menos uma atividade cadastrada na listagem (ex.: código 1, "Treinar 5x na semana"). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a atividade "Treinar 5x na semana" na listagem |
| **QUANDO** clicar no ícone de exclusão (X) na coluna de ações |
| **E** clicar no botão "Confirmar" do modal de confirmação |
| **ENTÃO** a atividade deve ser removida do sistema |
| **E** não deve mais ser exibida na listagem. |

| **Critérios de Aceitação** |
| --- |
| O modal de confirmação deve oferecer as opções "Cancelar" e "Confirmar". |
| Os indicadores do topo devem ser atualizados após a exclusão (ex.: "Total de atividades" de 6 para 5, "Com pontuação" de 5 para 4 e "Com descrição" de 4 para 3). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1lUKhmJLyo0G8_OCx5BnB_W1oNjZcwNCn/view?usp=sharing |
