

---

## Cenário: Gerenciamento de Modelos de Ficha

### Caso de Teste 01: Criar modelo de ficha com dados válidos e tratamento de erro na gravação

| ID | Descrição |
| --- | --- |
| **CT-01** | Validar o comportamento do sistema ao tentar salvar um novo modelo de ficha preenchendo os campos obrigatórios. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SiFit com permissão de acesso ao menu **Modelos de Ficha**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de **Modelos de Ficha** |
| **E** clica no botão de adicionar um novo modelo **(+)** |
| **QUANDO** preencher o campo "Nome do Modelo" (ex: "Lux") |
| **E** selecionar um personal no campo "Personal" (ex: "Gabriella") |
| **E** clicar em **Criar Modelo** |
| **ENTÃO** o sistema deve processar a requisição e, em caso de erro na API/servidor, exibir a mensagem *"Erro ao salvar modelo"* em um modal de alerta. |

| **Critérios de Aceitação** |
| --- |
| * O modal de erro deve ser exibido claramente ao usuário com a opção de fechar/tentar novamente. |
| * Se a gravação for bem-sucedida, o modal deve fechar e a nova ficha deve ser exibida na listagem de modelos. |

---

### Caso de Teste 02: Tentar criar modelo de ficha sem preencher campos obrigatórios

| ID | Descrição |
| --- | --- |
| **CT-02** | Validar se o sistema exibe mensagens de validação ao tentar criar um modelo com campos em branco. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela do modal **Novo Modelo de Ficha**. |

| **Passos** |
| --- |
| **DADO** que a janela modal "Novo Modelo de Ficha" está aberta |
| **QUANDO** o usuário não preencher os campos "Nome do Modelo" ou "Personal" |
| **E** clicar no botão **Criar Modelo** |
| **ENTÃO** o sistema deve impedir o envio do formulário e indicar os campos obrigatórios pendentes de preenchimento. |

| **Critérios de Aceitação** |
| --- |
| * O botão "Criar Modelo" não deve submeter a requisição se os dados mínimos não forem informados. |

---

### Caso de Teste 03: Filtrar/Pesquisar modelos de ficha por parâmetros

| ID | Descrição |
| --- | --- |
| **CT-03** | Validar a busca e filtragem na listagem de modelos de ficha. |

| **Pré-condições** |
| --- |
| Estar na tela inicial de **Modelos de Ficha**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a listagem de modelos de ficha |
| **QUANDO** preencher um dos filtros ("Código", "Título do modelo" ou "Nome do criador") |
| **E** clicar no botão de pesquisa (ícone de lupa) |
| **ENTÃO** a tabela abaixo deve atualizar e exibir apenas os registros correspondentes aos critérios informados. |

| **Critérios de Aceitação** |
| --- |
| * Se não houver correspondências, a mensagem *"Nenhum modelo de ficha encontrado"* deve continuar visível na listagem. |

https://jam.dev/c/1ba229ab-a763-4087-892b-b06d1a84b7a3
