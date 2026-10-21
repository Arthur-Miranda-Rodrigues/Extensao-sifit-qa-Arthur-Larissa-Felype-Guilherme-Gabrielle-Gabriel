
---

## Cenário 8: Gerenciamento de Check-ins.

## Caso de Teste 01: Filtro de Busca por Código ou Nome na Tabela de Check-ins
---

| ID | Descrição |
| --- | --- |
| **CT08-CT01** | Validar a busca por código ou nome diretamente no campo de pesquisa da listagem principal de check-ins. |

| **Pré-condições** |
| --- |
| Usuário autenticado na plataforma e posicionado na tela "Check-ins". |

| **Passos** |
| --- |
| **DADO** que o usuário acessou o menu lateral "Check-in".  |
| **QUANDO** utilizar o campo de busca acima da tabela (ex.: digitando "4143").  |
| **ENTÃO** o sistema deve filtrar em tempo real e exibir a mensagem "Nenhum registro encontrado" quando não houver correspondências. |
| **E** ao buscar por um nome ou código existente (ex.: "148" ou "Marcelo Longo"), a tabela deve filtrar e apresentar com precisão a linha do aluno correspondente. |

| **Critérios de aceitação** |
| --- |
| O campo de pesquisa da tabela principal deve filtrar os registros de check-in em tempo real conforme o código ou nome digitado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1BtIBChNujq9Bb3yRSW-OfKxu3oVBkneU/view?usp=sharing |

---

## Caso de Teste 02: Registro Direto de Entrada pela Tabela Principal

| ID | Descrição |
| --- | --- |
| **CT08-CT02** | Confirmar a confirmação de presença clicando na ação "Registrar entrada" na linha do aluno com status Pendente.|

| **Pré-condições** |
| --- |
| Aluno listado na tabela de Check-ins com o status "Pendente". |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de Check-ins visualizando os alunos com pendência de entrada. |
| **QUANDO** clicar no link/botão "Registrar entrada" na coluna Ação do aluno desejado. |
| **ENTÃO** o sistema deve exibir o indicador visual de carregamento ("Carregando..."). |
| **E** atualizar o status da presença do aluno para ativo/confirmado na lista principal. |

| **Critérios de aceitação** |
| --- |
| O clique na ação "Registrar entrada" na tabela deve alterar instantaneamente o estado da presença do cliente no sistema. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ZteZ0BoXsjpERQEgpaBRVhozu_n4qo1z/view?usp=sharing |

---

## Caso de Teste 03: Validação do Painel de Entrada Rápida por Código

| ID | Descrição |
| --- | --- |
| **CT08-CT03** | Validar o comportamento do painel lateral "Entrada rápida" ao inserir um código de cliente e acionar "Realizar check-in". |

| **Pré-condições** |
| --- |
| Estar na página principal do módulo de Check-ins. |

| **Passos** |
| --- |
| **DADO** que o usuário está no módulo de Check-ins. |
| **E** localiza o painel lateral "Entrada rápida". |
| **QUANDO** digitar o código de um cliente no campo "Código do cliente" (ex.: "390"). |
| **E** clicar no botão "Realizar check-in". |
| **ENTÃO** o sistema deve processar o código digitado e registrar a entrada rápida do cliente ou notificar a validação do identificador. |

| **Critérios de aceitação** |
| --- |
| O painel de entrada rápida deve aceitar a digitação do código do aluno e processar o check-in através do botão "Realizar check-in". |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1-Tf82n1hUsCA8Kv-mQAm221nR6Sup_Fr/view?usp=sharing |

---

## Caso de Teste 04: Processamento de Check-in Manual com Busca e Observação

| ID | Descrição |
| --- | --- |
| **CT08-CT04** | Validar o fluxo completo do modal "+ Check-in manual", incluindo busca por cliente, seleção e inserção de observação opcional. |

| **Pré-condições** |
| --- |
| Usuário posicionado na tela principal do módulo de Check-ins. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de Check-ins. |
| **QUANDO** clicar no botão "+ Check-in manual". |
| **E** o modal "Entrada manual" for aberto na aba "Cliente existente". |
| **E** pesquisar o cliente por nome no campo de busca (ex.: "pa", "Ueslei Nunes SouzaSS"). |
| **E** o sistema exibir o cartão "Cliente encontrado" destacando o status ("Cliente liberado para realizar o check-in").|
| **E** preencher o campo "Observação (OPCIONAL)" com um texto descritivo. |
| **E** clicar em "Registrar entrada". |
| **ENTÃO** o modal deve ser concluído com sucesso e a presença do aluno deve ser registrada na unidade. |

| **Critérios de aceitação** |
| --- |
| O modal de entrada manual deve localizar o cliente em tempo real, confirmar sua liberação, permitir anotação de observações e efetivar a entrada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1IZbE1qDhQv_EX1O6ex7KP8aXH9ZKRvOF/view?usp=sharing |
