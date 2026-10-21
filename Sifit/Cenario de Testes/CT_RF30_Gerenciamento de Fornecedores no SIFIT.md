## Cenário 30: Gerenciamento de Fornecedores no SIFIT

## 2. Cenários de Teste

### Caso de Teste 01: Pesquisa de Fornecedor por Código ou Nome

| ID | Descrição |
| --- | --- |
| **C30-CT01** | O sistema deve permitir a busca e filtragem de fornecedores cadastrados utilizando os campos de código ou nome. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT e posicionado na tela de **Fornecedores**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu de **Fornecedores**<br> |
| **QUANDO** preenche o campo "Código" (ex: "205") ou o campo "Nome" (ex: "Jayna Souza") e clica no botão **Buscar**<br> |
| **ENTÃO** o sistema deve filtrar e exibir na tabela apenas o registro correspondente aos critérios informados. |

| **Critérios de Aceitação** |
| --- |
| * A tabela de fornecedores deve atualizar dinamicamente exibindo apenas os registros que satisfaçam a busca realizada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ZDVpVulOATOYG8SfbfXpo4WGNofro_Tk/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Novo Fornecedor com Dados Válidos

| ID | Descrição |
| --- | --- |
| **C30-CT02** | O sistema deve permitir o cadastro de um novo fornecedor preenchendo corretamente os campos obrigatórios e complementares no modal "Novo Fornecedor". |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela de **Fornecedores** com o modal de cadastro aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Novo Fornecedor**<br> |
| **QUANDO** preenche o nome (ex: "Lucas Castro"), documentos, contatos (telefones e e-mail), endereço completo (Estado, Cidade, CEP, Número, Bairro, Complemento) e observações |
| **E** clica no botão **Salvar**<br> |
| **ENTÃO** o novo fornecedor deve ser adicionado com sucesso e exibido na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * O fornecedor criado deve aparecer na listagem geral com o status ativo e os contadores da tela devem ser incrementados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/19U34BvJM8nNhDbGxHMGBGblR5BjaIM1k/view?usp=sharing |

---

### Caso de Teste 03: Validação de Campos Obrigatórios no Cadastro de Fornecedor

| ID | Descrição |
| --- | --- |
| **C30-CT03** | O sistema deve impedir o cadastro e emitir mensagens de alerta caso o usuário tente salvar um fornecedor sem preencher os campos obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário deve estar no modal "Novo Fornecedor". |

| **Passos** |
| --- |
| **DADO** que o usuário deixa campos obrigatórios em branco (como o Nome do fornecedor ou dados essenciais) |
| **QUANDO** tenta clicar no botão **Salvar**<br> |
| **ENTÃO** o sistema deve bloquear a operação e exibir mensagens de aviso/erro sinalizando a obrigatoriedade dos campos (ex: "Insira o nome do fornecedor" / "Erro ao salvar fornecedor"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema não deve permitir a gravação de registros incompletos, alertando o usuário sobre as pendências. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1twhWPHchIr378KEPXb_NnglgAF2-hEzT/view?usp=sharing |

---

### Caso de Teste 04: Visualização Detalhada do Fornecedor

| ID | Descrição |
| --- | --- |
| **C30-CT04** | O sistema deve exibir todas as informações consolidadas de um fornecedor ao acionar a opção de visualização de cadastro. |

| **Pré-condições** |
| --- |
| Existir um fornecedor previamente cadastrado na tabela. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza um fornecedor na tabela principal |
| **QUANDO** clica no ícone de visualização (olho) na coluna de Ações |
| **ENTÃO** o modal "Visualizar Fornecedor" deve abrir exibindo detalhadamente os dados de cadastro, contatos, endereços e observações. |

| **Critérios de Aceitação** |
| --- |
| * As informações detalhadas do fornecedor selecionado devem ser apresentadas corretamente para consulta. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1SOkoJ69Mxnc7aizsR6R_kksNUVm0foAl/view?usp=sharing |

---

### Caso de Teste 05: Tentativa de Exclusão de Fornecedor com Confirmação

| ID | Descrição |
| --- | --- |
| **C30-CT05** | O sistema deve exigir confirmação em modal ao solicitar a exclusão de um fornecedor e processar a requisição de remoção. |

| **Pré-condições** |
| --- |
| Existir um fornecedor listado na tabela. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de exclusão (lixeira/X) de um fornecedor na tabela |
| **QUANDO** o modal de confirmação "Deseja deletar este fornecedor?" é exibido e o usuário clica em **Continuar**<br> |
| **ENTÃO** o sistema deve processar a solicitação de exclusão ou retornar tratativas de resposta do servidor. |

| **Critérios de Aceitação** |
| --- |
| * A ação de exclusão deve ser submetida após a confirmação explícita do usuário no modal de segurança. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/19nWDHldALiY5XZoa_9GRiJjjGmjTU5pK/view?usp=sharing |
