
---

## Cenário de teste: Gestão de Modelos de Contrato no sistema SIFIT

### Caso de Teste 01: Acessar formulário de criação de modelo de contrato

| ID | Descrição |
| --- | --- |
| C11-CT01 | O sistema deve redirecionar o usuário para a tela de adição ao clicar no botão de novo modelo. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema e na página de **Modelos Contrato**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Modelos Contrato"

 |
| **QUANDO** clica no botão "Adicionar Modelo Contrato"

 |
| **ENTÃO** o sistema deve carregar a página "Modelos de Contrato > Adicionar" com os campos de título, editor de texto, pré-visualização e painel de variáveis disponíveis.

 |

| **Critérios de aceitação** |
| --- |
| A tela deve exibir todos os componentes necessários para a criação do modelo (Título do modelo, Status, Texto do contrato, Painel de Variáveis e Pré-visualização).

 |

---

### Caso de Teste 02: Inserir variáveis dinâmicas no corpo do contrato

| ID | Descrição |
| --- | --- |
| C11-CT02 | O sistema deve permitir a inclusão de tags/variáveis dinâmicas no editor de texto do contrato. |

| **Pré-condições** |
| --- |
| O usuário deve estar no formulário de adição/edição de **Modelos de Contrato**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está preenchendo ou editando o "Texto do contrato"

 |
| **QUANDO** seleciona ou clica em uma variável disponível na barra lateral direita (ex: Dados do aluno, Dados da academia ou Dados do contrato)

 |
| **ENTÃO** a tag correspondente (ex: `{nome_aluno}`, `{cpf_aluno}`, `{nome_academia}`) deve ser inserida no ponto onde está o cursor no editor de texto.

 |

| **Critérios de aceitação** |
| --- |
| As variáveis inseridas devem permanecer no texto formatadas corretamente para substituição dinâmica na geração dos contratos dos alunos.

 |

---

### Caso de Teste 03: Atualizar e validar a pré-visualização do contrato

| ID | Descrição |
| --- | --- |
| C11-CT03 | O sistema deve gerar e atualizar a pré-visualização do contrato de acordo com o texto digitado. |

| **Pré-condições** |
| --- |
| O usuário deve ter inserido conteúdo no campo "Texto do contrato".

 |

| **Passos** |
| --- |
| **DADO** que o usuário inseriu ou alterou a minuta do contrato no editor

 |
| **QUANDO** clica no botão "Atualizar preview" na seção de Pré-visualização do contrato

 |
| **ENTÃO** o quadro de visualização abaixo deve carregar o documento formatado com as cláusulas, formatação de texto e variáveis configuradas.

 |

| **Critérios de aceitação** |
| --- |
| O preview deve refletir exatamente a estrutura e formatação aplicadas no editor do contrato.

 |

---

### Caso de Teste 04: Salvar novo modelo de contrato com sucesso

| ID | Descrição |
| --- | --- |
| C11-CT04 | O sistema deve permitir salvar um modelo de contrato preenchido e retornar à listagem principal. |

| **Pré-condições** |
| --- |
| O usuário deve estar na página de adição de modelo de contrato.

 |

| **Passos** |
| --- |
| **DADO** que o usuário preenche o "Título do modelo" (ex: "Contrato de 1 ano de academia")

 |
| **E** mantém o status como "Ativo"

 |
| **E** insere o texto base com as cláusulas contratuais no editor

 |
| **QUANDO** clica no botão "Salvar modelo" no canto inferior direito

 |
| **ENTÃO** o sistema grava os dados e redireciona o usuário de volta para a tela "Modelos Contrato".

 |

| **Critérios de aceitação** |
| --- |
| O contrato cadastrado deve ser armazenado com sucesso e a tela principal de modelos deve ser recarregada.

 |

 https://jam.dev/c/eb0b3335-d069-4a60-9644-19edb2d36786
