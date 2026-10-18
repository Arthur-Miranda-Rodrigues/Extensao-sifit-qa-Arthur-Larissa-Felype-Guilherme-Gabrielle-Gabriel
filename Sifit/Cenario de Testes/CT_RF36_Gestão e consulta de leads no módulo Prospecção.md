
---

# Cenário: Gestão e consulta de leads no módulo Prospecção

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo de **Prospecção** do sistema **SiFit**. O objetivo é validar as funcionalidades de pesquisa de leads por nome/termo, filtragem por estágios do funil de vendas, cadastro de novos leads com validação de campos obrigatórios, visualização/edição de dados cadastrados e exclusão de registros na plataforma.

---

## 2. Cenários de Teste

### Caso de Teste 01: Pesquisa de Lead por Nome ou Termo

| ID | Descrição |
| --- | --- |
| **C36-CT01** | O sistema deve permitir a busca e filtragem de leads cadastrados utilizando os campos de texto por nome, e-mail, telefone ou código. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela de **Prospecção**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu de **Prospecção**<br> |
| **QUANDO** preenche o campo de busca com o nome de um lead (ex: "João Ribeiro") e interage com os filtros de estágio |
| **ENTÃO** a tabela deve exibir apenas o registro correspondente aos termos pesquisados. |

| **Critérios de Aceitação** |
| --- |
| * A tabela deve atualizar dinamicamente exibindo o lead pesquisado juntamente com seu código, nome, estágio e data de criação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Y0uAOhtuumczRWYcpSXTZw2kXHLOtHvb/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Novo Lead com Sucesso

| ID | Descrição |
| --- | --- |
| **C36-CT02** | O sistema deve permitir o cadastro bem-sucedido de um novo lead preenchendo os dados pessoais, contato, observação e definindo o estágio inicial. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de **Prospecção** com o modal "Adicionar Lead" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Adicionar Lead**<br> |
| **QUANDO** preenche o nome completo (ex: "Steven Grant"), seleciona o estágio (ex: "Fez Aula Experimental"), insere e-mail, telefone e observações |
| **E** clica no botão **Salvar Lead**<br> |
| **ENTÃO** o novo lead deve ser cadastrado com sucesso e listado na tabela principal de prospecção. |

| **Critérios de Aceitação** |
| --- |
| * O novo lead deve ser gravado e exibido na listagem com os contadores de totais atualizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1pDjrKT7b8ewKjDX9lOdJupsSwrO3HyPg/view?usp=sharing |

---

### Caso de Teste 03: Validação de Campos Obrigatórios ao Cadastrar Lead

| ID | Descrição |
| --- | --- |
| **C36-CT03** | O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar um lead sem preencher o campo de nome. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal "Adicionar Lead" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário mantém o campo de nome em branco no modal de cadastro |
| **QUANDO** clica no botão **Salvar Lead**<br> |
| **ENTÃO** o sistema deve bloquear a operação e exibir mensagens de alerta indicando a pendência (ex: "Preencha este campo"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir a gravação de registros sem as informações obrigatórias. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Ws8nuqkbFox0Zrp4DGhmO-kVRzM7XvNG/view?usp=sharing |

---

### Caso de Teste 04: Visualização e Edição de Dados do Lead

| ID | Descrição |
| --- | --- |
| **C36-CT04** | O sistema deve permitir visualizar os dados de um lead existente, atualizar informações de contato/observações e alterar seu estágio no funil. |

| **Pré-condições** |
| --- |
| Existir um lead cadastrado na tabela de prospecção. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição/visualização (lápis) de um lead na tabela. |
| **QUANDO** altera dados como o e-mail, observações ou estágio do lead no modal correspondente |
| **E** clica em **Salvar Lead**<br> |
| **ENTÃO** as modificações devem ser gravadas e refletidas corretamente na listagem. |

| **Critérios de Aceitação** |
| --- |
| * As alterações de estágio e dados cadastrais do lead devem persistir após o salvamento. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/11wYwP_3tsOY_8VRol8CZIKL6ZX6XYFDm/view?usp=sharing |

---

### Caso de Teste 05: Exclusão de Lead com Confirmação

| ID | Descrição |
| --- | --- |
| **C36-CT05** | O sistema deve solicitar confirmação via modal antes de remover definitivamente um lead cadastrado. |

| **Pré-condições** |
| --- |
| Existir um lead listado na tabela de prospecção. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (lixeira/X) de um lead na tabela |
| **QUANDO** o modal de confirmação "Deseja deletar este lead?" for exibido e o usuário clicar em **Confirmar**<br> |
| **ENTÃO** o registro do lead deve ser permanentemente removido da base de dados e da listagem. |

| **Critérios de Aceitação** |
| --- |
| * O lead selecionado deve ser apagado após a confirmação e os contadores da tela devem ser atualizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1BdsSM66bbzEHasBwxRcNsNDPviYtvFQm/view?usp=sharing |
