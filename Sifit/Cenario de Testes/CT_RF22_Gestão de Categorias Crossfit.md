
---

# Cenario 22: Gestão de Categorias Crossfit

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 22: Gestão de Categorias Crossfit** do módulo **Treinamento > Categorias Crossfit** do sistema **SiFit**. O objetivo é validar as operações de consulta, cadastramentos (comportamento de sucesso e validação de campo obrigatório), alteração de registros e tentativas de exclusão (incluindo o tratamento de erro ao deletar registros vinculados).

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Categorias Crossfit

#### Caso de Teste 01: Pesquisa/Filtro de Categoria por Código

| ID | Descrição |
| --- | --- |
| **C22-CT01** | Validar a filtragem de registros na listagem utilizando o campo de busca por Código. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Categorias Crossfit**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Categorias Crossfit**<br> |
| **QUANDO** preencher o campo **Código** com "3". |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** a tabela deve exibir estritamente o registro correspondente ao código informado. |

| **Critérios de Aceitação** |
| --- |
| * A grade de exibição deve apresentar apenas o item filtrado. |
| * Os contadores informativos da tela devem atualizar a quantidade de registros exibidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/16lg9tcBGW6NV6BcXaGYJcedVArEwAFJP/view?usp=sharing |

---

#### Caso de Teste 02: Cadastramento de Nova Categoria com Sucesso

| ID | Descrição |
| --- | --- |
| **C22-CT02** | Validar o cadastramento bem-sucedido de uma nova categoria preenchendo o campo nome. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página **Categorias Crossfit**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Categorias Crossfit**<br> |
| **E** clica no botão **+ Nova Categoria**<br> |
| **QUANDO** preencher o campo **Nome** com "Cardio 3" no modal *Cadastrar Categoria*<br> |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** o sistema deve cadastrar a nova categoria com sucesso. |
| **E** o registro deve ser inserido na tabela principal. |

| **Critérios de Aceitação** |
| --- |
| * A nova categoria é gravada e exibida na listagem com código e datas gerados automaticamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/13oxtzLloeSxg7Qzmdmfz8Sa0QToKgaTG/view?usp=sharing |

---

#### Caso de Teste 03: Validação de Campo Obrigatório ao Cadastrar Categoria

| ID | Descrição |
| --- | --- |
| **C22-CT03** | Validar a emissão de aviso de campo obrigatório ao tentar salvar uma categoria sem preencher o nome. |

| **Pré-condições** |
| --- |
| Usuário autenticado na página **Categorias Crossfit**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **+ Nova Categoria**<br> |
| **QUANDO** mantiver o campo **Nome** vazio e clicar diretamente em **Salvar**<br> |
| **ENTÃO** o sistema deve exibir um modal de aviso informando "Informe o nome da categoria". |

| **Critérios de Aceitação** |
| --- |
| * O sistema impede o cadastro de registros incompletos e alerta o operador corretamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1gjflekEmKiB7yQKps7yz81mxYv1AV5_R/view?usp=sharing |

---

#### Caso de Teste 04: Visualização da listagem atualizada após cadastro

| ID | Descrição |
| --- | --- |
| **C22-CT04** | Validar a consistência da listagem principal após a inclusão de novas categorias. |

| **Pré-condições** |
| --- |
| Categorias recém-cadastradas presentes na base de dados. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a tela principal de **Categorias Crossfit**<br> |
| **QUANDO** conferir a listagem de registros e cartões indicadores de totais. |
| **ENTÃO** todos os itens cadastrados devem estar listados corretamente com seus respectivos códigos e nomenclaturas.  |

| **Critérios de Aceitação** |
| --- |
| * Os dados exibidos na grade devem refletir fielmente o estado atual do banco de dados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1HubUm6YZfIkTvfrUrw1anDmxViytKyFX/view?usp=sharing |

---

#### Caso de Teste 05: Edição de Registro Existente

| ID | Descrição |
| --- | --- |
| **C22-CT05** | Validar a alteração do nome de uma categoria existente através do modal de edição. |

| **Pré-condições** |
| --- |
| Existir categoria cadastrada na listagem principal. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição (lápis) na coluna **Ações** de um registro. |
| **QUANDO** alterar o campo **Nome** (ex: de "Endurance" para "Endurance 2") no modal *Editar Categoria*<br> |
| **E** clicar em **Salvar**<br> |
| **ENTÃO** a tabela deve refletir o nome atualizado imediatamente. |

| **Critérios de Aceitação** |
| --- |
| * O registro editado deve ser atualizado com sucesso na interface e na base de dados.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ERS3IEYkvz0H25hezw4CRBnT2u3RHY1Y/view?usp=sharing |

---

#### Caso de Teste 06: Tratamento de Erro ao Tentar Deletar Categoria Vinculada

| ID | Descrição |
| --- | --- |
| **C22-CT06** | Validar o tratamento de erro do sistema ao tentar excluir uma categoria que possui dependências/vínculos. |

| **Pré-condições** |
| --- |
| Existir uma categoria vinculada a registros ativos no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (lixeira) em uma categoria. |
| **E** confirma a exclusão no modal de confirmação (*"Deseja deletar esta categoria?"*). |
| **QUANDO** o sistema processar a exclusão. |
| **ENTÃO** deve ser exibida uma mensagem de **Erro** ("Erro ao deletar categoria") por conter restrições de integridade. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve proteger a integridade dos dados impedindo a exclusão indevida e exibindo feedback claro ao usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1HYE66urJUwb8mYBhwgK_9ZK1RUZd_naH/view?usp=sharing |
