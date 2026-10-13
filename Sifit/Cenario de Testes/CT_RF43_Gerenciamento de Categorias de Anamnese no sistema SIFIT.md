
---

## Cenário de teste: Gerenciamento de Categorias de Anamnese no sistema SIFIT

### Caso de Teste 01: Criar uma nova categoria de anamnese

| ID | Descrição |
| --- | --- |
| C16-CT01 | O sistema deve permitir cadastrar uma nova categoria definindo nome, status, ícone e cor visual. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela **Categorias de Anamnese**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Categorias de Anamnese"

 |
| **E** clica no botão "+ Nova Categoria"

 |
| **E** preenche o campo "Nome da Categoria" (ex: "Alimentação")

 |
| **E** seleciona um ícone da lista (ex: `bi-apple`)

 |
| **E** escolhe uma cor na paleta disponível

 |
| **QUANDO** clica em "Criar Categoria"

 |
| **ENTÃO** o sistema exibe a animação "Salvando..."

 |
| **E** a nova categoria é adicionada à listagem exibindo o ícone e a cor configurados.

 |

| **Critérios de aceitação** |
| --- |
| A nova categoria deve ser exibida no grid com a barra de pré-visualização na cor selecionada, e os contadores do topo da página devem ser incrementados.

 |

---

### Caso de Teste 02: Editar uma categoria existente

| ID | Descrição |
| --- | --- |
| C16-CT02 | O sistema deve permitir alterar as informações (nome, status, ícone ou cor) de uma categoria cadastrada. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos uma categoria cadastrada no sistema.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de lápis (Editar) no card da categoria desejada

 |
| **E** altera o status de "Ativo" para "Inativo" (ou altera o ícone/cor)

 |
| **QUANDO** clica no botão "Atualizar"

 |
| **ENTÃO** as alterações são salvas e refletidas no card da categoria.

 |

| **Critérios de aceitação** |
| --- |
| A alteração de status deve atualizar a tag visual do card (ex: "Inativo" em vermelho) e reajustar os contadores "Ativas" e "Inativas" no cabeçalho.

 |

---

### Caso de Teste 03: Filtrar categorias por status

| ID | Descrição |
| --- | --- |
| C16-CT03 | O sistema deve filtrar o grid de categorias de acordo com o status selecionado no menu suspenso. |

| **Pré-condições** |
| --- |
| Devem existir categorias ativas e inativas cadastradas.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de "Categorias de Anamnese"

 |
| **QUANDO** altera o filtro "Todos os status" no canto superior direito para "Ativo"

 |
| **ENTÃO** o sistema exibe apenas as categorias com status ativo

 |
| **QUANDO** altera o filtro para "Inativo"

 |
| **ENTÃO** o sistema exibe apenas as categorias com status inativo.

 |

| **Critérios de aceitação** |
| --- |
| Caso não existam categorias correspondentes ao filtro selecionado, o sistema deve exibir a mensagem padrão "Nenhuma categoria encontrada".

 |

---

### Caso de Teste 04: Excluir uma categoria de anamnese

| ID | Descrição |
| --- | --- |
| C16-CT04 | O sistema deve permitir excluir uma categoria mediante confirmação do usuário. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos uma categoria disponível para exclusão.

 |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a categoria que deseja remover

 |
| **E** clica no ícone de lixeira (Excluir)

 |
| **E** visualiza o modal de confirmação "Excluir a categoria 'Nome'?"

 |
| **QUANDO** clica no botão "Confirmar"

 |
| **ENTÃO** a categoria é removida e a listagem é atualizada.

 |

| **Critérios de aceitação** |
| --- |
| A categoria excluída não deve mais aparecer no grid e os indicadores de total de categorias devem ser recalculados.

 |

---

### Caso de Teste 05: Buscar categoria por nome

| ID | Descrição |
| --- | --- |
| C16-CT05 | O sistema deve filtrar em tempo real as categorias conforme o termo digitado no campo de busca. |

| **Pré-condições** |
| --- |
| Devem existir múltiplas categorias cadastradas na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Categorias de Anamnese"

 |
| **QUANDO** digita o nome de uma categoria (ex: "ene" ou "ali") no campo "Buscar categoria..."

 |
| **ENTÃO** o sistema oculta as categorias divergentes e mantém visíveis apenas os cards que contêm o termo buscado.

 |

| **Critérios de aceitação** |
| --- |
| O filtro deve funcionar de forma dinâmica conforme a digitação do usuário no campo de busca.

 |

 https://jam.dev/c/1af2ebf7-99df-4d1f-88fe-32da7ce2ecea
