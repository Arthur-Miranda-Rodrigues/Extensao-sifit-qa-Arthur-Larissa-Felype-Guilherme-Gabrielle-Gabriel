
---

## Cenário de teste: Gestão e consulta de leads no módulo Prospecção (CT_RF31)

### Caso de Teste 01: Buscar lead por nome com sucesso

| ID | Descrição |
| --- | --- |
| C09-CT01 | O sistema deve retornar corretamente o lead pesquisado pelo nome, e-mail, telefone ou código. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na tela de **Prospecção**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela de "Prospecção"

 |
| **E** insere o nome de um lead existente (ex: "Rafael Souzas") no campo de busca "Buscar lead"

 |
| **QUANDO** o sistema processa a busca

 |
| **ENTÃO** a lista deve exibir apenas o lead correspondente aos termos pesquisados

 |

| **Critérios de aceitação** |
| --- |
| O código, nome, estágio e data de criação do lead devem ser exibidos corretamente na tabela.

 |

---

### Caso de Teste 02: Filtrar por estágio do lead sem resultados

| ID | Descrição |
| --- | --- |
| C09-CT02 | O sistema deve exibir uma mensagem apropriada quando nenhum lead for encontrado para o estágio selecionado. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na tela de **Prospecção**. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela de "Prospecção"

 |
| **E** seleciona um estágio no filtro "Estágio" que não possua registros (ex: "Fez Aula Experimental", "Proposta" ou "Fechado")

 |
| **QUANDO** a listagem é atualizada

 |
| **ENTÃO** a mensagem "Nenhum lead encontrado." deve ser exibida na tabela

 |

| **Critérios de aceitação** |
| --- |
| O sistema deve informar claramente que não existem registros para o filtro aplicado.

 |

---

### Caso de Teste 03: Aplicar filtro por estágio do lead

| ID | Descrição |
| --- | --- |
| C09-CT03 | O sistema deve permitir a filtragem de leads por estágio no funil de vendas. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema e na tela de **Prospecção** com leads cadastrados. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa a tela de "Prospecção"

 |
| **E** seleciona uma opção no campo "Estágio" (ex: "Novo Contato" ou "Interessado")

 |
| **QUANDO** a listagem é atualizada

 |
| **ENTÃO** apenas os leads com o estágio selecionado devem ser listados na tabela

 |

| **Critérios de aceitação** |
| --- |
| O filtro deve atualizar a lista de forma dinâmica e apresentar apenas os leads do estágio selecionado.

 |

 https://jam.dev/c/ea730141-0f46-4cb3-8c28-cb732b94717b
