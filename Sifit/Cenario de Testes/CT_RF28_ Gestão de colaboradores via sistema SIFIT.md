


---

## Cenário de teste: Gestão de colaboradores via sistema SIFIT

### Caso de Teste 01: Adicionar novo colaborador com dados válidos

| Item | Descrição |
| --- | --- |
| **ID** | C03-CT01 |
| **Descrição** | O sistema deve permitir o cadastro de um novo colaborador com dados válidos. |
| **Pré-condições** | O usuário deve estar logado no sistema SIFIT e ter permissão de acesso à tela de Colaboradores. |
| **Passos** | **DADO** que o usuário acessa o menu "Colaboradores"

<br>

<br>**E** clica no botão "Novo Colaborador"<br>

<br>**E** preenche os dados cadastrais (ex.: Nome "Steven Grant", Status "Ativo", Data de Nascimento, Sexo, Tipo Sanguíneo, CPF, RG, CREF, Cadastro de Login, Dados para Contato, Endereço, Biometria e Observação)<br>

<br>**QUANDO** clicar no botão "Salvar"<br>

<br>**ENTÃO** o colaborador deve ser cadastrado com sucesso e exibido na lista de Colaboradores. |
| **Critérios de Aceitação** | O novo colaborador cadastrado deve ser listado corretamente na tabela do menu "Colaboradores". |

---

### Caso de Teste 02: Tentar adicionar colaborador sem preencher campos obrigatórios

| Item | Descrição |
| --- | --- |
| **ID** | C03-CT02 |
| **Descrição** | O sistema deve impedir o cadastro e indicar obrigatoriedade ao tentar salvar um colaborador com campos obrigatórios em branco. |
| **Pré-condições** | O usuário deve estar logado no sistema e na tela de "Cadastrar Colaborador". |
| **Passos** | **DADO** que o usuário acessa a tela de "Cadastrar Colaborador"<br>

<br>**E** deixa os campos obrigatórios (como Tipo Sanguíneo, etc.) em branco<br>

<br>**QUANDO** clicar no botão "Salvar"<br>

<br>**ENTÃO** o sistema deve exibir o alerta "Este campo é obrigatório" abaixo dos campos não preenchidos. |
| **Critérios de Aceitação** | As mensagens de validação e obrigatoriedade devem ser exibidas indicando os campos pendentes. |

---

### Caso de Teste 03: Pesquisar colaborador já cadastrado

| Item | Descrição |
| --- | --- |
| **ID** | C03-CT03 |
| **Descrição** | O sistema deve filtrar e retornar corretamente o colaborador pesquisado por Código ou Nome. |
| **Pré-condições** | O colaborador pesquisado deve estar previamente cadastrado no sistema. |
| **Passos** | **DADO** que o usuário acessa o menu "Colaboradores"

<br>

<br>**E** digita o código (ex.: "3") ou o nome (ex.: "Marcelo Longo Zandonadi") nos campos de filtro "Código" ou "Nome"

<br>

<br>**QUANDO** clicar no botão "Buscar"

<br>

<br>**ENTÃO** o sistema deve filtrar a lista e exibir apenas o colaborador correspondente à busca.

 |
| **Critérios de Aceitação** | Apenas os registros correspondentes aos parâmetros informados na busca devem ser exibidos na tabela.

 |

https://jam.dev/c/0a093418-b086-4d01-8767-52162deece27
