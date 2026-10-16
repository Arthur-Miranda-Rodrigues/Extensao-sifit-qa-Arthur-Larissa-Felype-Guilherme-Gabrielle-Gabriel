
---

# Cenário 24: Gerenciamento e Filtro de Caixas no Módulo Financeiro

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 24: Gerenciamento e Filtro de Caixas** no sistema **SiFit**. O objetivo é validar as operações de abertura de caixa, filtros por status e período, visualização de entradas e saídas, conferência física com obrigatoriedade de motivo, tratamento de erros na busca de contas e emissão/impressão de relatórios de fechamento de caixa.

---

## 2. Cenários de Teste

### Caso de Teste 01: Abertura de Novo Caixa com Local Válido

| ID | Descrição |
| --- | --- |
| **C24-CT01** | Validar a abertura de um novo caixa selecionando um local de contas válido no sistema. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema na tela de **Caixas** e possuir permissão para abrir novos caixas. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de gerenciamento de **Caixas**<br><br> |
| **QUANDO** clicar no botão **"Abrir Caixa"**<br> |
| **E** selecionar um local válido no campo **"Local de Contas"** (ex.: "Caixa Muay Thai")  |
| **E** clicar no botão **"Salvar"**<br><br> |
| **ENTÃO** o novo caixa deve ser criado com sucesso |
| **E** exibido na listagem com o status **"ABERTO"** destacado em verde. |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve registrar a abertura do caixa vinculada ao funcionário logado e ao local escolhido. |
| * A tabela principal deve ser atualizada exibindo o novo registro com status "ABERTO". |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1NF6Hkqhb1KJKA4mdwkrULdW9Q5OExM4x/view?usp=sharing |

---

### Caso de Teste 02: Filtragem de Caixas por Status e Período

| ID | Descrição |
| --- | --- |
| **C24-CT02** | Validar a filtragem dos caixas na tabela com base no status ("Aberto" ou "Fechado") e intervalo de datas. |

| **Pré-condições** |
| --- |
| Existir registros de caixas cadastrados com diferentes status no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário visualiza a tela de **Caixas** com os filtros de data inicial, data final e status<br>|
| **QUANDO** selecionar o status desejado (ex.: "Aberto" ou "Fechado") e definir o período |
| **E** clicar no botão **"Buscar"**<br><br>  |
| **ENTÃO** a tabela deve ser atualizada exibindo apenas os registros correspondentes aos filtros aplicados. |

| **Critérios de Aceitação** |
| --- |
| * O filtro deve retornar com precisão os caixas que correspondem aos critérios informados ou exibir a mensagem "Nenhum caixa encontrado" caso não haja resultados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1QOwm8ko48pnXvWGe95BRthlFBfRjWk2-/view?usp=sharing |

---

### Caso de Teste 03: Visualização e Detalhamento de Entradas no Fechamento

| ID | Descrição |
| --- | --- |
| **C24-CT03** | Validar a visualização detalhada das entradas financeiras ao acessar a aba **Ver Entradas** no painel de fechamento do caixa. |

| **Pré-condições** |
| --- |
| O usuário estar na tela de **Caixas** e clicar no ícone de detalhes/fechamento de um caixa cadastrado. |

| **Passos** |
| --- |
| **DADO** que o usuário abre o painel de fechamento do caixa e seleciona o local correspondente (ex: "Caixa Academia")

<br> |
| **QUANDO** clicar no botão **"Ver Entradas"**<br><br> |
| **ENTÃO** o sistema deve carregar e exibir os dados consolidados e o detalhamento das entradas vinculadas ao período e local de contas. |

| **Critérios de Aceitação** |
| --- |
| * O painel deve listar corretamente as entradas financeiras e calcular os totais esperados para o caixa. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1M3JxZGAHXqLbdVFgB3Qzj9ZLzcOpC_EZ/view?usp=sharing |

---

### Caso de Teste 04: Visualização e Detalhamento de Saídas no Fechamento

| ID | Descrição |
| --- | --- |
| **C24-CT04** | Validar a visualização detalhada das saídas/despesas ao acessar a aba **Ver Saídas** no painel de fechamento do caixa. |

