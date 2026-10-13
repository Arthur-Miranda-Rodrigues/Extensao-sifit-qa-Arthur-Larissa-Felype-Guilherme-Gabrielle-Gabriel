

---

## Cenário de teste: Gerenciamento de Modelos de Anamnese no sistema SIFIT

### Caso de Teste 01: Criar um novo modelo de anamnese

| ID | Descrição |
| --- | --- |
| C15-CT01 | O sistema deve permitir cadastrar um novo modelo de anamnese definindo nome, descrição e status. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela **Modelos de Anamnese** (Menu Dados > Modelos).

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Modelos de Anamnese"

 |
| **E** clica no botão "Novo Modelo" no canto superior direito

 |
| **E** preenche o campo "Nome do Modelo" (ex: "Triplet")

 |
| **E** preenche o campo "Descrição" (ex: "Triplet")

 |
| **E** mantém o status como "Ativo"

 |
| **QUANDO** clica em "Salvar Modelo"

 |
| **ENTÃO** o sistema redireciona para a listagem e exibe o novo modelo cadastrado no card.

 |

| **Critérios de aceitação** |
| --- |
| O novo modelo deve ser exibido na listagem com o status "Ativo" e atualizar os cards de métricas no topo da página.

 |

---

### Caso de Teste 02: Visualizar preview do modelo e mensagem de modelo sem perguntas

| ID | Descrição |
| --- | --- |
| C15-CT02 | O sistema deve permitir a pré-visualização (preview) do modelo e alertar caso não existam perguntas vinculadas. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos um modelo cadastrado na listagem sem perguntas vinculadas.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de "Modelos de Anamnese"

 |
| **QUANDO** clica na opção "Preview" do card de um modelo sem perguntas (ex: "Esteira")

 |
| **ENTÃO** o sistema exibe um modal com a mensagem "Nenhuma pergunta adicionada ainda".

 |

| **Critérios de aceitação** |
| --- |
| O modal de preview deve ser exibido com o título correspondente ao modelo e permitir o fechamento pelo ícone "X".

 |

---

### Caso de Teste 03: Alterar status do modelo para inativo

| ID | Descrição |
| --- | --- |
| C15-CT03 | O sistema deve permitir a edição do modelo para alterar seu status de "Ativo" para "Inativo". |

| **Pré-condições** |
| --- |
| Deve existir um modelo ativo cadastrado no sistema.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica em "Editar" no card do modelo desejado (ex: "Esteira")

 |
| **E** altera o campo "Status" de "Ativo" para "Inativo"

 |
| **QUANDO** clica no botão "Salvar Modelo"

 |
| **ENTÃO** o sistema exibe o indicador "Salvando..." e redireciona para a listagem

 |
| **E** a tag do modelo é atualizada para a cor vermelha com o texto "Inativo".

 |

| **Critérios de aceitação** |
| --- |
| O status do modelo deve ser atualizado na listagem e o contador de modelos "Ativos" no cabeçalho deve ser decrementado.

 |

---

### Caso de Teste 04: Excluir um modelo de anamnese

| ID | Descrição |
| --- | --- |
| C15-CT04 | O sistema deve solicitar confirmação antes de remover definitivamente um modelo de anamnese. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos um modelo cadastrado na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de "Modelos de Anamnese"

 |
| **E** clica no ícone de lixeira (Excluir) do card do modelo desejado (ex: "Esteira")

 |
| **E** visualiza o modal de confirmação "Excluir o modelo 'Esteira'?"

 |
| **QUANDO** clica no botão "Confirmar"

 |
| **ENTÃO** o modelo é removido da tela e os contadores do topo da página são atualizados.

 |

| **Critérios de aceitação** |
| --- |
| O modelo excluído não deve mais ser exibido na listagem de modelos.

 |

---

### Caso de Teste 05: Adicionar perguntas ao modelo através do Montador Visual

| ID | Descrição |
| --- | --- |
| C15-CT05 | O sistema deve permitir a vinculação de perguntas a um modelo utilizando a estrutura de arrastar ou selecionar no montador visual. |

| **Pré-condições** |
| --- |
| Existirem perguntas cadastradas disponíveis na seção "Perguntas Disponíveis".

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de edição do modelo (ex: "Triplet")

 |
| **E** localiza a pergunta disponível no painel esquerdo "Montador Visual"

 |
| **QUANDO** seleciona a pergunta desejada (ex: "Quantos tipos") para movê-la para o quadro "Modelo Atual"

 |
| **E** marca a caixa de seleção "Obrigatória" (se aplicável)

 |
| **E** clica em "Salvar Modelo"

 |
| **ENTÃO** o modelo é atualizado e o indicador de quantidade de perguntas no card exibe a contagem atualizada.

 |

| **Critérios de aceitação** |
| --- |
| As perguntas vinculadas devem ser salvas no modelo e refletidas no contador "Resumo do Modelo".

 |

 https://jam.dev/c/0183812d-efe0-4616-bafc-3901c2443f77
