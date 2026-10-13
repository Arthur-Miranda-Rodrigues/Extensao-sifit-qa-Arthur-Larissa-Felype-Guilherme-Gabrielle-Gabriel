
---

## Cenário: Gerenciamento de Tipos de Documentos no SIFIT

### Caso de Teste 01: Buscar tipos de documentos por Código ou Nome



| ID | Descrição |
| --- | --- |
| **DOC-CT01** | O sistema deve permitir a filtragem de tipos de documentos por código ou por nome.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela "Tipos de Documentos".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está no menu "Tipos de Documentos"

 |
| **QUANDO** preencher o campo "Código" (ex: "3") e clicar no ícone de busca

 |
| **ENTÃO** o sistema deve listar apenas o tipo de documento correspondente ao código

 |
| **E** ao limpar o código, preencher o campo "Nome do documento" (ex: "vale") e clicar em buscar

 |
| **ENTÃO** o sistema deve filtrar a listagem pelo nome informado.

 |

| **Critérios de aceitação** |
| --- |
| A tabela de registros deve ser atualizada exibindo somente os itens que correspondem aos critérios de busca digitados.

 |

---

### Caso de Teste 02: Cadastrar um novo tipo de documento



| ID | Descrição |
| --- | --- |
| **DOC-CT02** | O sistema deve permitir a criação de um novo tipo de documento definindo seu nome e aplicação.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Tipos de Documentos".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Novo Tipo"

 |
| **E** preenche o campo "Nome" (ex: "Eventos")

 |
| **E** seleciona a "Aplicação" desejada (ex: "Colaborador")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** o novo tipo de documento deve ser gravado e exibido na listagem.

 |

| **Critérios de aceitação** |
| --- |
| O registro deve ser incluído na tabela principal e os contadores de totais por aplicação (ex: Colaborador/Fornecedor) devem ser atualizados.

 |

---

### Caso de Teste 03: Editar e Excluir um tipo de documento



| ID | Descrição |
| --- | --- |
| **DOC-CT03** | O sistema deve permitir alterar a aplicação de um tipo de documento existente e removê-lo do cadastro.

 |

| **Pré-condições** |
| --- |
| Deve existir ao menos um tipo de documento cadastrado na lista.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica na lupa/editar de um registro (ex: item "teste")

 |
| **E** altera o campo "Aplicação" (ex: de "Colaborador" para "Conta / Fornecedor")

 |
| **E** clica em "Salvar"

 |
| **ENTÃO** a alteração deve refletir imediatamente na listagem

 |
| **QUANDO** o usuário clicar no botão de exclusão ("X") de um registro e confirmar a remoção na modal

 |
| **ENTÃO** o item deve ser excluído e removido da listagem.

 |

| **Critérios de aceitação** |
| --- |
| As edições devem ser salvas com sucesso e a exclusão confirmada deve decrementar o total de registros listados na tela.

 |

https://jam.dev/c/7dda0042-47b2-496a-b614-7b3bde126852
