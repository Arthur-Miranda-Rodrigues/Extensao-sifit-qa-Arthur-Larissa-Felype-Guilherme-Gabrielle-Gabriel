## Cenário 15: Registro de Contas a Pagar

### Caso de Teste 03: Visualização Detalhada da Conta a Pagar

| ID | Descrição |
| --- | --- |
| **C15-CT03** | Confirmar se os dados do registro são apresentados de forma íntegra no modal **Visualizar Conta a Pagar**. |

| **Pré-condições** |
| --- |
| Existir pelo menos uma conta cadastrada e visível na tabela principal (ex.: #21 – Centrion Web – testes22). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a conta na listagem de Contas a Pagar |
| **QUANDO** clicar no ícone de visualização (lupa) na linha do registro |
| **ENTÃO** o sistema deve abrir o modal **Visualizar Conta a Pagar** com o status (PENDENTE) e as seções *Informações Gerais* (funcionário cadastrante, data de lançamento, tipo e tipo de despesa), *Dados da Conta* (código, título, valor a pagar e vencimento), *Dados Fornecedor* (código 205 e nome Centrion Web), *Documento* (tipo, doc. fornecedor, data de emissão e categoria) e *Observação* |
| **E QUANDO** clicar em **Fechar** |
| **ENTÃO** o modal deve ser fechado e o usuário deve retornar à listagem. |

| **Critérios de aceitação** |
| --- |
| O modal de visualização deve carregar todas as informações da conta selecionada de maneira legível e correta. |

| **Resultado obtido** |
| --- |
| O modal foi exibido com todas as seções (Título "testes22", R$ 170,00, Fornecedor 205 – Centrion Web, Observação "ttt") e fechou normalmente. **Observações de apresentação:** o *Tipo* aparece como "DESPESA_FORNECEDOR" e o tipo de despesa como "variavel"; a data de emissão aparece no formato "2025-10-01"; a *Categoria* aparece como o número "13" e o *Tipo* do documento como "1"; os campos *Código* e *Doc. Fornecedor* estão vazios; e os rótulos "Informacoes" e "Observacao" estão sem acentuação. |


| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KiWx9QYxlleZDS9Ns09cYcaOk2zXi1lg/view?usp=sharing |

---

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
