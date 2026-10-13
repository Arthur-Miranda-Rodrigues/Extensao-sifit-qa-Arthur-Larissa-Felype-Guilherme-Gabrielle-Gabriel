


---

# Cenário de teste: Gerenciamento de Exercícios

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo **Treinamento > Exercícios** do sistema **SiFit**. O objetivo é validar a gestão da biblioteca de exercícios por grupos musculares, contemplando a criação, edição com upload de mídias, exclusão e a validação de regras de campos obrigatórios.

---

## 2. Cenários de Teste

### Cenário 01: Gestão e Operações na Biblioteca de Exercícios

#### Caso de Teste 01: Visualização e Edição de Exercício Existente

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar a alteração e inclusão de mídias em um exercício cadastrado na biblioteca. |

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit e localizado na tela **Biblioteca de Exercícios**. |
| Existir o grupo muscular "Bíceps" cadastrado contendo ao menos o exercício "AA". |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios** |
| **E** localiza o exercício "AA" dentro do grupo muscular **Bíceps** |
| **QUANDO** clicar no ícone de visualização (lupa) do exercício |
| **E** carregar uma nova imagem para o exercício dentro do modal **Exercício** |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações do exercício devem ser salvas com sucesso |
| **E** o sistema deve retornar à listagem da biblioteca exibindo o registro atualizado. |

| **Critérios de Aceitação** |
| --- |
| * A mídia enviada deve ser vinculada corretamente ao exercício. |
| * O modal deve ser fechado e os dados atualizados sem erros de execução. |

---

#### Caso de Teste 02: Cadastro de Novo Exercício em Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Validar a criação de um novo exercício e sua vinculação a um grupo muscular específico. |

| **Pré-condições** |
| --- |
| Usuário autenticado no SiFit e localizado na tela **Biblioteca de Exercícios**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios** |
| **QUANDO** clicar no botão **+ Adicionar** presente no card do grupo muscular **Bíceps** |
| **E** preencher o campo **Nome** com "Quarken" |
| **E** anexar uma imagem e/ou vídeo demonstrativo no modal **Exercício** |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o novo exercício deve ser cadastrado e exibido no card do grupo muscular correspondente |
| **E** o contador totalizador da biblioteca de exercícios deve ser incrementado em +1. |

| **Critérios de Aceitação** |
| --- |
| * O exercício "Quarken" deve constar na listagem do grupo **Bíceps**. |
| * O contador global da biblioteca deve ser atualizado refletindo o novo quantitativo. |

---

#### Caso de Teste 03: Exclusão de Exercício de um Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar a remoção de um exercício de um grupo muscular. |

| **Pré-condições** |
| --- |
| Existir ao menos um exercício cadastrado no grupo muscular selecionado (ex.: "Quarken" ou "AA"). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Biblioteca de Exercícios** |
| **QUANDO** localizar o exercício desejado no grupo muscular **Bíceps** |
| **E** clicar no ícone de exclusão (**X** em vermelho) ao lado do exercício |
| **E** confirmar a remoção no modal de confirmação (*"Deseja deletar o exercício?"*) clicando em **Confirmar** |
| **ENTÃO** o exercício deve ser removido da listagem do grupo muscular |
| **E** o contador totalizador da biblioteca deve ser decrementado em -1. |

| **Critérios de Aceitação** |
| --- |
| * O registro excluído não deve mais ser exibido na interface. |
| * A contagem total da biblioteca deve ser recalculada imediatamente. |

---

#### Caso de Teste 04: Validação de Campo Obrigatório no Cadastro de Exercício

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Validar a regra de negócio que impede a gravação de exercício sem a inclusão do nome. |

| **Pré-condições** |
| --- |
| Usuário com o modal **Exercício** aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário aciona a opção **+ Adicionar** em um grupo muscular |
| **E** deixa o campo **Nome** em branco |
| **QUANDO** anexar uma imagem ou vídeo demonstrativo |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o sistema deve bloquear a gravação do registro |
| **E** exibir a mensagem de aviso: *"Informe o nome do exercício."*. |

| **Critérios de Aceitação** |
| --- |
| * O cadastro não deve ser efetuado enquanto o campo obrigatório **Nome** não for preenchido. |
| * A mensagem de alerta deve ser clara e visível para o operador. |

https://jam.dev/c/a6ce9380-799e-4fb0-8438-1b430601706d
