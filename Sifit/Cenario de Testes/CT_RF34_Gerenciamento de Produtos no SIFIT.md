## Cenário 34: Gerenciamento de Produtos no SIFIT

### Caso de Teste 01: Filtrar produtos por Código, Nome, Status e Tipo

| ID | Descrição |
| --- | --- |
| **C34-CT01** | O sistema deve permitir filtrar a listagem de produtos por Código, Nome, Status (Ativo/Inativo) e Tipo (Venda/Pontuação). |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela "Produtos", com os produtos "Notebook" (código 4) e "Notebook Gamer" (código 5), ambos do tipo "Venda" e com status "Ativo", cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela "Produtos" |
| **QUANDO** preencher o campo "Nome" com "Notebook" e clicar no botão de busca (lupa) |
| **ENTÃO** os dois produtos correspondentes devem ser exibidos na tabela |
| **E** ao limpar o nome, preencher o campo "Código" com "5" e clicar na lupa |
| **ENTÃO** apenas o produto "Notebook Gamer" deve ser exibido (1 registro) |
| **E** ao limpar o código, selecionar o "Status" como "Ativo" e clicar na lupa |
| **ENTÃO** os produtos ativos devem ser exibidos |
| **E** ao selecionar o "Tipo" como "Venda" e clicar na lupa |
| **ENTÃO** a lista deve exibir os produtos do tipo "Venda" |
| **E** ao selecionar o "Tipo" como "Pontuação" e clicar na lupa |
| **ENTÃO** o sistema deve exibir a mensagem "Nenhum produto encontrado." caso não existam produtos desse tipo. |

| **Critérios de Aceitação** |
| --- |
| A busca deve retornar apenas os dados que atendem aos critérios de filtro configurados. |
| O rodapé da tabela deve refletir a quantidade de registros exibidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1AB4Fu5ji3dbF582L1QsGZf-1guh30d7k/view?usp=sharing |

---

### Caso de Teste 02: Cadastrar novo produto do tipo Pontuação com imagem

| ID | Descrição |
| --- | --- |
| **C34-CT02** | O sistema deve permitir cadastrar um novo produto informando Nome, Descrição, Tipo, Pontuação e Imagem. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela "Produtos" e possuir uma imagem salva no computador para anexar ao produto. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Novo" |
| **E** preenche o campo "Nome" com "Nintendo Switch 2" |
| **E** preenche o campo "Descrição" com "Nintendo Switch 2" |
| **E** seleciona o "Tipo" como "Pontuação" |
| **E** informa o valor no campo "Pontuação" (20000) |
| **E** clica em "Selecione um arquivo" e anexa uma imagem do produto |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** o produto deve ser cadastrado com sucesso |
| **E** exibido na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| O produto cadastrado deve ser exibido na lista com o tipo "Pontuação", o valor "20000 pts" e o status "Ativo". |
| Os indicadores do topo devem ser atualizados (ex.: "Total de produtos" de 2 para 3 e "Ativos" de 2 para 3). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1xr9IxT4HhELbW2eK1YkNUBG2yzHom-XU/view?usp=sharing |

---

### Caso de Teste 03: Editar dados de um produto existente

| ID | Descrição |
| --- | --- |
| **C34-CT03** | O sistema deve permitir a alteração das informações de um produto previamente cadastrado. |

| **Pré-condições** |
| --- |
| Existirem os produtos "Notebook" (código 4, tipo "Venda", preço R$ 1550, status "Ativo") e "Notebook Gamer" (código 5, tipo "Venda") cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de visualizar/editar (lupa) do produto "Notebook" (código 4) |
| **E** altera o campo "Preço" de "1550" para "2000" |
| **E** altera o "Status" de "Ativo" para "Inativo" |
| **QUANDO** clicar no botão "Salvar" |
| **ENTÃO** as alterações devem ser salvas e a tabela deve exibir o preço "R$ 2000" e o status "Inativo" |
| **E** ao editar o produto "Notebook Gamer" (código 5), alterando o "Tipo" de "Venda" para "Pontuação" e informando a pontuação, a tabela deve exibir o produto com o tipo "Pontuação" e o valor em pontos. |

| **Critérios de Aceitação** |
| --- |
| As informações editadas devem ser persistidas e exibidas imediatamente na listagem. |
| Os indicadores do topo devem ser atualizados (ex.: "Ativos" de 3 para 2, "Inativos" de 0 para 1 e "Para venda" de 2 para 1). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1IcgcJBvv8IaSMZNlD0Xc7_TAAkWLqHno/view?usp=sharing |

---

### Caso de Teste 04: Excluir produto com confirmação

| ID | Descrição |
| --- | --- |
| **C34-CT04** | O sistema deve solicitar confirmação antes de remover um produto do cadastro. |

| **Pré-condições** |
| --- |
| Deve existir ao menos um produto cadastrado na tabela (ex.: "Notebook", código 4, status "Inativo"). |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (X) do produto "Notebook" |
| **E** o modal de confirmação "Deseja deletar o produto?" é exibido com as opções "Cancelar" e "Confirmar" |
| **QUANDO** clicar no botão "Confirmar" |
| **ENTÃO** o produto deve ser removido da tabela de produtos |
| **E** os indicadores do topo devem ser atualizados. |

| **Critérios de Aceitação** |
| --- |
| O produto excluído não deve mais aparecer na listagem. |
| Os contadores devem ser atualizados corretamente (ex.: "Total de produtos" de 3 para 2, "Inativos" de 1 para 0 e "Para venda" de 1 para 0). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1K-87lo9yZz52yuALIkIWGuVshobEITz7/view?usp=sharing |

