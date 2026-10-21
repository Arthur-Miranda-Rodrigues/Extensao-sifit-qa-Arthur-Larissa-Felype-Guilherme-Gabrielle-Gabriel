## Cenário 37: Gestão e consulta de planos no sistema SIFIT

### Caso de Teste 01: Pesquisa de Plano por Código, Nome ou Status

| ID | Descrição |
| --- | --- |
| **C37-CT01** | O sistema deve filtrar e retornar corretamente o plano correspondente ao utilizar os filtros de código, nome ou status (Ativo/Inativo). |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema e na página de **Planos**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Planos**<br> |
| **QUANDO** insere o código (ex: "32"), o nome do plano (ex: "Aba") ou seleciona o status no filtro correspondente e clica em **Buscar**<br> |
| **ENTÃO** a tabela de resultados deve listar apenas o registro correspondente ao filtro informado. |

| **Critérios de Aceitação** |
| --- |
| * As informações exibidas na tabela (Código, Nome, Alunos, Valor, Duração e Status) devem ser condizentes com o plano pesquisado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1l5q-a7dAbEAe8SYRnm5lLZa9V3Vue6HC/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Novo Plano com Sucesso

| ID | Descrição |
| --- | --- |
| **C37-CT02** | O sistema deve permitir o cadastro bem-sucedido de um novo plano definindo dados básicos, valores, períodos de cobrança e regras de equipe/dependentes. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de **Planos** com o modal "+ Novo Plano" acessível. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **+ Novo Plano**<br> |
| **QUANDO** preenche o nome (ex: "Aba"), seleciona o grupo, define a modalidade de cobrança, duração, parcelas, valores, parâmetros de personal/função e benefícios |
| **E** clica no botão **Salvar Plano**<br> |
| **ENTÃO** o modal é fechado e o novo plano é adicionado à listagem do sistema. |

| **Critérios de Aceitação** |
| --- |
| * O plano deve ser salvo com sucesso e refletir nos contadores e na listagem geral do sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1oanKKQddBc4EAFQH6kVl-sipn0OdOL4p/view?usp=sharing |

---

### Caso de Teste 03: Edição de Plano Existente

| ID | Descrição |
| --- | --- |
| **C37-CT03** | O sistema deve permitir a alteração das informações e do status (Ativo/Inativo) de um plano já cadastrado. |

| **Pré-condições** |
| --- |
| Existir um plano previamente cadastrado na tabela principal. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o plano na listagem e clica no ícone de edição (lupa/lápis) do registro |
| **QUANDO** altera configurações necessárias no modal, como o status (ex: para "Ativo") ou a quantidade de dependentes |
| **E** clica no botão **Salvar Plano**<br> |
| **ENTÃO** as alterações devem ser gravadas e atualizadas na listagem imediatamente. |

| **Critérios de Aceitação** |
| --- |
| * As informações modificadas devem ser persistidas e exibidas corretamente na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1JuBEIGyYbJ9aJ5r1gA0ufP5p-K51wDAh/view?usp=sharing |

---

### Caso de Teste 04: Tentativa de Exclusão de Plano Vinculado

| ID | Descrição |
| --- | --- |
| **C37-CT04** | O sistema deve impedir a exclusão de um plano que possua vínculos ativos e apresentar uma mensagem de erro apropriada. |

| **Pré-condições** |
| --- |
| Existir um plano listado na tabela que possua dependências ou alunos vinculados. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão ("X") de um plano na tabela |
| **QUANDO** o modal de confirmação "Deseja deletar o Plano?" é exibido e o usuário clica em **Confirmar**<br> |
| **ENTÃO** o sistema deve processar a requisição e exibir uma mensagem de alerta/modal informando "Erro ao deletar Plano". |

| **Critérios de Aceitação** |
| --- |
| * O plano não deve ser removido do banco de dados caso possua restrições, exibindo a mensagem de erro de forma clara. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1de8saJ7mYqSROLZLBznVBWbAhUJDUbyY/view?usp=sharing |

---

### Caso de Teste 05: Validação de Campos Obrigatórios no Cadastro de Plano

| ID | Descrição |
| --- | --- |
| **C37-CT05** | O sistema deve impedir o salvamento e sinalizar a obrigatoriedade caso o usuário tente cadastrar um plano sem preencher os campos essenciais. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal "+ Novo Plano" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário deixa campos obrigatórios em branco (como o Nome do plano) no modal de cadastro |
| **QUANDO** clica no botão **Salvar Plano**<br> |
| **ENTÃO** o sistema deve bloquear a operação e exibir mensagens de alerta indicando as pendências de preenchimento. |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir gravar registros incompletos, destacando as validações obrigatórias na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nL_bo2pMlqooZhDG0cF0lzY8JrlWYNJ-/view?usp=sharing |
