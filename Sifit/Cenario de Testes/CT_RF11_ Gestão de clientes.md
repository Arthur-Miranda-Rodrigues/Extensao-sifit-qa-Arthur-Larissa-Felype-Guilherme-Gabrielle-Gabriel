
---

# Cenário 11: Gestão de Clientes

**Descrição:** Validação do módulo de Gestão de Clientes na plataforma SIFIT, englobando o cadastro completo com foto e dados de endereço/aplicativo, validação de campos obrigatórios em branco, ações no perfil do cliente, tratamento de exceções de exclusão e refinamento de buscas combinadas.

---

## Caso de Teste 01: Preenchimento Completo e Cadastro de Novo Cliente

| ID | Descrição |
| --- | --- |
| **C11-CT01** | Validar o fluxo de cadastro de um novo cliente informando identificação, documentos, foto, contatos, endereço, dados biométricos, credenciais de aplicativo e informações complementares/responsável.

 |

| **Pré-condições** |
| --- |
| Usuário autenticado na plataforma SIFIT e posicionado na tela de listagem de clientes.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de listagem de clientes e clica no botão **"+ Novo Cliente"**<br> |
| **QUANDO** preencher a seção de Identificação (Nome: "Livia", Status: "Ativo", Data de Nascimento, Tipo Sanguíneo)

 |
| **E** preencher os campos de Documentos (CPF e RG)

 |
| **E** carregar a foto do cliente via explorador de arquivos

 |
| **E** preencher os dados de Contato e Endereço (CEP, Estado, Cidade, Logradouro, Número, Bairro, Complemento)

 |
| **E** configurar a Biometria (Código do Leitor) e os dados de Acesso ao Aplicativo (Usuário e Senha)

 |
| **E** preencher os Dados do Responsável e Outros Dados (Estado Civil, Profissão)

 |
| **E** clicar no botão **"Cadastrar Cliente"**<br> |
| **ENTÃO** o sistema deve processar os dados e salvar o novo cliente com sucesso na base de dados.

 |

| **Critérios de aceitação** |
| --- |
| Todos os campos do formulário de cadastro devem ser persistidos corretamente, salvando o registro e exibindo o cliente na listagem geral.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KvJfzejSuqN4VbZbsa0ETD65awbK8TpF/view?usp=sharing |

---

## Caso de Teste 02: Validação de Campos Obrigatórios em Branco no Cadastro

| ID | Descrição |
| --- | --- |
| **C11-CT02** | Validar o comportamento do sistema ao tentar submeter o formulário de cadastro de cliente deixando campos obrigatórios em branco.

 |

| **Pré-condições** |
| --- |
| Usuário posicionado no formulário de cadastro de cliente (`/clientes/novo`).

 |

| **Passos** |
| --- |
| **DADO** que o usuário está no formulário de cadastro de cliente

 |
| **QUANDO** preencher apenas parcialmente os campos (ex.: preenchendo o nome e deixando campos obrigatórios como status, data de nascimento ou documentos em branco)

 |
| **E** clicar no botão **"Cadastrar Cliente"**<br> |
| **ENTÃO** o sistema deve barrar o envio, sinalizar visualmente as pendências e exibir alertas de validação nos campos obrigatórios não preenchidos.

 |

| **Critérios de aceitação** |
| --- |
| O sistema não deve permitir a criação de registros incompletos, exigindo o preenchimento de todas as obrigatoriedades cadastrais antes da persistência.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Q539d09tDet3RYqsRutnFXQCw18SvFOc/view?usp=sharing |

---

## Caso de Teste 03: Edição e Atualização de Dados no Perfil do Cliente

| ID | Descrição |
| --- | --- |
| **C11-CT03** | Validar a atualização cadastral de um cliente existente a partir de seu perfil, alterando dados de endereço, biometria, aplicativo e dados complementares.

 |

| **Pré-condições** |
| --- |
| Cliente previamente cadastrado e com perfil visível no sistema.

 |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o perfil de um cliente (ex.: *Steven Kaiki*) e clica na opção de editar dados

 |
| **QUANDO** modificar informações como endereço (Bairro, Complemento), código biométrico, credenciais do aplicativo e dados adicionais

 |
| **E** confirmar as alterações clicando em **"Salvar Alterações"** (com confirmação de segurança via PIN/Sistema quando exigido)

 |
| **ENTÃO** os dados cadastrais devem ser atualizados instantaneamente no perfil do aluno.

 |

| **Critérios de aceitação** |
| --- |
| As modificações feitas nos campos do perfil do cliente devem ser salvas de forma íntegra e refletidas imediatamente na aplicação.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1MfaZEVapyBr_rguipgIu4_MumS339T08/view?usp=sharing |

---

## Caso de Teste 04: Tratamento de Exceção em Tentativa de Exclusão de Cliente

| ID | Descrição |
| --- | --- |
| **C11-CT04** | Validar o comportamento do sistema ao acionar a exclusão de um registro de cliente na listagem, tratando eventuais falhas de servidor (*Erro no servidor*).

 |

| **Pré-condições** |
| --- |
| Usuário na tela de listagem de clientes visualizando os registros disponíveis.

 |

| **Passos** |
| --- |
| **DADO** que o usuário localiza um cliente na tabela de listagem

 |
| **QUANDO** clicar no ícone de exclusão (lixeira) na linha do cliente e confirmar a ação no modal de segurança

 |
| **ENTÃO** caso ocorra instabilidade ou restrição no backend, o sistema deve exibir o modal de alerta com a mensagem: *"Erro no servidor - Erro interno inesperado"* acompanhado do botão **Fechar**.

 |

| **Critérios de aceitação** |
| --- |
| O sistema deve tratar falhas críticas de exclusão exibindo um feedback visual amigável sem corromper a sessão do usuário.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1dB9oVQTKlkFWpnpEquTj4H1j7zWHehcK/view?usp=sharing |

---

## Caso de Teste 05: Pesquisa Avançada e Filtragem de Clientes por Código e Nome

| ID | Descrição |
| --- | --- |
| **C11-CT05** | Validar a consulta de clientes combinando filtros de código e nome diretamente nos campos de busca da listagem principal.

 |

| **Pré-condições** |
| --- |
| Usuário posicionado na tela de listagem de clientes do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de clientes

 |
| **QUANDO** preencher o campo de código (ex.: "388") e o campo de nome do cliente

 |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** o sistema deve filtrar e atualizar a tabela exibindo exclusivamente o registro correspondente aos parâmetros combinados.

 |

| **Critérios de aceitação** |
| --- |
| A busca combinada por código e nome deve retornar com precisão o registro cadastrado correspondente na grade de resultados.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1TGbyv27DdywqPIb7WrtA1Zps3kBk6Oaa/view?usp=sharing |
