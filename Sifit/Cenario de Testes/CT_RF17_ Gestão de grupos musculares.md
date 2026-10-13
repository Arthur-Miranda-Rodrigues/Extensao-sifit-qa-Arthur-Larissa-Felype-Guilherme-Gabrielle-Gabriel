
---

# Cenários:Gestão de Grupos Musculares

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 11 (RF11) - Gestão de Grupos Musculares** do módulo **Treinamento > Grupos Musculares** do sistema **SiFit**. O objetivo é validar o cadastro de novos grupos, a filtragem por múltiplos parâmetros, a edição/inclusão de imagens e o tratamento de integridade referencial em tentativas de exclusão de registros vinculados.

---

## 2. Cenários de Teste

### Cenário 01: Gestão e Operações em Grupos Musculares

#### Caso de Teste 01: Filtragem e Busca de Grupos Musculares

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar o funcionamento dos filtros por Código, Nome e Tipo de Membro na listagem de Grupos Musculares. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Grupos Musculares**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Grupos Musculares** |
| **QUANDO** preencher o campo **Código** com "2" e clicar em **Buscar** |
| **E** limpar o campo **Código**, preencher o campo **Nome** com "Biceps" e clicar em **Buscar** |
| **E** limpar o campo **Nome**, selecionar "Inferiores" no filtro **Tipo Membro** e clicar em **Buscar** |
| **E** alterar o filtro **Tipo Membro** para "Superiores" e clicar em **Buscar** |
| **E** alterar o filtro **Tipo Membro** para "Aerobio" e clicar em **Buscar** |
| **ENTÃO** a tabela deve filtrar e apresentar apenas os registros correspondentes aos parâmetros informados em cada etapa. |

| **Critérios de Aceitação** |
| --- |
| * Apenas registros equivalentes aos filtros aplicados (Código, Nome ou Tipo de Membro) devem ser exibidos na grade. |
| * Ao aplicar filtros sem resultados correspondentes, a listagem deve exibir o indicador de tabela vazia. |

---

#### Caso de Teste 02: Edição de Grupo Muscular Existente com Inclusão de Imagem

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Validar a alteração de dados e atualização do arquivo de imagem de um grupo muscular cadastrado. |

| **Pré-condições** |
| --- |
| Existir ao menos um grupo muscular cadastrado na base de dados (ex.: "Bíceps", Código 1). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de **Grupos Musculares** |
| **E** localiza o registro "Bíceps" (Código 1) |
| **QUANDO** clicar no ícone de edição (lupa) na coluna de ações |
| **E** clicar no botão **Escolher ficheiro** dentro do modal **Grupo Muscular** |
| **E** selecionar um arquivo de imagem válido (ex.: `imagem.png`) |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações do grupo muscular devem ser salvas com sucesso |
| **E** o modal deve ser fechado, retornando à listagem principal com a imagem atualizada. |

| **Critérios de Aceitação** |
| --- |
| * O arquivo de imagem anexado deve persistir no cadastro do grupo muscular. |
| * O formulário deve fechar automaticamente e atualizar a grade sem apresentar erros. |

---

#### Caso de Teste 03: Tentativa de Exclusão de Grupo Muscular Vinculado

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar se o sistema impede a remoção de um grupo muscular que possui vínculos com exercícios ou fichas de treino. |

| **Pré-condições** |
| --- |
| Existir um grupo muscular cadastrado que possua relação/vinculação com outros registros do sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tabela de **Grupos Musculares** |
| **QUANDO** clicar no ícone de exclusão (lixeira) do grupo muscular vinculado |
| **E** confirmar a ação no modal de confirmação (*"Deseja deletar o Grupo?"*) clicando no botão **Confirmar** |
| **ENTÃO** o sistema deve tratar a restrição de integridade referencial |
| **E** exibir um alerta indicando a impossibilidade da exclusão (ex.: *"Erro ao deletar Grupo"*). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir a exclusão de registros que possuam vínculos com exercícios cadastrados. |
| * Uma mensagem de erro informativa deve ser exibida ao usuário, mantendo o registro intacto na base de dados. |

---

#### Caso de Teste 04: Cadastro de Novo Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Validar a inclusão de um novo grupo muscular com preenchimento de Nome, Tipo de Membro e anexo de imagem. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Grupos Musculares**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Grupos Musculares** |
| **E** clica no botão de cadastro (**+**) |
| **QUANDO** preencher o campo **Nome** com "Peitoral" |
| **E** selecionar o **Tipo Membro** como "Superiores" |
| **E** anexar um arquivo de imagem válido |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o novo grupo muscular deve ser cadastrado com sucesso |
| **E** os cards contadores superiores (*Grupos cadastrados* e *Tipo de Membro*) devem atualizar seus totais incrementando +1. |

| **Critérios de Aceitação** |
| --- |
| * O grupo "Peitoral" deve passar a constar na listagem com um código identificador gerado pelo sistema. |
| * Os cards informativos de totalização da tela devem ser recarregados refletindo o novo registro. |


https://jam.dev/c/a8f20df5-1340-4a00-a04c-b8894dd1a2a0
