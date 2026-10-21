---

## Cenário 17: Gerenciamento de Exercícios
---

## 2. Cenários de Teste

### Caso de Teste 01: Cadastro de Novo Exercício em Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C17-CT01** | Validar a criação de um novo exercício e sua vinculação a um grupo muscular específico preenchendo o nome e anexando imagens e vídeos demonstrativos. |

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit e localizado na tela **Biblioteca de Exercícios**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios**<br> |
| **QUANDO** clicar no botão **+ Adicionar** presente no card do grupo muscular (ex.: **Bíceps**). |
| **E** preencher o campo **Nome** com o nome do exercício (ex.: "Levantamento de Peso"). |
| **E** anexar arquivos de imagem e/ou vídeo demonstrativo nos campos correspondentes do modal **Exercício**<br> |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** o novo exercício deve ser cadastrado com sucesso, exibido no card do grupo muscular correspondente e o contador totalizador da biblioteca deve ser incrementado. |

| **Critérios de Aceitação** |
| --- |
| * O exercício criado deve constar na listagem do grupo muscular correspondente com as mídias anexadas. |
| * O contador global da biblioteca deve ser atualizado refletindo o novo quantitativo. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/17emQxlJzdQ4Ntaf7m2afq0UqcGlHXond/view?usp=sharing |

---

### Caso de Teste 02: Edição e Atualização de Exercício Existente

| ID | Descrição |
| --- | --- |
| **C17-CT02** | Validar a visualização e alteração de um exercício já cadastrado na biblioteca, atualizando seu nome ou dados complementares.

 |

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit e localizado na tela **Biblioteca de Exercícios**. |
| Existir um exercício pré-cadastrado em um grupo muscular (ex.: exercício no grupo *Bíceps*). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios**<br> |
| **QUANDO** clicar no ícone de visualização/edição (lupa) de um exercício existente. |
| **E** modificar os dados desejados no modal **Exercício** (ex.: atualizar o nome para "Quarkan 3"). |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** as alterações do exercício devem ser salvas com sucesso e refletidas na listagem da biblioteca. |

| **Critérios de Aceitação** |
| --- |
| * O registro editado deve ser atualizado corretamente na interface sem perda de dados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1bQpemhSgO8mhlHThOD1ZL52CcTKmYuBM/view?usp=sharing |

---

### Caso de Teste 03: Exclusão de Exercício de um Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar a remoção de um exercício vinculado a um grupo muscular por meio do botão de exclusão e confirmação no modal. |

| **Pré-condições** |
| --- |
| Existir ao menos um exercício cadastrado no grupo muscular selecionado. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios**<br> |
| **QUANDO** localizar o exercício desejado no grupo muscular. |
| **E** clicar no ícone de exclusão (**X**) ao lado do exercício. |
| **E** confirmar a remoção no modal de confirmação (*"Deseja deletar o exercício?"*) clicando em **Confirmar**<br> |
| **ENTÃO** o exercício deve ser removido da listagem do grupo muscular e o contador totalizador da biblioteca deve ser decrementado. |

| **Critérios de Aceitação** |
| --- |
| * O registro excluído não deve mais ser exibido na interface do grupo muscular. |
| * A contagem total da biblioteca deve ser recalculada imediatamente após a confirmação.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1bQpemhSgO8mhlHThOD1ZL52CcTKmYuBM/view?usp=sharing |
