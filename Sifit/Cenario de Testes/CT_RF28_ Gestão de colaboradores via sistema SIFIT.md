## Cenário 28: Gestão de Colaboradores via Sistema SIFIT

## 2. Cenários de Teste

### Caso de Teste 01: Pesquisa de Colaborador por Código ou Nome

| ID | Descrição |
| --- | --- |
| **C28-CT01** | O sistema deve filtrar e retornar corretamente o colaborador pesquisado através dos filtros de código ou nome. |

| **Pré-condições** |
| --- |
| O colaborador pesquisado deve estar previamente cadastrado no sistema e o usuário localizado no menu **Colaboradores**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu **Colaboradores**<br> |
| **QUANDO** digita o código (ex.: "3") ou o nome (ex.: "Santiago" / "Roselia Lima") nos campos de filtro correspondentes |
| **E** clica no botão **Buscar**<br> |
| **ENTÃO** o sistema deve filtrar a lista exibindo apenas os registros correspondentes aos critérios informados.|

| **Critérios de Aceitação** |
| --- |
| * A tabela deve atualizar dinamicamente mostrando somente o(s) colaborador(es) correspondentes à busca realizada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1OmidiBr9VA3wfZ5eE7ktdnJryGPCqupO/view?usp=sharing |

---

### Caso de Teste 02: Adicionar Novo Colaborador com Dados Válidos

| ID | Descrição |
| --- | --- |
| **C28-CT02** | O sistema deve permitir o cadastro bem-sucedido de um novo colaborador com o preenchimento de todos os dados válidos. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema SIFIT na tela de cadastro de colaboradores. |

| **Passos** |
| --- |
| **DADO** que o usuário preenche os campos obrigatórios e complementares (Nome: "Steven Grant", Status, Data de Nascimento, Sexo, Tipo Sanguíneo, Documentos, Login, Contato, Endereço e Observações) |
| **QUANDO** clicar no botão **Salvar** localizado no rodapé da página |
| **ENTÃO** o colaborador deve ser cadastrado com sucesso na base de dados |
| **E** ser exibido corretamente na listagem principal de Colaboradores. |

| **Critérios de Aceitação** |
| --- |
| * O novo colaborador deve ser gravado e listado na tabela geral do sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1G_8tH2MkFsMSfAtwgx2eD53JmmdUqNIE/view?usp=sharing |

---

### Caso de Teste 03: Edição de Colaborador (Inativação de Status)

| ID | Descrição |
| --- | --- |
| **C28-CT03** | O sistema deve permitir alterar os dados cadastrais e o status de um colaborador já existente. |

| **Pré-condições** |
| --- |
| Existir um colaborador cadastrado na listagem do sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de edição (lápis) de um colaborador na tabela |
| **QUANDO** altera o status (ex.: de "Ativo" para "Inativo") ou outros dados no formulário |
| **E** clica em salvar as alterações |
| **ENTÃO** o registro do colaborador deve ser atualizado instantaneamente no sistema. |

| **Critérios de Aceitação** |
| --- |
| * As modificações de status e informações devem persistir corretamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1v7em5hEY_rUXzjJIiwZdHY4oG0E1Bd7L/view?usp=sharing |

---

### Caso de Teste 04: Gerenciamento e Vinculação de Funções do Colaborador

| ID | Descrição |
| --- | --- |
| **C28-CT04** | O sistema deve permitir gerenciar, vincular ou adicionar novas funções (ex.: "Treinador da academia", "Personal") a um colaborador. |

| **Pré-condições** |
| --- |
| O usuário estar na listagem e acionar a opção de gerenciar funções de um colaborador. |

| **Passos** |
| --- |
| **DADO** que o usuário abre o modal **Gerenciar Funções** para um colaborador |
| **QUANDO** seleciona uma função na lista suspensa (ex.: "Treinador da academia") e clica no botão **Adicionar**<br> |
| **ENTÃO** a função deve ser vinculada com sucesso ao colaborador |
| **E** ser listada na tabela de funções atreladas dentro do modal. |

| **Critérios de Aceitação** |
| --- |
| * A vinculação de funções deve ser registrada e refletida sem erros na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1YdRjDAjgdsA2MKxKLYG_IRf_uKA2Kpv3/view?usp=sharing |

---

### Caso de Teste 05: Visualização do Perfil Detalhado do Colaborador

| ID | Descrição |
| --- | --- |
| **C28-CT05** | O sistema deve exibir uma tela de perfil detalhado com todas as informações e métricas consolidadas ao selecionar um colaborador. |

| **Pré-condições** |
| --- |
| Existir um colaborador cadastrado na tabela principal. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o colaborador na listagem |
| **QUANDO** clica no ícone de visualização/detalhes correspondente (botão de olho) |
| **ENTÃO** o sistema deve redirecionar para a página **Perfil do Colaborador**<br> |
| **E** exibir os cards de resumo (Alunos, Recebimentos, Funções, Tempo de casa), dados pessoais e contatos. |

| **Critérios de Aceitação** |
| --- |
| * As informações e métricas do colaborador devem ser carregadas e apresentadas corretamente no perfil. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1zMi6h3Ax60VPH_ANN3zsPFbc3V37hLcX/view?usp=sharing |

---

### Caso de Teste 06: Validação de Campos Obrigatórios no Cadastro de Colaborador

| ID | Descrição |
| --- | --- |
| **C28-CT06** | O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar um colaborador com campos obrigatórios vazios. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de cadastro de novo colaborador. |

| **Passos** |
| --- |
| **DADO** que o usuário deixa campos obrigatórios em branco (como Nome, Tipo Sanguíneo ou dados essenciais) |
| **QUANDO** clica no botão **Salvar**<br> |
| **ENTÃO** o sistema deve bloquear a operação e exibir mensagens de alerta de preenchimento obrigatório abaixo dos campos correspondentes (ex.: "Este campo é obrigatório").  |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir gravar registros sem os dados obrigatórios preenchidos, destacando visualmente as pendências. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1jTxhy8gCtsDW1y5fBibU1K2TmtqlQcb2/view?usp=sharing |

---

### Caso de Teste 07: Exclusão de Colaborador

| ID | Descrição |
| --- | --- |
| **C28-CT07** | O sistema deve permitir a remoção definitiva de um colaborador cadastrado mediante confirmação em modal. |

| **Pré-condições** |
| --- |
| Existir um colaborador cadastrado passível de exclusão na listagem.

 |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o colaborador na tabela principal e clica no ícone de exclusão (lixeira) na coluna de Ações|
| **QUANDO** o modal de confirmação "Deseja deletar este colaborador?" for exibido e o usuário clicar em **Continuar**<br> |
| **ENTÃO** o registro do colaborador deve ser permanentemente removido da base de dados e da listagem. |

| **Critérios de Aceitação** |
| --- |
| * O colaborador selecionado deve ser apagado corretamente após a confirmação. |
| * Os contadores gerais da tela de colaboradores devem ser atualizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1c4xlEkphLqHfLKmIJup15duqnErL_5wj/view?usp=sharing |
