
---

# Cenário 42: Gerenciamento de Modelos de Anamnese no Sistema SIFIT

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 42: Gerenciamento de Modelos de Anamnese** no sistema **SiFit**. O objetivo é validar as operações de criação de novos modelos de anamnese, pré-visualização (preview) de fichas sem perguntas, alteração de status (ativo/inativo), exclusão de modelos com confirmação e vinculação de perguntas por meio do montador visual com marcação de obrigatoriedade.

---

## 2. Cenários de Teste

### Caso de Teste 01: Exclusão de Modelo de Anamnese com Confirmação

| ID | Descrição |
| --- | --- |
| **C42-CT01** | Validar a exibição do modal de confirmação de exclusão e a remoção definitiva de um modelo de anamnese do sistema. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e posicionado na tela **Modelos de Anamnese** com registros cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a listagem de modelos de anamnese<br> |
| **QUANDO** clica no ícone de lixeira (Excluir) em um dos cards (ex.: "Triplet 3") |
| **E** visualiza o modal de confirmação "Excluir o modelo 'Triplet 3'?" e clica em **"Confirmar"**<br><br> |
| **ENTÃO** o modelo deve ser removido da tela e os contadores do topo da página devem ser atualizados. |

| **Critérios de Aceitação** |
| --- |
| * O modal de confirmação deve ser exibido adequadamente e o registro deve deixar de existir na listagem após a confirmação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/13JHjQP5yygz_8tH9SlZ62w5SorWPnPKn/view?usp=sharing |

---

### Caso de Teste 02: Edição e Alteração de Status do Modelo para Inativo

| ID | Descrição |
| --- | --- |
| **C42-CT02** | Validar a alteração do status de um modelo de anamnese de "Ativo" para "Inativo" através da tela de edição. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de listagem de modelos com pelo menos um registro cadastrado. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"Editar"** no card de um modelo desejado<br> |
| **QUANDO** altera o campo **"Status"** de "Ativo" para "Inativo" e clica no botão **"Salvar Modelo"**<br><br> |
| **ENTÃO** o sistema exibe o indicador "Salvando...", redireciona para a listagem e atualiza a tag do modelo para a cor vermelha com o texto "Inativo". |

| **Critérios de Aceitação** |
| --- |
| * O status alterado deve refletir na listagem e os contadores de ativos/inativos no cabeçalho devem ser recalculados corretamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1zzEM7M0NkQRlWdWZmBa3CKeSvjCaqWtf/view?usp=sharing |

---

### Caso de Teste 03: Filtragem de Modelos de Anamnese por Status

| ID | Descrição |
| --- | --- |
| **C42-CT03** | Validar a filtragem dos modelos de anamnese na listagem principal utilizando o seletor de status (Ativo, Inativo ou Todos). |

| **Pré-condições** |
| --- |
| O usuário estar na página principal de **Modelos de Anamnese**. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza os modelos cadastrados e os cards de métricas no topo<br> |
| **QUANDO** clica no filtro de status (alternando entre "Todos os status", "Ativo" e "Inativo") e realiza buscas textuais<br> |
| **ENTÃO** a listagem de modelos deve atualizar dinamicamente para exibir apenas os registros que correspondem ao filtro selecionado. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve filtrar com precisão os modelos de acordo com o status escolhido na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tq9wVmTqXbINtKu-6LU2LsI6jPtXv8tZ/view?usp=sharing |

---

### Caso de Teste 04: Cadastro de Novo Modelo de Anamnese

| ID | Descrição |
| --- | --- |
| **C42-CT04** | Validar o fluxo de cadastro de um novo modelo de anamnese preenchendo as informações gerais e definindo seu status inicial. |

| **Pré-condições** |
| --- |
| O usuário estar na tela principal de **Modelos de Anamnese**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"Novo Modelo"** no canto superior direito<br> |
| **QUANDO** preenche os campos "Nome do Modelo" e "Descrição" |
| **E** clica no botão **"Salvar Modelo"**<br><br> |
| **ENTÃO** o novo modelo deve ser gravado com sucesso e exibido na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * O novo modelo deve ser incluído na tabela/cards com os dados fornecidos e atualizar os totalizadores da tela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1TMSIq8VsB8ukO8-bXjVjPBM68oeVQc4F/view?usp=sharing |

---

### Caso de Teste 05: Vinculação de Perguntas e Configuração de Obrigatoriedade no Montador Visual

| ID | Descrição |
| --- | --- |
| **C42-CT05** | Validar a seleção e adição de perguntas ao modelo através do montador visual, incluindo a marcação de campos obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de criação ou edição de um modelo de anamnese contendo perguntas disponíveis no painel esquerdo. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza as perguntas disponíveis no painel esquerdo do montador visual<br> |
| **QUANDO** seleciona as perguntas desejadas para compor o "Modelo Atual" |
| **E** marca a opção **"Obrigatória"** nas perguntas selecionadas conforme a regra de negócio |
| **E** clica em **"Salvar Modelo"**<br><br> |
| **ENTÃO** o modelo deve ser atualizado salvando as perguntas vinculadas e refletindo a contagem no resumo lateral. |

| **Critérios de Aceitação** |
| --- |
| * As perguntas devem ser associadas corretamente ao modelo e os indicadores de obrigatoriedade devem ser persistidos sem falhas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DMR446oaawDMBouwS94V487PNOviNyG0/view?usp=sharing |
