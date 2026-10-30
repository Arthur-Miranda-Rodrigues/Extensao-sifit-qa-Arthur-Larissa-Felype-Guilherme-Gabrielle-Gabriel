## Cenário 15: Registro de Contas a Pagar

### Caso de Teste 04: Exclusão de Conta a Pagar

| ID | Descrição |
| --- | --- |
| **C15-CT04** | Validar a exclusão de uma conta a pagar na listagem mediante confirmação no modal. |

| **Pré-condições** |
| --- |
| Usuário na tela de listagem de Contas a Pagar com registros visíveis (ex.: #24, #21 e #20 – 3 contas listadas). |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a listagem de contas a pagar |
| **QUANDO** passar o cursor sobre o ícone de lixeira da linha do registro (ex.: #21) |
| **ENTÃO** deve ser exibida a dica "Deletar" |
| **E QUANDO** clicar no ícone de lixeira |
| **ENTÃO** o sistema deve exibir o modal *"Deseja deletar esta conta?"* com os botões **Cancelar** e **Confirmar** |
| **E QUANDO** clicar em **Confirmar** |
| **ENTÃO** a conta deve ser removida da tabela e o indicador "Contas Listadas" deve ser atualizado. |

| **Critérios de aceitação** |
| --- |
| A exclusão só deve ocorrer após a confirmação, e a conta excluída não deve mais aparecer na listagem. |

| **Resultado obtido** |
| --- |
| A conta #21 foi removida e a listagem passou a exibir 2 contas (#24 e #20), com "Contas Listadas" atualizado de 3 para 2. Não ocorreu mensagem de erro no servidor nesta execução. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1a4XPvqhVO9lRqqgFaccGb4HOEwWTnx1S/view?usp=sharing |

---
