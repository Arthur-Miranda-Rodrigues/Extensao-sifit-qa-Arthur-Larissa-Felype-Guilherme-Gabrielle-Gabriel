## Cenário 18: Gestão de Grupos Musculares
---

## 2. Cenários de Teste

### Cenário 01: Gestão e Operações em Grupos Musculares

#### Caso de Teste 01: Filtragem e Busca de Grupos Musculares

| ID | Descrição |
| --- | --- |
| **C18-CT01** | Validar o funcionamento dos filtros por Código, Nome e Tipo Membro na listagem de Grupos Musculares, e a limpeza dos filtros. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Grupos Musculares**, com grupos cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Grupos Musculares** |
| **QUANDO** preencher o campo **Nome** com "Teste" e clicar em **Buscar** |
| **E** limpar o campo **Nome**, preencher o campo **Código** com "2" e clicar em **Buscar** |
| **E** limpar o campo **Código**, selecionar "Inferiores" no filtro **Tipo Membro** (opções: Todos, Inferiores, Superiores e Aeróbio) e clicar em **Buscar** |
| **E** alterar o filtro **Tipo Membro** para "Superiores" e clicar em **Buscar** |
| **E** alterar o filtro **Tipo Membro** para "Aeróbio" e clicar em **Buscar** |
| **E** clicar no botão de atualizar ao lado de **Buscar** |
| **ENTÃO** a tabela deve filtrar e apresentar apenas os registros correspondentes aos parâmetros informados em cada etapa |
| **E** ao final, os filtros devem voltar ao estado padrão com a listagem completa. |

| **Critérios de Aceitação** |
| --- |
| * Apenas registros equivalentes aos filtros aplicados (Código, Nome ou Tipo Membro) devem ser exibidos na grade. |
| * O botão de atualizar deve limpar os filtros e recarregar a listagem completa. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18GGFhiaoM5HLyuODyVbJLLGf01IEtNUU/view?usp=sharing |

---

#### Caso de Teste 02: Cadastro de Novo Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C18-CT02** | Validar a inclusão de um novo grupo muscular com preenchimento de Nome, Tipo Membro e anexo de imagem. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Grupos Musculares**. |
| Possuir um arquivo de imagem válido (ex.: `musculos-abdominais.jpg`). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Grupos Musculares** |
| **E** clica no botão de cadastro (**+**), abrindo o modal **Grupo Muscular** |
| **QUANDO** preencher o campo **Nome** com "Abdomen" |
| **E** clicar em **Escolher arquivo** e selecionar a imagem `musculos-abdominais.jpg` |
| **E** selecionar o **Tipo Membro** como "Inferiores" |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o novo grupo muscular deve ser cadastrado com sucesso |
| **E** os cards contadores superiores (*Grupos cadastrados* e o card do tipo de membro correspondente) devem ser atualizados com +1. |

| **Critérios de Aceitação** |
| --- |
| * O grupo "Abdomen" deve constar na listagem com código gerado pelo sistema. |
| * O modal deve ser fechado após salvar e a imagem selecionada deve ser exibida na pré-visualização antes do salvamento. |
| * Os cards de totalização devem refletir o novo registro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1aadWeVRhsgmdTwvEp28jVLcEagmaiUza/view?usp=sharing |

---

#### Caso de Teste 03: Edição de Grupo Muscular com Troca de Imagem

| ID | Descrição |
| --- | --- |
| **C18-CT03** | Validar a alteração do nome e da imagem de um grupo muscular já cadastrado. |

| **Pré-condições** |
| --- |
| Existir ao menos um grupo muscular cadastrado (ex.: código 5, "Teste", Superiores). |
| Possuir um arquivo de imagem válido (ex.: `Haroldx Canio e Garthon Kamidala.png`). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de **Grupos Musculares** |
| **E** localiza o registro de código 5 ("Teste") |
| **QUANDO** clicar no ícone de edição (lupa) na coluna de ações |
| **E** clicar em **Escolher arquivo** e selecionar uma nova imagem |
| **E** alterar o campo **Nome** de "Teste" para "Teste 2" |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações devem ser salvas com sucesso |
| **E** o modal deve ser fechado, retornando à listagem com o nome e a imagem atualizados. |

| **Critérios de Aceitação** |
| --- |
| * O novo nome e a nova imagem devem persistir no cadastro do grupo muscular. |
| * O modal deve fechar automaticamente e a grade deve ser atualizada sem erros. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tZ5BNi8Pz_ZD4UT4F-Hn7OPSPHimAzdv/view?usp=sharing |

---

#### Caso de Teste 04: Cadastro de Grupo Muscular Sem Preencher Nome e Tipo Membro

| ID | Descrição |
| --- | --- |
| **C18-CT04** | Validar o tratamento de campos obrigatórios ao cadastrar um grupo muscular informando apenas a imagem. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Grupos Musculares**. |
| Possuir um arquivo de imagem válido (ex.: `Haroldx Canio e Garthon Kamidala.png`). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Grupos Musculares** |
| **E** clica no botão de cadastro (**+**), abrindo o modal **Grupo Muscular** |
| **QUANDO** selecionar apenas a imagem, deixando **Nome** e **Tipo Membro** vazios |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o sistema não deve permitir o cadastro |
| **E** deve informar que os campos **Nome** e **Tipo Membro** são obrigatórios. |
| **ENTÃO** o sistema cadastra mesmo sem preenchimento obrigatório devido a um bug |

| **Critérios de Aceitação** |
| --- |
| * Nenhum grupo muscular deve ser cadastrado sem **Nome** e **Tipo Membro**. |
| * O sistema deve exibir mensagem informando os campos que precisam ser preenchidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/16umD_rrlyjFLRKMBB-g0nF2_dc9_e5V8/view?usp=sharing |

---

#### Caso de Teste 05: Exclusão de Grupo Muscular

| ID | Descrição |
| --- | --- |
| **C18-CT05** | Validar a exclusão de um grupo muscular pela listagem, com confirmação. |

| **Pré-condições** |
| --- |
| Existir um grupo muscular sem vínculos com outros registros (ex.: código 6, "TEsteSS", Inferiores). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tabela de **Grupos Musculares** |
| **QUANDO** clicar no ícone de exclusão (lixeira) do grupo desejado |
| **E** clicar em **Confirmar** no modal *"Deseja deletar o Grupo?"* |
| **ENTÃO** o grupo muscular deve ser removido da listagem |
| **E** o card contador **Grupos cadastrados** deve ser recalculado. |

| **Critérios de Aceitação** |
| --- |
| * O grupo excluído não deve mais constar na listagem. |
| * Os totais da tela devem refletir a exclusão. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Yrix5ncRoEkit0YJjK34JzC3D4p4adqd/view?usp=sharing |
