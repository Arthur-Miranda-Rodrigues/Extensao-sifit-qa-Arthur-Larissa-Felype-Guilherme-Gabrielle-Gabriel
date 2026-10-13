

Aqui está a documentação reestruturada e padronizada do **Módulo de Gestão de Categorias Crossfit (RF16 - SIFIT)**, formatada em tabelas com cenários BDD/Gherkin e critérios de aceitação:

---

# Cenario de teste: Gestão de Categorias Crossfit

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 16 (RF16) - Gestão de Categorias Crossfit** do módulo **Treinamento > Categorias Crossfit** do sistema **SiFit**. O objetivo é validar o cadastramento de novas categorias, a alteração de nomes de registros existentes, a filtragem e pesquisa dinâmica por Código e Nome, e a remoção de categorias cadastradas.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Categorias Crossfit

#### Caso de Teste 01: Cadastramento de Nova Categoria de Crossfit

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar a criação e inclusão de uma nova categoria de Crossfit no sistema. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado no menu **Categorias Crossfit**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Categorias Crossfit** |
| **E** clica no botão **+ Nova Categoria** |
| **QUANDO** preencher o campo **Nome** com "BodyBuilder" no modal *Cadastrar Categoria* |
| **E** clicar no botão **Salvar** |
| **ENTÃO** a nova categoria deve ser cadastrada com sucesso |
| **E** o registro deve ser exibido na listagem principal contendo seu código gerado, data de criação e data de atualização. |

| **Critérios de Aceitação** |
| --- |
| * A categoria cadastrada deve ser gravada na base de dados e inserida na grade de exibição. |
| * As colunas de Código, Data de Criação e Data de Atualização devem ser preenchidas automaticamente pelo sistema. |

---

#### Caso de Teste 02: Edição de Categoria de Crossfit

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Verificar a alteração do nome de uma categoria de Crossfit previamente cadastrada. |

| **Pré-condições** |
| --- |
| Existir a categoria "BodyBuilder" cadastrada na listagem de **Categorias Crossfit**. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a categoria "BodyBuilder" na listagem de **Categorias Crossfit** |
| **QUANDO** clicar no ícone de edição (lápis) na coluna **Ações** |
| **E** alterar o campo **Nome** para "BodyBuilder supremo" no modal *Editar Categoria* |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o registro deve ser atualizado na base de dados |
| **E** a tabela deve refletir o novo nome da categoria imediatamente. |

| **Critérios de Aceitação** |
| --- |
| * A alteração do nome deve persistir corretamente no banco de dados. |
| * A listagem principal deve ser recarregada exibindo a nomenclatura atualizada. |

---

#### Caso de Teste 03: Filtragem/Pesquisa de Categorias por Código e Nome

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar o funcionamento dos campos de busca por Código e Nome da Categoria. |

| **Pré-condições** |
| --- |
| Existirem categorias cadastradas na base de dados do sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na página **Categorias Crossfit** |
| **QUANDO** preencher o campo **Código** com "2" e verificar o resultado |
| **E** limpar o campo de código, preencher o campo **Nome** com "E" |
| **E** clicar no botão **Buscar** ou aguardar a filtragem dinâmica |
| **ENTÃO** a tabela deve filtrar e apresentar apenas os registros correspondentes aos parâmetros pesquisados em cada etapa |
| **E** o card indicador de totalização ("Exibidas") deve atualizar sua contagem refletindo o total de registros filtrados. |

| **Critérios de Aceitação** |
| --- |
| * A grade deve apresentar estritamente os registros condizentes com os filtros aplicados. |
| * Os contadores informativos da tela devem acompanhar o número exato de itens exibidos após a busca. |

---

#### Caso de Teste 04: Exclusão de Categoria de Crossfit

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Validar a funcionalidade de remoção de uma categoria de Crossfit do sistema. |

| **Pré-condições** |
| --- |
| Existir a categoria "BodyBuilder supremo" cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a categoria "BodyBuilder supremo" na tabela principal |
| **QUANDO** clicar no ícone de exclusão (lixeira) na coluna **Ações** |
| **E** clicar no botão **Confirmar** dentro do modal de confirmação (*"Deseja deletar esta categoria?"*) |
| **ENTÃO** a categoria deve ser removida da base de dados |
| **E** o sistema deve emitir uma mensagem de confirmação de exclusão e remover o item da tabela principal. |

| **Critérios de Aceitação** |
| --- |
| * O registro selecionado deve ser eliminado do sistema sem causar inconsistências. |
| * A grade de exibição deve ser atualizada imediatamente, ocultando a categoria removida. |

https://jam.dev/c/7cadafc7-b6df-4e3a-9619-7d4f8a5d5082
