## Cenário 26: Gerenciamento e Cadastro de Despesas Fixas

### Caso de Teste 01: Filtragem de Despesas Fixas por Nome e Recorrência

| ID | Descrição |
| --- | --- |
| **C26-CT01** | O sistema deve permitir a busca e filtragem de despesas fixas utilizando os filtros de nome e recorrência na interface. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela de "Despesas Fixas" no módulo Financeiro. |

| **Passos** |
| --- |
| **DADO** que o usuário está visualizando a listagem completa de despesas fixas |
| **QUANDO** preencher o campo de busca por nome (ex.: "Energia") |
| **E** interagir com os seletores de filtros de status e recorrência |
| **ENTÃO** a tabela deve exibir dinamicamente os registros correspondentes aos filtros aplicados e recalcular os indicadores de valores. |

| **Critérios de Aceitação** |
| --- |
| * A listagem deve responder aos filtros aplicados, exibindo apenas os registros correspondentes. |
| * Os cards de resumo superior devem refletir os dados filtrados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Ut2y3_D4efnwfn6SGBGLVNia3rpr2Fw6/view?usp=sharing |

---

### Caso de Teste 02: Cadastrar uma Nova Despesa Fixa com Sucesso

| ID | Descrição |
| --- | --- |
| **C26-CT02** | O sistema deve permitir o cadastro de uma nova despesa fixa preenchendo todos os campos obrigatórios no modal correspondente. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela de "Despesas Fixas". |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão "Nova Despesa" (ícone `+` no topo superior direito). |
| **E** preenche o campo "Nome da despesa" (ex.: "Comida"). |
| **E** define o "Status" como "Ativo"  |
| **E** insere o "Valor" (ex.: "2000,00") |
| **QUANDO** clicar no botão **Salvar Despesa**<br> |
| **ENTÃO** a nova despesa deve ser salva e exibida na listagem principal com o status "ATIVO".|

| **Critérios de Aceitação** |
| --- |
| * A nova despesa deve ser gravada com sucesso e listada corretamente na tabela. |
| * O valor total somado nos cards do topo deve ser atualizado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1_uVSF9Upmf_bqHgll-ClQ-NN-QDjpYK3/view?usp=sharing |

---

### Caso de Teste 03: Edição e Atualização de Despesa Fixa

| ID | Descrição |
| --- | --- |
| **C26-CT03** | O sistema deve permitir editar os parâmetros (como valor, status ou recorrência) de uma despesa fixa já existente. |

| **Pré-condições** |
| --- |
| Existir ao menos uma despesa fixa previamente cadastrada na listagem. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição de uma despesa na tabela |
| **QUANDO** alterar os campos desejados (ex.: alterar valor para "200" e o status para "Inativo") |
| **E** clicar em **Salvar Despesa**<br> |
| **ENTÃO** as alterações devem ser gravadas e refletidas imediatamente na linha correspondente da tabela. |

| **Critérios de Aceitação** |
| --- |
| * As modificações de dados e status devem ser atualizadas de forma persistente. |
| * A tabela deve recarregar exibindo as informações atualizadas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1wJdBFo6c8_TcQtw5GVQqny-1_iqXLkgj/view?usp=sharing |

---

### Caso de Teste 04: Exclusão de Despesa Fixa

| ID | Descrição |
| --- | --- |
| **C26-CT04** | O sistema deve permitir a remoção definitiva de uma despesa fixa mediante confirmação em modal. |

| **Pré-condições** |
| --- |
| Existir uma despesa fixa cadastrada passível de exclusão.|

| **Passos** |
| --- |
| **DADO** que o usuário localiza a despesa na listagem e clica no ícone de exclusão (lixeira) na coluna de Ações |
| **QUANDO** o modal de confirmação "Deseja deletar a despesa fixa?" for exibido e o usuário clicar em **Continuar**<br> |
| **ENTÃO** a despesa deve ser permanentemente removida da base de dados e da listagem. |

| **Critérios de Aceitação** |
| --- |
| * O registro selecionado deve ser apagado corretamente após a confirmação. |
| * Os contadores e totais da tela devem ser recalculados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1JQh1lCoflH2tu40DpRzLGveULEE46lVK/view?usp=sharing |

---

### Caso de Teste 05: Validação de Campos Obrigatórios ao Cadastrar Nova Despesa

| ID | Descrição |
| --- | --- |
| **C26-CT05** | O sistema deve validar o preenchimento dos campos obrigatórios e exibir mensagens de erro/alerta caso o usuário tente salvar uma nova despesa com campos vazios. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal "Nova Despesa" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário mantém campos obrigatórios (como o nome da despesa ou valor) em branco no modal de cadastro |
| **QUANDO** clicar no botão **Salvar Despesa**<br> |
| **ENTÃO** o sistema deve impedir a conclusão do cadastro |
| **E** exibir mensagens de validação solicitando o preenchimento dos campos obrigatórios (ex.: "Preencha este campo"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir gravar registros incompletos na base de dados. |
| * Os avisos visuais de validação devem apontar diretamente para os campos não preenchidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1e8M1JswuAQP_hLPcV5vu_xS82sMfHHxO/view?usp=sharing |
