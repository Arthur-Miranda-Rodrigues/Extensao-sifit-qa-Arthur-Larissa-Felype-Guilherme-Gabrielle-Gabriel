
---

# Cenário de Testes: Registro de Contas a Pagar (RF08)

**Descrição:** Validação do módulo de Contas a Pagar na plataforma SIFIT, englobando o cadastro de novas despesas, pesquisa e consulta de fornecedores no modal, aplicação de filtros e busca avançada na listagem, visualização detalhada do registro e tratamento de exceções/erros de servidor no fluxo de exclusão.

---

## Caso de Teste 01: Cadastro de Conta a Pagar com Dados Válidos

| ID | Descrição |
| --- | --- |
| RF08-CT01 | Verificar se o sistema permite registrar uma nova conta a pagar preenchendo os campos obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na página de "Contas a Pagar". |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o módulo de "Contas a Pagar"<br>

<br>

<br>**E** clica no botão "+ Nova Conta"<br>

<br>

<br>**E** preenche os campos obrigatórios (Título, Valor a Pagar, Data de Emissão, Categoria e Tipo de Despesa)<br>

<br>

<br>**QUANDO** clicar no botão "Salvar"<br>

<br>

<br>**ENTÃO** a conta deve ser gravada com sucesso e exibida na listagem de Contas a Pagar com o estado "PENDENTE". |

| **Critérios de aceitação** |
| --- |
| A conta a pagar cadastrada deve ser adicionada e exibida corretamente na tabela de listagem principal. |

---

## Caso de Teste 02: Pesquisa de Fornecedor no Cadastro de Conta

| ID | Descrição |
| --- | --- |
| RF08-CT02 | Validar a funcionalidade de busca/modal de fornecedor ao registrar uma conta. |

| **Pré-condições** |
| --- |
| Estar no formulário de "Cadastrar Conta a Pagar". |

| **Passos** |
| --- |
| **DADO** que o usuário está no formulário de "Cadastrar Conta a Pagar"<br>

<br>

<br>**E** clica no botão "Pesquisar" ao lado do campo "Fornecedor"<br>

<br>

<br>**E** introduz o nome do fornecedor (ex: "Marcelo") no campo de busca do modal<br>

<br>

<br>**QUANDO** clicar no botão "Buscar"<br>

<br>

<br>**ENTÃO** o sistema deve consultar a base de dados e retornar os fornecedores correspondentes à pesquisa ou indicar ausência de resultados. |

| **Critérios de aceitação** |
| --- |
| O modal de pesquisa deve filtrar corretamente os fornecedores cadastrados conforme o parâmetro digitado. |

---

## Caso de Teste 03: Filtro e Consulta na Tabela de Contas a Pagar

| ID | Descrição |
| --- | --- |
| RF08-CT03 | Verificar o funcionamento dos filtros por Nome/Título, Código e Tipo de Data na listagem. |

| **Pré-condições** |
| --- |
| Existirem registros de contas a pagar previamente cadastrados na base de dados. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de listagem de Contas a Pagar<br>

<br>

<br>**QUANDO** filtrar pelo Nome/Título da conta e clicar em "Buscar"<br>

<br>

<br>**E** limpar os campos e filtrar por um Código específico (ex: #23)<br>

<br>

<br>**E** alterar o parâmetro do filtro "Tipo de Data" de "Vencimento" para "Pagamento"<br>

<br>

<br>**ENTÃO** a tabela deve atualizar exibindo exclusivamente os registros que cumprem os critérios informados. |

| **Critérios de aceitação** |
| --- |
| Os filtros combinados de título, código e tipo de data devem atualizar e exibir com precisão os registros na tabela. |

---

## Caso de Teste 04: Visualização dos Detalhes da Conta

| ID | Descrição |
| --- | --- |
| RF08-CT04 | Confirmar se os dados do registro são apresentados corretamente no modal de visualização. |

| **Pré-condições** |
| --- |
| Existir pelo menos uma conta cadastrada e visível na tabela principal. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza uma conta na listagem<br>

<br>

<br>**QUANDO** clicar no ícone de visualização (lupa) na linha do registro desejado<br>

<br>

<br>**ENTÃO** o sistema deve abrir um modal apresentando detalhadamente as seções "Informações Gerais", "Dados da Conta", "Dados do Fornecedor" e "Documento". |

| **Critérios de aceitação** |
| --- |
| O modal deve exibir integralmente todos os campos e informações vinculados ao registro selecionado. |

---

## Caso de Teste 05: Exclusão de Conta a Pagar (Tratamento de Erro no Servidor / Bug)

| ID | Descrição |
| --- | --- |
| RF08-CT05 | Verificar o comportamento do sistema ao tentar eliminar uma conta a pagar e validar o tratamento de erros. |

| **Pré-condições** |
| --- |
| Existir uma conta a pagar cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a listagem de contas a pagar<br>

<br>

<br>**E** clica no ícone de exclusão (lixeira) na linha do registro<br>

<br>

<br>**QUANDO** confirmar a ação na mensagem de confirmação ("Deseja deletar esta conta?") clicando em "Confirmar"<br>

<br>

<br>**ENTÃO** o sistema deve remover o registro da base de dados ou tratar a falha exibindo o alerta de erro: "Erro no servidor - Erro interno inesperado.". |

| **Critérios de aceitação** |
| --- |
| O registro deve ser removido com sucesso do banco de dados ou, na ocorrência de erro interno (HTTP 500), notificar amigavelmente o usuário via modal de alerta. |


https://jam.dev/c/a50b1c50-42ac-4b0d-84eb-9328bb0377d6
