## Cenário 40: Gestão de Bandeiras de Cartão no Sistema SIFIT

### Caso de Teste 01: Validação de Campos Obrigatórios e Abertura do Modal de Nova Bandeira

| ID | Descrição |
| --- | --- |
| **C40-CT01** | O sistema deve abrir o modal "Nova Bandeira" com os campos limpos e validar o preenchimento obrigatório ao tentar salvar sem o nome da bandeira. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e posicionado na tela **Bandeiras de Cartão**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Bandeiras de Cartão<br> |
| **QUANDO** clica no botão **"Nova Bandeira"** no canto superior direito |
| **ENTÃO** o modal "Nova Bandeira" deve ser exibido com os campos de código, nome, taxas e parcelas zerados/vazios. |
| **DADO** que o usuário tenta clicar no botão **"Salvar"** com o campo "Nome" vazio<br> |
| **ENTÃO** o sistema deve exibir um aviso de alerta informando "Informe o nome da bandeira". |

| **Critérios de Aceitação** |
| --- |
| * O modal deve carregar corretamente permitindo a inserção de dados. |
| * O sistema deve bloquear o salvamento caso o campo obrigatório "Nome" não esteja preenchido, exibindo o pop-up de aviso. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/14_n6VY4kp9UXFn_QR8N-qEjqOvZ4GpAo/view?usp=sharing |

---

### Caso de Teste 02: Cadastro de Nova Bandeira com Taxas e Regras de Parcelamento

| ID | Descrição |
| --- | --- |
| **C40-CT02** | O sistema deve permitir o preenchimento do nome, taxas adicionais, taxa de débito e a adição de regras de parcelamento para uma nova bandeira. |

| **Pré-condições** |
| --- |
| O modal "Nova Bandeira" deve estar aberto na tela. |

| **Passos** |
| --- |
| **DADO** que o usuário preenche o campo **"Nome"** da bandeira (ex.: "Bandeira Azul")<br>|
| **QUANDO** informa a **"Taxa Adicional"** (ex.: "20,00") e a **"Taxa Débito"** (ex.: "10,00") |
| **E** clica no botão **"+ Adicionar Parcela"** preenchendo o número da parcela e a taxa correspondente, confirmando com o ícone de check |
| **E** clica no botão **"Salvar"** para concluir o cadastro<br> |
| **ENTÃO** a nova bandeira e suas respectivas configurações de taxas e parcelas devem ser gravadas no sistema. |
| **E** ao clica no botão **"Salvar"** nada acontece e continua vazio com a mensagem **Nenhuma bandeira encontrada.**<br> |

| **Critérios de Aceitação** |
| --- |
| * As informações de taxas de débito, adicionais e parcelas configuradas devem ser vinculadas com sucesso ao registro da bandeira. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1C8jVC7gSKOwovdkp4g04xzEWm9ywy1Vp/view?usp=sharing |

---

### Caso de Teste 03: Consulta e Filtragem de Bandeiras de Cartão

| ID | Descrição |
| --- | --- |
| **C40-CT03** | O sistema deve executar a consulta e filtragem de bandeiras de cartão cadastradas com base nos parâmetros informados nos campos de busca. |

| **Pré-condições** |
| --- |
| O usuário deve estar na tela **Bandeiras de Cartão**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de bandeiras de cartão<br> |
| **QUANDO** informa um termo de pesquisa no campo **"Código"** ou no campo **"Nome"** (ex.: "Bandeira Azul") |
| **E** clica no botão de busca (ícone de lupa azul)<br> |
| **ENTÃO** a tabela deve ser atualizada exibindo os resultados correspondentes ou a mensagem de ausência de registros caso não localize. |

| **Critérios de Aceitação** |
| --- |
| * A busca deve filtrar com precisão os dados cadastrados, retornando a linha correspondente ou o feedback adequado na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1npVhrbMEmlaSiAXKjUViSorlnW31-EWO/view?usp=sharing |
