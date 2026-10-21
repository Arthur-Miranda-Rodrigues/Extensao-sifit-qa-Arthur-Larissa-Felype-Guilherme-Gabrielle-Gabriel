## Cenário 39: Gestão de Tipos de Pagamento no Sistema SIFIT

### Caso de Teste 01: Validação de Campos Obrigatórios ao Cadastrar Tipo de Pagamento

| ID | Descrição |
| --- | --- |
| **C39-CT01** | O sistema deve validar o preenchimento obrigatório dos campos ao tentar cadastrar um novo tipo de pagamento em branco. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e posicionado na tela **Tipos de Pagamento**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"+ Novo"** para abrir o modal de cadastro<br> |
| **QUANDO** tenta clicar diretamente no botão **"Salvar"** sem preencher os campos obrigatórios (como Nome) |
| **ENTÃO** o sistema deve exibir mensagens de validação/alerta bloqueando o salvamento e indicando o preenchimento necessário, mas o sistema salva mesmo assim. |

| **Critérios de Aceitação** |
| --- |
| * O cadastro não deve ser efetuado se houver campos obrigatórios vazios. |
| * Os alertas visuais devem orientar o usuário sobre as informações pendentes. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DJOIkA1NMxXX4LXgCUpR9l9xJCbwQ0dN/view?usp=sharing |

---

### Caso de Teste 02: Filtragem de Tipos de Pagamento por Código, Nome e Status

| ID | Descrição |
| --- | --- |
| **C39-CT02** | O sistema deve permitir a busca e filtragem precisa dos tipos de pagamento cadastrados utilizando código, nome ou status. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Tipos de Pagamento** com registros existentes na tabela.|

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Tipos de Pagamento"<br> |
| **QUANDO** preenche o campo "Código" (ex.: "1") ou o campo "Nome" (ex.: "Dinheiro") |
| **E** altera os filtros de status (ex.: Ativo/Inativo) e tipo |
| **ENTÃO** a tabela deve listar estritamente os registros correspondentes aos critérios aplicados ou exibir "Nenhum tipo de pagamento encontrado". |

| **Critérios de Aceitação** |
| --- |
| * A busca por múltiplos parâmetros deve retornar resultados precisos e atualizar dinamicamente a contagem na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1gspl432-BC5aibXGFWMFUYgU8jnUi1lV/view?usp=sharing |

---

### Caso de Teste 03: Cadastrar um Novo Tipo de Pagamento com Sucesso

| ID | Descrição |
| --- | --- |
| **C39-CT03** | O sistema deve permitir o cadastro de um novo tipo de pagamento definindo corretamente os campos obrigatórios, status, bandeira e integração. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Tipos de Pagamento**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **"+ Novo"**<br><br> |
| **QUANDO** preenche o campo **Nome** (ex: "PayPal"), define o **Status** como "Ativo", configura a bandeira, o tipo e a opção **"Pagamento Pelo Sistema"**<br> |
| **E** clica no botão **"Salvar"**<br><br> |
| **ENTÃO** o modal fecha e o novo tipo de pagamento é gravado com sucesso e exibido na listagem. |

| **Critérios de Aceitação** |
| --- |
| * O novo registro deve persistir no banco de dados e atualizar os contadores no topo da página (Total, Ativos/Inativos, Via Gateway). |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1bOuIpC0IAdiDdlAB4EbweGD2ago6KN-V/view?usp=sharing |

---

### Caso de Teste 04: Editar e Atualizar Dados de um Tipo de Pagamento

| ID | Descrição |
| --- | --- |
| **C39-CT04** | O sistema deve permitir a alteração e atualização das configurações de um tipo de pagamento existente. |

| **Pré-condições** |
| --- |
| Existir tipos de pagamento listados na tabela principal. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição de um item na listagem<br> |
| **QUANDO** altera parâmetros como "Pagamento Pelo Sistema" (ex: de "Não" para "Sim") |
| **E** clica no botão **"Salvar"**<br><br>|
| **ENTÃO** as modificações devem ser salvas e refletidas imediatamente na tabela. |
| **E** ao muda de **Status**  de **Inativo** para **Ativo**, permanece **Inativo** <br><br>|

| **Critérios de Aceitação** |
| --- |
| * As propriedades modificadas devem ser persistidas com sucesso e atualizadas na coluna "VIA GATEWAY" da listagem. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1a8HyikdekLeWsy5-fcHgBmbI5pl0xsuk/view?usp=sharing |

---

### Caso de Teste 05: Tentar Excluir Tipo de Pagamento Vinculado e Validar Mensagem de Erro

| ID | Descrição |
| --- | --- |
| **C39-CT05** | O sistema deve bloquear a remoção de tipos de pagamento vinculados a outras operações e exibir a mensagem de erro adequada. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Tipos de Pagamento**. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "X" (excluir) na linha de um tipo de pagamento<br> |
| **QUANDO** confirma a intenção no modal de exclusão clicando em **"Confirmar"**<br> |
| **ENTÃO** o sistema deve exibir um modal de alerta com o título "Erro" e a mensagem **"Erro ao deletar tipo de pagamento"**. |

| **Critérios de Aceitação** |
| --- |
| * O registro protegido não deve ser excluído e o usuário deve conseguir fechar o aviso de erro através do botão **"Fechar"**.|

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1d6OG4LJoPXy2d9ZcYwDV23_IXISCg0Uv/view?usp=sharing |
