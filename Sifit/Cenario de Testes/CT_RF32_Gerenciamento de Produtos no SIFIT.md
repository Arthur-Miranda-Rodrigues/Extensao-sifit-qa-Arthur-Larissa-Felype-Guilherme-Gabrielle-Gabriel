
---

## Cenário de teste: Gerenciamento de Produtos no SIFIT

### Caso de Teste 01: Filtrar Produtos por Código, Nome, Status e Tipo

| ID | Descrição |
| --- | --- |
| **PROD-CT01** | O sistema deve permitir filtrar a listagem de produtos por Código, Nome, Status (Ativo/Inativo) e Tipo (Venda/Pontuação).

 |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SIFIT e na tela de "Produtos".

 |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela de "Produtos"

 |
| **QUANDO** preencher o campo "Código" com "3" e clicar no botão "Buscar"

 |
| **ENTÃO** apenas o produto com código 3 deve ser exibido

 |
| **E** ao preencher o campo "Nome do produto" com "Notebook" e clicar em "Buscar"

 |
| **ENTÃO** os produtos correspondentes devem ser exibidos na tabela

 |
| **E** ao selecionar o "Status" como "Inativo" e clicar em "Buscar"

 |
| **ENTÃO** a mensagem "Nenhum produto encontrado." deve ser exibida

 |
| **E** ao selecionar o "Tipo" como "Venda" ou "Pontuação" e clicar em "Buscar"

 |
| **ENTÃO** a lista deve ser filtrada conforme o tipo selecionado.

 |

| **Critérios de Aceitação** |
| --- |
| A busca deve aplicar os filtros individualmente ou em conjunto, retornando apenas os dados que atendem aos critérios configurados.

 |

---

### Caso de Teste 02: Cadastrar Novo Produto do Tipo Venda com Imagem

| ID | Descrição |
| --- | --- |
| **PROD-CT02** | O sistema deve permitir cadastrar um novo produto informando Nome, Descrição, Tipo, Preço e Imagem.

 |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de "Produtos".

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "+ Novo"

 |
| **E** preenche o "Nome" como "Notebook Gamer"

 |
| **E** preenche a "Descrição" como "Notebook Gamer"

 |
| **E** seleciona o "Tipo" como "Venda"

 |
| **E** insere o "Preço" como "7000.99"

 |
| **E** clica em "Selecione um arquivo" para anexar uma imagem

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** o produto é cadastrado com sucesso, os contadores superiores são atualizados e o registro aparece na listagem principal.

 |

| **Critérios de Aceitação** |
| --- |
| O produto cadastrado deve ser exibido na lista com o tipo "Venda", o valor formatado em reais (R$ 7000.99) e o status "Ativo".

 |

---

### Caso de Teste 03: Editar Dados de um Produto Existente

| ID | Descrição |
| --- | --- |
| **PROD-CT03** | O sistema deve permitir a alteração das informações de um produto previamente cadastrado.

 |

| **Pré-condições** |
| --- |
| Deve haver ao menos um produto cadastrado na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Editar" (lápis) do produto "Notebook" (código 4)

 |
| **E** altera o valor no campo "Preço" de "1500" para "1550"

 |
| **QUANDO** clicar no botão "Salvar"

 |
| **ENTÃO** as alterações devem ser salvas e a tabela deve refletir o novo valor (R$ 1550).

 |

| **Critérios de Aceitação** |
| --- |
| As informações editadas devem ser persitidas no sistema e atualizadas na visualização da listagem.

 |

---

### Caso de Teste 04: Excluir Produto com Confirmação

| ID | Descrição |
| --- | --- |
| **PROD-CT04** | O sistema deve solicitar confirmação antes de remover um produto do cadastro.

 |

| **Pré-condições** |
| --- |
| Deve existir ao menos um produto cadastrado na tabela.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de "Excluir" (lixeira/X) do produto "Notebook Fitness"

 |
| **E** o modal de confirmação "Deseja deletar o produto?" é exibido

 |
| **QUANDO** clicar no botão "Confirmar"

 |
| **ENTÃO** o produto deve ser removido da tabela de produtos e o totalizador de produtos deve ser decrementado.

 |

 https://jam.dev/c/379e33b4-4a28-400f-a51d-145934dea313

| **Critérios de Aceitação** |
| --- |
| O produto excluído não deve mais aparecer na busca/listagem de produtos e os contadores numéricos devem ser redefinidos corretamente.

 |
