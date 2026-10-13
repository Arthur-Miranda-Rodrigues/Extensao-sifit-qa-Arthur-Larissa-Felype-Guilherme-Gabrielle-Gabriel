


---

## Cenário de teste: Módulo Inteligência & Automação e Gestão de Clientes

### Caso de Teste 01: Execução da automação de Risco de Evasão e consulta do relatório de alunos

| ID | Descrição |
| --- | --- |
| C06-CT01 | O sistema deve permitir a execução da automação de Risco de Evasão e exibir o relatório detalhado dos alunos com os respetivos scores de risco. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no sistema SIFIT e a automação "Risco de Evasão" deve estar ativa no painel de "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu "Inteligência & Automação" |
| **E** clica em "Executar agora" no card da automação "Risco de Evasão" |
| **E** clica em "Ver resultados" para expandir o "Relatório de Risco de Evasão" |
| **QUANDO** selecionar um aluno da lista (ex: "gabrieli bononi") |
| **ENTÃO** o painel lateral deve ser exibido com os detalhes do score de risco, motivos e informações complementares |

| **Critérios de aceitação** |
| --- |
| Os motivos do score, a contagem de dias sem treinar e a recomendação de contato de urgência devem ser apresentados corretamente. |

---

### Caso de Teste 02: Tentativa de execução manual de automação sem suporte (Aniversariantes)

| ID | Descrição |
| --- | --- |
| C06-CT02 | O sistema deve exibir mensagem informativa ao tentar executar manualmente uma automação que não suporta acionamento manual. |

| **Pré-condições** |
| --- |
| O usuário deve estar na página "Inteligência & Automação". |

| **Passos** |
| --- |
| **DADO** que o usuário está no painel "Inteligência & Automação" |
| **E** localiza o card da automação "Aniversariantes" |
| **QUANDO** clicar em "Executar agora" |
| **ENTÃO** um pop-up de aviso com o título "Aviso" e a mensagem "Execução manual ainda não disponível para esta automação" deve ser exibido |

| **Critérios de aceitação** |
| --- |
| O sistema impede a execução manual e disponibiliza o botão "Entendi" para fechar o modal. |

---

### Caso de Teste 03: Edição e atualização de dados cadastrais e de aplicativo do cliente

| ID | Descrição |
| --- | --- |
| C06-CT03 | O sistema deve permitir a edição e salvamento das informações de contato, endereço, biometria e credenciais de aplicativo do cliente. |

| **Pré-condições** |
| --- |
| O cliente deve estar cadastrado no sistema e acessível via tela "Visualizar Cliente". |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Visualizar Cliente" do aluno |
| **E** clica em "Alterar dados" |
| **E** preenche/atualiza os campos em "Contato" (Telefone, Celular), "Endereço" (Logradouro, Número, Bairro), "Biometria" e credenciais do "Aplicativo" (Usuário e Senha) |
| **QUANDO** clicar no botão "Salvar Alterações" |
| **ENTÃO** o sistema processa a requisição e atualiza os dados do perfil do cliente |

| **Critérios de aceitação** |
| --- |
| As informações editadas devem ser persitidas no formulário do cliente após o salvamento. |

https://jam.dev/c/4bcd5e50-1f48-4678-8912-1709888ccb30
