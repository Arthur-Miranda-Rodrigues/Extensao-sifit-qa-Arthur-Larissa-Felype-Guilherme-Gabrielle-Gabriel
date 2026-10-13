
---

## Cenário: Gerenciamento de Fornecedores no SIFIT

### Caso de Teste 01: Buscar fornecedores por Código ou Nome



| ID | Descrição |
| --- | --- |
| **FOR-CT01** | O sistema deve permitir a busca de fornecedores cadastrados utilizando o código ou o nome.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e na tela de "Fornecedores".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está no menu de "Fornecedores"

 |
| **QUANDO** preencher o campo "Código" (ex: "215") e clicar em "Buscar"

 |
| **ENTÃO** o sistema deve listar apenas o fornecedor correspondente

 |
| **E** ao limpar o código, preencher o campo "Nome" (ex: "Equipamentos Polmet") e clicar em "Buscar"

 |
| **ENTÃO** o sistema deve filtrar a listagem pelo nome informado.

 |

| **Critérios de aceitação** |
| --- |
| A tabela de fornecedores deve atualizar exibindo apenas os registros que satisfaçam os filtros informados.

 |

---

### Caso de Teste 02: Cadastrar um novo fornecedor com dados válidos



| ID | Descrição |
| --- | --- |
| **FOR-CT02** | O sistema deve permitir o cadastro de um novo fornecedor via modal "Novo Fornecedor".

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de "Fornecedores".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Novo Fornecedor"

 |
| **E** preenche o campo "Nome do fornecedor" (ex: "Jeremias Castro")

 |
| **E** preenche os dados de CNPJ, Telefones, E-mail e Endereço completo

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** o novo fornecedor deve ser adicionado e exibido na lista principal.

 |

| **Critérios de aceitação** |
| --- |
| O fornecedor criado deve aparecer na listagem geral com o status "ATIVO" e o contador de fornecedores deve ser incrementado.

 |

---

### Caso de Teste 03: Visualizar, editar e tentar deletar um fornecedor



| ID | Descrição |
| --- | --- |
| **FOR-CT03** | O sistema deve permitir a visualização, edição de dados e a solicitação de exclusão de um fornecedor.

 |

| **Pré-condições** |
| --- |
| Deve haver fornecedores já cadastrados na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Visualizar/Editar" de um fornecedor na lista

 |
| **E** altera um dado (ex: altera o número do endereço de "5050" para "5052")

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** as alterações devem ser gravadas

 |
| **E** ao clicar no ícone de "Excluir" (X) do registro e confirmar a ação na modal

 |
| **ENTÃO** o sistema deve processar a solicitação ou retornar a mensagem de validação do servidor.

 |

| **Critérios de aceitação** |
| --- |
| Os dados alterados devem permanecer salvos no cadastro do fornecedor e a tentativa de exclusão deve acionar a confirmação.

 |

 https://jam.dev/c/7665800f-fc1f-4d0f-90f1-d9c24924f244
