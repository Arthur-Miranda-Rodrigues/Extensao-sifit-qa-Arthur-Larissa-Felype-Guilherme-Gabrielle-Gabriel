## Cenário 43: Gerenciamento de Categorias de Anamnese no sistema SIFIT

### Caso de Teste 01: Criação de Nova Categoria de Anamnese com Sucesso

| ID | Descrição |
| --- | --- |
| **C43-CT01** | O sistema deve permitir cadastrar uma nova categoria definindo nome, status, ícone e cor visual. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela de **Categorias de Anamnese**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Categorias de Anamnese" |
| **E** clica no botão **+ Nova Categoria**<br> |
| **E** preenche o campo "Nome da Categoria" (ex: "Saúde"), seleciona um ícone (ex: `bi-capsule`) e escolhe uma cor na paleta |
| **QUANDO** clica em **Criar Categoria**<br> |
| **ENTÃO** a nova categoria deve ser gravada e exibida no grid com os parâmetros configurados.|

| **Critérios de Aceitação** |
| --- |
| * A nova categoria deve ser exibida no grid com a barra de pré-visualização na cor selecionada, e os contadores de totais devem ser atualizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1bTePKaWPkGrz-KM5Ifd9D717Wql2HKeJ/view?usp=sharing |

---

### Caso de Teste 02: Validação de Campos Obrigatórios ao Criar Categoria

| ID | Descrição |
| --- | --- |
| **C43-CT02** | O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar uma categoria sem preencher o nome. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal "Nova Categoria" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário mantém o campo "Nome da Categoria" em branco no modal de cadastro |
| **QUANDO** tenta prosseguir e clica em **Criar Categoria**<br> |
| **ENTÃO** o sistema deve bloquear a operação e exibir e validar o preenchimento obrigatório. |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir a gravação de registros incompletos, alertando o usuário sobre a pendência no campo de nome. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1TH9F29TriAYocA0qINtF1lC-ADlKarFT/view?usp=sharing |

---

### Caso de Teste 03: Edição de Categoria Existente

| ID | Descrição |
| --- | --- |
| **C43-CT03** | O sistema deve permitir alterar as informações (como status, nome, ícone ou cor) de uma categoria cadastrada. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos uma categoria cadastrada no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de lápis (Editar) no card da categoria desejada |
| **E** altera o status de "Ativo" para "Inativo" e ajusta a cor ou o ícone |
| **QUANDO** clica no botão **Atualizar**<br> |
| **ENTÃO** as alterações devem ser salvas e refletidas imediatamente no card correspondente. |

| **Critérios de Aceitação** |
| --- |
| * A alteração de status e dados deve atualizar a tag visual do card e reajustar os contadores no cabeçalho. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wGufL84tPgLa68my1udJp_-rRk5Q2ADB/view?usp=sharing |

---

### Caso de Teste 04: Filtragem de Categorias por Status e Busca Dinâmica

| ID | Descrição |
| --- | --- |
| **C43-CT04** | O sistema deve filtrar o grid de categorias conforme o status selecionado (Ativo/Inativo) e permitir a busca por termos no campo de pesquisa. |

| **Pré-condições** |
| --- |
| Devem existir categorias cadastradas na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Categorias de Anamnese**<br> |
| **QUANDO** seleciona um filtro de status (ex: "Inativo") ou digita um termo no campo "Buscar categoria..." |
| **ENTÃO** o sistema deve atualizar dinamicamente a exibição dos cards correspondentes ou retornar a mensagem "Nenhuma categoria encontrada". |

| **Critérios de Aceitação** |
| --- |
| * Os filtros e campos de busca devem responder instantaneamente exibindo apenas os registros compatíveis com o critério aplicado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Bmw_dJJIFgTOqspbcplQn6mQWyOb11jB/view?usp=sharing |

---

### Caso de Teste 05: Exclusão de Categoria de Anamnese com Confirmação

| ID | Descrição |
| --- | --- |
| **C43-CT05** | O sistema deve solicitar confirmação via modal e remover permanentemente uma categoria selecionada. |

| **Pré-condições** |
| --- |
| Deve existir pelo menos uma categoria disponível para exclusão na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a categoria que deseja remover e clica no ícone de lixeira (Excluir) |
| **QUANDO** o modal de confirmação "Excluir a categoria [Nome]?" é exibido e o usuário clica em **Confirmar**<br> |
| **ENTÃO** a categoria deve ser removida do grid e os contadores da página devem ser recalculados. |

| **Critérios de Aceitação** |
| --- |
| * A exclusão deve ocorrer com sucesso após a confirmação explícita do usuário no modal. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1_Vc6ZYeEKZ-Ff3qCkbXedDTJXF7eVxaF/view?usp=sharing |
