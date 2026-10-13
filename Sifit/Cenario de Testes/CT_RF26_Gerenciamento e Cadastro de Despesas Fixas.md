
---

## Cenário de teste: Gerenciamento e Cadastro de Despesas Fixas

### Caso de Teste 01: Cadastrar uma nova despesa fixa com sucesso

| ID | Descrição |
| --- | --- |
| C08-CT01 | O sistema deve permitir o cadastro de uma nova despesa fixa preenchendo todos os campos obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela de "Despesas Fixas" no módulo Financeiro. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Despesa" (ícone `+`)

 |
| **E** preenche o campo "Nome da despesa" (ex.: "Funcionários")

 |
| **E** define o "Status" como "Ativo"

 |
| **E** insere o "Valor" (ex.: "3000,00")

 |
| **E** seleciona a "Recorrência" (ex.: "1 Ano")

 |
| **QUANDO** clicar em "Salvar Despesa"

 |
| **ENTÃO** a despesa deve ser salva e exibida na listagem com o status "ATIVO"

 |

| **Critérios de aceitação** |
| --- |
| A nova despesa deve ser listada corretamente e o valor total somado no card de "Valor Listado" ao buscar pelas despesas ativas. |

---

### Caso de Teste 02: Inativar e excluir uma despesa fixa

| ID | Descrição |
| --- | --- |
| C08-CT02 | O sistema deve permitir alterar o status de uma despesa para "Inativo" e posteriormente realizar a sua exclusão. |

| **Pré-condições** |
| --- |
| Existir ao menos uma despesa fixa previamente cadastrada. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição de uma despesa (ex.: "Teste")

 |
| **E** altera o status de "Ativo" para "Inativo" e clica em "Salvar Despesa"

 |
| **E** filtra as despesas por status "Inativo"

 |
| **QUANDO** clicar no ícone de lixeira e confirmar a remoção no modal "Deseja deletar a despesa fixa?"

 |
| **ENTÃO** a despesa deve ser permanentemente removida da listagem

 |

| **Critérios de aceitação** |
| --- |
| O contador de "Inativas" deve atualizar e a mensagem "Nenhuma despesa fixa encontrada" deve ser exibida quando não houver registros inativos. |

---

### Caso de Teste 03: Filtrar despesas fixas por código, nome e status

| ID | Descrição |
| --- | --- |
| C08-CT03 | O sistema deve filtrar corretamente a listagem de despesas fixas de acordo com os filtros aplicados. |

| **Pré-condições** |
| --- |
| Devem existir despesas ativas e inativas cadastradas com diferentes nomes e códigos. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela de "Despesas Fixas"

 |
| **QUANDO** digita um número no campo "Código" (ex.: "3") ou um texto no campo "Nome da despesa" (ex.: "Teste")

 |
| **E** clica no botão "Buscar" (ícone de lupa)

 |
| **ENTÃO** a tabela deve atualizar e listar apenas as despesas correspondentes aos critérios informados

 |

| **Critérios de aceitação** |
| --- |
| A tabela e o indicador "Valor Listado" devem recalcular e apresentar apenas a soma das despesas resultantes da busca. |

https://jam.dev/c/60a97112-4d54-4458-98dd-bbf6c2031909