| **Pré-condições** |
| --- |
| O usuário estar visualizando o painel de fechamento de caixa e alternar para o local de contas desejado (ex: "Caixa Muay Thai"). |

| **Passos** |
| --- |
| **DADO** que o usuário está no painel de fechamento de caixa<br> |
| **QUANDO** clicar no botão **"Ver Saídas"**<br><br> |
| **ENTÃO** o sistema deve exibir os valores referentes a despesas, fornecedores, salários e demais saídas registradas no período. |

| **Critérios de Aceitação** |
| --- |
| * O total de saídas e suas respectivas categorias devem ser apresentados adequadamente na interface. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1EumBw1mRjqOgMhh0F3fk24NJiU9mh4Hy/view?usp=sharing |

---

### Caso de Teste 05: Validação e Registro de Conferência Física de Caixa (Com Motivo Obrigatório)

| ID | Descrição |
| --- | --- |
| **C24-CT05** | Validar que o sistema obriga o preenchimento do campo **"Motivo"** ao registrar uma divergência na conferência física do caixa. |

| **Pré-condições** |
| --- |
| O usuário estar posicionado no painel de fechamento de caixa e acionar a opção de conferência. |

| **Passos** |
| --- |
| **DADO** que o usuário clica em **"Informar valor contado"** e insere o valor físico gerando diferença de saldo<br> |
| **QUANDO** tentar clicar em **"Registrar Conferência"** sem preencher o campo **"Motivo"**<br> |
| **ENTÃO** o sistema exibe um aviso de alerta solicitando a inclusão do motivo <br> |
| **DADO** que o usuário fecha o aviso, preenche o campo **"Motivo"** e clica em **"Registrar Conferência"** novamente<br> |
| **ENTÃO** a conferência é salva com sucesso, exibindo mensagem de confirmação.|

| **Critérios de Aceitação** |
| --- |
| * A conferência só é concluída e gravada com sucesso após o preenchimento de uma justificativa válida no campo motivo. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1D2vdCLqQ1EHUMnbm0_raP5tVUB7p6NRs/view?usp=sharing |

---

### Caso de Teste 06: Tratamento de Erro na Busca de Contas com Parâmetros Inválidos

| ID | Descrição |
| --- | --- |
| **C24-CT06** | Validar o comportamento do sistema ao tentar buscar contas com parâmetros ou locais que gerem conflito na janela de fechamento de caixa.|

| **Pré-condições** |
| --- |
| O usuário estar na janela modal de fechamento de caixa.|

| **Passos** |
| --- |
| **DADO** que o usuário ajusta os parâmetros de data ou seleciona um local de contas de teste/inválido<br>|
| **QUANDO** clicar no botão **"Buscar Contas"**<br><br>  |
| **ENTÃO** o sistema deve identificar a inconsistência e exibir uma mensagem de erro ("Erro: Erro ao buscar contas"). |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve tratar falhas de busca de contas informando claramente o usuário por meio de pop-up de erro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1vyBD4X36a7QDvDsLktQFzKYjN7vO15yb/view?usp=sharing |

---

### Caso de Teste 07: Impressão / Emissão do Relatório de Fechamento de Caixa

| ID | Descrição |
| --- | --- |
| **C24-CT07** | Validar a funcionalidade de geração e impressão do relatório oficial de fechamento de caixa em formato PDF. |

| **Pré-condições** |
| --- |
| O usuário estar visualizando os detalhes de um caixa fechado/conferido na listagem principal. |

| **Passos** |
| --- |
| **DADO** que o usuário clica no ícone de relatório/impressão na coluna de Ações correspondente<br>|
| **QUANDO** o sistema abrir a pré-visualização do documento de **Relatório de Fechamento de Caixa**<br> |
| **E** selecionar as opções de impressão ou salvamento em PDF e acionar **"Imprimir"**<br><br> |
| **ENTÃO** o relatório contendo o resumo financeiro, entradas, saídas e dados do operador deve ser gerado e impresso com sucesso. |

| **Critérios de Aceitação** |
| --- |
| * O relatório gerado deve conter todas as informações consolidadas do caixa selecionado sem falhas de formatação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1SwYWWnkaBmViE8A8wtdoKl5o9cW7DvdA/view?usp=sharing |
