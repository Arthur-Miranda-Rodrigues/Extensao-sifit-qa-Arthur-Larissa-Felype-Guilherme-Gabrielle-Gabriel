
---

# Cenário 31: Gerenciamento de Tipos de Documentos no SIFIT

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo de **Configurações > Tipos de Documentos** do sistema **SiFit**. O objetivo é validar as funcionalidades de busca de tipos de documentos por código, nome e aplicação, o cadastro de novos tipos de documentos com validação de campos obrigatórios, a edição de registros existentes, a visualização detalhada de dados e a tentativa de exclusão de registros na plataforma.

---

## 2. Cenários de Teste

### Caso de Teste 01: Pesquisa de Tipos de Documentos por Código, Nome ou Aplicação

| ID | Descrição |
| --- | --- |
| **C31-CT01** | O sistema deve permitir a filtragem de tipos de documentos cadastrados utilizando os campos de código, nome ou o filtro de aplicação. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e localizado na tela **Tipos de Documentos**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu **Tipos de Documentos**<br> |
| **QUANDO** preenche o campo "Código" (ex: "3"), o campo "Nome do documento" (ex: "vale") ou seleciona uma opção no filtro de "Aplicação" |
| **E** clica no botão de busca (lupa) |
| **ENTÃO** o sistema deve atualizar a tabela exibindo somente os itens que correspondem aos critérios informados. |

| **Critérios de Aceitação** |
| --- |
| * A tabela de registros deve ser atualizada dinamicamente com base nos filtros selecionados pelo usuário. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1y4fVIJ5CdjNLbGhCuwrj_TcpDgml5fIt/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Novo Tipo de Documento com Sucesso

| ID | Descrição |
| --- | --- |
| **C31-CT02** | O sistema deve permitir a criação bem-sucedida de um novo tipo de documento definindo seu nome e a respectiva aplicação. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de **Tipos de Documentos** com o modal de novo tipo acessível. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Novo Tipo**<br> |
| **QUANDO** preenche o campo "Nome" (ex: "Eventos") e seleciona a "Aplicação" (ex: "Conta / Fornecedor") |
| **E** clica no botão **Salvar**<br> |
| **ENTÃO** o novo tipo de documento deve ser gravado com sucesso e exibido na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * O novo registro deve ser incluído na tabela e os contadores de totais por aplicação devem ser incrementados corretamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/18wEPVnCfQ4bUGLGPC78VQ7xK2L2muMbX/view?usp=sharing |

---

### Caso de Teste 03: Validação de Campos Obrigatórios ao Cadastrar Tipo de Documento

| ID | Descrição |
| --- | --- |
| **C31-CT03** | O sistema deve impedir o salvamento e emitir um aviso caso o usuário tente cadastrar um tipo de documento com o campo de nome vazio. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal "Tipo de Documento" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário deixa o campo "Nome" em branco no modal de cadastro |
| **QUANDO** clica no botão **Salvar**<br> |
| **ENTÃO** o sistema deve bloquear a ação e exibir um aviso de validação (ex: "Informe o nome do tipo de documento"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir a gravação de dados incompletos, alertando o usuário sobre a pendência no campo obrigatório. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1i0G4RR8tmpyFLpPVgOLPu3Fum47JA0f7/view?usp=sharing |

---

### Caso de Teste 04: Edição de Tipo de Documento (Alteração de Aplicação)

| ID | Descrição |
| --- | --- |
| **C31-CT04** | O sistema deve permitir alterar os dados cadastrais (como a aplicação) de um tipo de documento já existente. |

| **Pré-condições** |
| --- |
| Existir um tipo de documento cadastrado na lista principal. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição/lupa de um registro na tabela |
| **QUANDO** modifica o campo de "Aplicação" (ex: de "Colaborador" para "Conta / Fornecedor") |
| **E** clica no botão **Salvar**<br> |
| **ENTÃO** a alteração deve ser gravada e refletida imediatamente na listagem. |

| **Critérios de Aceitação** |
| --- |
| * As modificações efetuadas devem persistir corretamente no sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1dCntTSlneTEGNeHm-KCXA-iJ6DoQid5t/view?usp=sharing |

---

### Caso de Teste 05: Tentativa de Exclusão de Tipo de Documento com Confirmação

| ID | Descrição |
| --- | --- |
| **C31-CT05** | O sistema deve solicitar confirmação via modal ao tentar excluir um tipo de documento e processar a solicitação de remoção. |

| **Pré-condições** |
| --- |
| Existir um tipo de documento cadastrado na tabela. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (X) de um registro na tabela |
| **QUANDO** o modal de confirmação "Deseja remover o tipo de Documento?" for exibido e o usuário clicar em **Confirmar**<br> |
| **ENTÃO** o sistema deve processar a requisição de exclusão e retornar a tratativa correspondente do servidor. |

| **Critérios de Aceitação** |
| --- |
| * O fluxo de exclusão deve exigir a confirmação explícita do usuário antes de submeter a remoção. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1jBvZS9vvYmmD4du6-XqWbr-cwRreILNc/view?usp=sharing |
