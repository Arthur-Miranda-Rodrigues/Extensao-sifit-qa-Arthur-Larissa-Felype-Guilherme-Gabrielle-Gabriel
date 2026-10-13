
---

## Cenário: Gestão de Bandeiras de Cartão no sistema SIFIT

### Caso de Teste 01: Abrir modal de cadastro de bandeira de cartão

| ID | Descrição |
| --- | --- |
| C13-CT01 | O sistema deve abrir o modal "Nova Bandeira" com os campos zerados e prontos para preenchimento. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela **Bandeiras de Cartão**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Bandeiras de Cartão"

 |
| **QUANDO** clica no botão "Nova Bandeira" no canto superior direito

 |
| **ENTÃO** o modal "Nova Bandeira" deve ser exibido com os campos Nome, Taxa Adicional, Taxa Débito e a seção de Parcelas vazios/zerados.

 |

| **Critérios de aceitação** |
| --- |
| O modal deve carregar corretamente e permitir a inserção das informações de taxas e parcelas.

 |

---

### Caso de Teste 02: Adicionar taxas e regras de parcelamento a uma nova bandeira

| ID | Descrição |
| --- | --- |
| C13-CT02 | O sistema deve permitir a configuração do número de parcelas e suas respectivas taxas para a bandeira. |

| **Pré-condições** |
| --- |
| O modal "Nova Bandeira" deve estar aberto.

 |

| **Passos** |
| --- |
| **DADO** que o usuário preenche o "Nome" da bandeira (ex: "Loo")

 |
| **E** informa a "Taxa Adicional" (ex: "20,00") e "Taxa Débito" (ex: "5,00")

 |
| **QUANDO** clica no botão "+ Adicionar Parcela"

 |
| **E** preenche os campos "Nº Parcela" (ex: "10") e "Taxa" (ex: "2,50")

 |
| **E** clica no botão de confirmação (Check Azul)

 |
| **ENTÃO** a parcela configurada deve ser adicionada à listagem de parcelas no modal.

 |

| **Critérios de aceitação** |
| --- |
| As taxas de débito, adicionais e o parcelamento configurado devem ser vinculados corretamente à nova bandeira de cartão.

 |

---

### Caso de Teste 03: Cancelar o cadastro de uma nova bandeira de cartão

| ID | Descrição |
| --- | --- |
| C13-CT03 | O sistema deve descartar as informações inseridas ao clicar no botão "Cancelar". |

| **Pré-condições** |
| --- |
| O modal "Nova Bandeira" deve estar aberto com dados preenchidos.

 |

| **Passos** |
| --- |
| **DADO** que o usuário preencheu os campos da bandeira e/ou adicionou parcelas no modal

 |
| **QUANDO** clica no botão "Cancelar"

 |
| **ENTÃO** o modal deve ser fechado e nenhuma bandeira deve ser salva ou exibida na listagem.

 |

| **Critérios de aceitação** |
| --- |
| As alterações não devem ser persistidas no banco de dados e a tela deve retornar ao estado original de busca.

 |

---

### Caso de Teste 04: Consultar bandeiras de cartão por filtro de busca

| ID | Descrição |
| --- | --- |
| C12-CT04 | O sistema deve executar a consulta de bandeiras com base nos filtros informados. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Bandeiras de Cartão**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário informa um termo no campo "Código" ou "Nome"

 |
| **QUANDO** clica no botão de busca (ícone de lupa azul)

 |
| **ENTÃO** a tabela deve atualizar exibindo os resultados correspondentes ou a mensagem "Nenhuma bandeira encontrada" caso não haja registros.

 |

https://jam.dev/c/9fad678d-1a1b-4383-beff-a706ec7b55e7

| **Critérios de aceitação** |
| --- |
| A busca deve filtrar com precisão e apresentar a lista atualizada ou o feedback de ausência de dados.

 |
