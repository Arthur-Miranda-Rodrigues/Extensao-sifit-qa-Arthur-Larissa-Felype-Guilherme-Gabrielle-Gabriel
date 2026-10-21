## Cenário 29: Gestão de Funções

### Caso de Teste 01: Pesquisa e Filtragem de Funções por Nome e Tipo

| ID | Descrição |
| --- | --- |
| **C29-CT01** | O sistema deve filtrar e retornar corretamente a listagem de funções com base nos critérios de nome, código e tipo (interno ou externo). |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SIFIT e localizado na tela de **Funções**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu de **Funções**<br> |
| **QUANDO** preenche o campo de nome da função (ex.: "Treinador da academia") ou seleciona o tipo no filtro (ex.: "Interno" / "Externo") |
| **E** clica no botão **Buscar**<br> |
| **ENTÃO** o sistema deve atualizar a tabela exibindo apenas os registros correspondentes aos filtros aplicados. |

| **Critérios de Aceitação** |
| --- |
| * A tabela deve exibir de forma dinâmica apenas as funções que atendem aos parâmetros pesquisados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1v9YLpw8Vk1cWcQxe8Mff15EbzvZhaN-3/view?usp=sharing |

---

### Caso de Teste 02: Validação de Campos Obrigatórios ao Cadastrar Nova Função

| ID | Descrição |
| --- | --- |
| **C29-CT02** | O sistema deve impedir o cadastro e sinalizar a obrigatoriedade caso o usuário tente salvar uma nova função deixando campos obrigatórios em branco. |

| **Pré-condições** |
| --- |
| O usuário deve estar com o modal **Nova Função** aberto na tela de Funções. |

| **Passos** |
| --- |
| **DADO** que o usuário mantém o campo de nome da função em branco no modal de cadastro |
| **QUANDO** clica no botão **Salvar Função**<br> |
| **ENTÃO** o sistema deve bloquear o salvamento e exibir mensagens de alerta indicando a obrigatoriedade (ex.: "Preencha este campo"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir gravar registros incompletos, destacando visualmente as pendências nos campos obrigatórios. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KjINrIWCpnCh6lgtRxHZGsVhnL8SGWY8/view?usp=sharing |

---

### Caso de Teste 03: Cadastro de Nova Função com Sucesso

| ID | Descrição |
| --- | --- |
| **C29-CT03** | O sistema deve permitir o cadastro de uma nova função preenchendo corretamente os campos de nome, tipo de funcionário e parâmetros relacionados. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Funções** com o modal de nova função acessível. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Nova Função**<br> |
| **QUANDO** preenche o nome da função (ex.: "Caixa"), define o tipo de funcionário (ex.: "Interno/Externo") e configura as opções de Personal e Avaliador. |
| **E** clica em **Salvar Função**<br> |
| **ENTÃO** a nova função deve ser salva com sucesso e listada na tabela principal do sistema. |

| **Critérios de Aceitação** |
| --- |
| * A nova função deve ser registrada e exibida na listagem com os contadores de totais atualizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/13inRBRi1sz2beu95sRaJE4AC8yVdo1b5/view?usp=sharing |

---

### Caso de Teste 04: Configuração e Edição de Permissões da Função

| ID | Descrição |
| --- | --- |
| **C29-CT04** | O sistema deve permitir visualizar e alterar as permissões de acesso liberadas para uma determinada função. |

| **Pré-condições** |
| --- |
| Existir uma função cadastrada na tabela principal. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza a função na listagem e clica no ícone de permissões (chave/cadeado) na coluna de Ações |
| **QUANDO** o modal de **Permissões** for exibido e o usuário marcar ou desmarcar as caixas de seleção correspondentes aos módulos do sistema |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** as novas permissões de acesso devem ser vinculadas e salvas com sucesso para a função. |

| **Critérios de Aceitação** |
| --- |
| * As permissões alteradas devem persistir corretamente no sistema para o perfil da função selecionada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1mg24GsBuwFmdmgYTh0RfsB2laHGU2R6n/view?usp=sharing |

---

### Caso de Teste 05: Visualização dos Dados Cadastrais de uma Função

| ID | Descrição |
| --- | --- |
| **C29-CT05** | O sistema deve exibir o modal com os dados detalhados de uma função ao acionar a opção de visualização. |

| **Pré-condições** |
| --- |
| Existir uma função cadastrada na tabela de funções. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza uma função na tabela e clica no ícone de visualização (olho) na coluna de Ações |
| **QUANDO** o modal de visualização de dados for carregado |
| **ENTÃO** os detalhes da função (Código, Nome, Tipo de Funcionário, Personal e Avaliador) devem ser exibidos corretamente para conferência. |

| **Critérios de Aceitação** |
| --- |
| * O modal de visualização deve apresentar as informações precisas e consistentes com o registro selecionado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nxn1kU9MgyrnQxVqlim9i1GnBtz1CI-r/view?usp=sharing |
