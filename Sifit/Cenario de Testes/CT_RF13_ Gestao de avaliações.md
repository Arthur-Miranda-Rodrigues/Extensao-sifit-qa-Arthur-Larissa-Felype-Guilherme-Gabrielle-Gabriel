---

## Cenário 13: Gerenciamento de Avaliações Físicas

## Caso de Teste 01: Filtros de Busca e Indicadores na Listagem de Avaliações
---

| ID | Descrição |
| --- | --- |
| **C13-CT01** | Validar os filtros por Código, Nome e Status (Todos / Pendente / Realizado) e a exibição dos indicadores no topo da tela "Avaliações". |

| **Pré-condições** |
| --- |
| Usuário autenticado e posicionado na tela "Avaliações" (menu lateral), com avaliações pendentes e realizadas cadastradas. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Avaliações" e visualiza os indicadores "Avaliação no Mês", "Mês Passado" e "Média Mensal" |
| **QUANDO** digitar um nome no campo "Nome" (ex.: "Marcelo Longo Zandonadi") e clicar em "Buscar" |
| **ENTÃO** a tabela deve exibir somente as avaliações desse aluno |
| **E QUANDO** informar um código no campo "Código" e clicar em "Buscar" |
| **ENTÃO** a tabela deve exibir apenas a avaliação correspondente ao código |
| **E QUANDO** abrir o campo "Status", escolher uma das opções ("Todos", "Pendente" ou "Realizado") e clicar em "Buscar" |
| **ENTÃO** a tabela deve listar somente as avaliações com o status selecionado (ex.: "Realizado" exibe apenas linhas com o selo verde "REALIZADO"). |

| **Critérios de aceitação** |
| --- |
| A listagem deve ser filtrada de acordo com o código, nome ou status informados, e os indicadores do topo devem ser exibidos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1GzFSkiPYJp2B7jHmFxCPelhPwI07ibEl/view?usp=sharing |

---

## Caso de Teste 02: Cadastro de Avaliação com Busca de Aluno e Seleção do Personal

| ID | Descrição |
| --- | --- |
| **C13-CT02** | Validar o fluxo do modal "Cadastrar Avaliação": busca do aluno por código ou nome, seleção do personal responsável, data e hora. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela "Avaliações"; alunos e personais cadastrados no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Avaliações" |
| **QUANDO** clicar em "Cadastrar Avaliação" |
| **ENTÃO** o modal deve exibir o funcionário cadastrante (ex.: 11 – Jair), a data de lançamento (12/10/2026) e os campos "Aluno" (Código e Nome) e "Selecione o personal responsável" (Personal, Data e Hora) |
| **E QUANDO** clicar no botão de lupa ao lado do aluno |
| **ENTÃO** deve abrir o modal "Buscar Aluno" com o seletor "Tipo de Pesquisa" (Código / Nome), o campo "Pesquisa" e a lista de alunos com o botão "Selecionar" |
| **E QUANDO** pesquisar por código (ex.: "68") ou selecionar um aluno da lista (ex.: código 5 – Mátila Rhana Alves Feitosa) |
| **ENTÃO** o código e o nome do aluno devem ser preenchidos automaticamente no cadastro |
| **E QUANDO** escolher o personal no campo "Personal" (opções: Gabriella, Santhago, Vinicius), definir data e hora e clicar em "Salvar" |
| **ENTÃO** a avaliação deve ser registrada e o usuário deve retornar à listagem com o indicador "Avaliação no Mês" atualizado. |

| **Critérios de aceitação** |
| --- |
| O sistema deve permitir localizar o aluno, selecioná-lo, informar o personal, data e hora e concluir o cadastro da avaliação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1eDHQUO1sXqc3Rf2Jx6bPcJaqvyd26kfS/view?usp=sharing |

---

## Caso de Teste 03: Validação dos Campos Obrigatórios no Cadastro de Avaliação

| ID | Descrição |
| --- | --- |
| **C13-CT03** | Verificar as mensagens de aviso ao tentar salvar a avaliação sem aluno, sem personal ou sem hora. |

| **Pré-condições** |
| --- |
| Modal "Cadastrar Avaliação" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário está no modal "Cadastrar Avaliação" |
| **QUANDO** clicar em "Salvar" sem selecionar o aluno |
| **ENTÃO** o sistema deve exibir o aviso "Selecione um aluno." com o botão "Entendi" |
| **E QUANDO** abrir "Buscar Aluno" e pesquisar por nome sem resultado |
| **ENTÃO** a lista deve exibir "Nenhum aluno encontrado." |
| **E QUANDO** selecionar o aluno, não escolher o personal e clicar em "Salvar" |
| **ENTÃO** o sistema deve exibir o aviso "Selecione o personal responsável." |
| **E QUANDO** escolher o personal, deixar a hora em "00:00" sem preencher e clicar em "Salvar" |
| **ENTÃO** o sistema deve exibir o aviso "Informe a hora da avaliação." |

| **Critérios de aceitação** |
| --- |
| O cadastro não deve ser concluído enquanto aluno, personal e hora não forem informados, e cada ausência deve gerar o aviso correspondente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DRwKU8DjIcf1Y2W6hqIyrQYFX6raTZLw/view?usp=sharing |

---

## Caso de Teste 04: Preenchimento de Circunferências, Subcutâneas e Composição Corporal

| ID | Descrição |
| --- | --- |
| **C13-CT04** | Validar o lançamento das medidas em centímetros e milímetros e a exibição automática da aba "Composição" na avaliação de um aluno. |

| **Pré-condições** |
| --- |
| Existir avaliação realizada na listagem (ex.: Mona Liza); modal "Avaliação de [aluno] – Dados da avaliação corporal e medidas" aberto. |

| **Passos** |
| --- |
| **DADO** que o usuário abriu a avaliação do aluno e acessou a aba "Circunferências" |
| **QUANDO** informar/alterar as medidas em cm (Ombro, Tórax, Cintura, Quadril, Abdomen, Coxa Direita/Esquerda, Braço Direito/Esquerdo, Antebraço Direito/Esquerdo, Panturrilha Dir.) |
| **E** acessar a aba "Subcutâneas" e informar as dobras em mm (Bíceps, Tríceps, Subescapular, Supra-ilíaca, Tórax, Axilar Média, Abdominal, Coxa, Panturrilha) |
| **E** acessar a aba "Composição" |
| **ENTÃO** o sistema deve exibir IMC, Densidade Corporal, % de Gordura, Peso da Gordura, Peso em Excesso, Resultado % de Gordura e a Classificação Visual coerentes com os dados informados. |

| **Critérios de aceitação** |
| --- |
| As medidas devem ser aceitas e os indicadores da aba "Composição" devem ser calculados e classificados de forma consistente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1yIEklGcQNw3Cc8v-e9_UPLAEYJrIRdVT/view?usp=sharing |

---

## Caso de Teste 05: Alteração de Data e Hora de uma Avaliação Pendente

| ID | Descrição |
| --- | --- |
| **C13-CT05** | Validar o modal "Alterar Data / Hora da avaliação" para uma avaliação com status Pendente. |

| **Pré-condições** |
| --- |
| Existir avaliação com status "PENDENTE" (ex.: Lurdes Gabrielly – 07/11/2026 07:30). |

| **Passos** |
| --- |
| **DADO** que o usuário acionou a ação de alterar data/hora na linha da avaliação pendente |
| **QUANDO** o modal exibir a data e a hora atuais da avaliação |
| **E** informar a "Nova Data" (ex.: 19/10/2026) e a "Nova Hora" (ex.: 7:00) |
| **E** clicar em "Salvar" |
| **ENTÃO** o sistema deve fechar o modal e a listagem deve apresentar a avaliação com a nova data e hora. |

| **Critérios de aceitação** |
| --- |
| A nova data/hora informada deve ser persistida e refletida na listagem. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1hHRLjP7s7nbUKiq2rVbNZ7NuxxhOvSIj/view?usp=sharing |

---

## Caso de Teste 06: Registro de IMC e Conclusão de Avaliação Pendente

| ID | Descrição |
| --- | --- |
| **C13-CT06** | Validar o preenchimento da aba "IMC" (idade, altura e peso) em uma avaliação pendente e a mudança de status ao salvar. |

| **Pré-condições** |
| --- |
| Existir avaliação com status "PENDENTE" (ex.: Lurdes Gabrielly). |

| **Passos** |
| --- |
| **DADO** que o usuário abriu a avaliação pendente e está na aba "IMC" |
| **QUANDO** informar Idade (27), Altura (1,80) e Peso (68 e depois 68,9) |
| **E** clicar em "Salvar" |
| **ENTÃO** o sistema deve calcular o IMC, salvar a avaliação e alterar o status para "REALIZADO" na listagem. |

| **Critérios de aceitação** |
| --- |
| Após informar altura e peso e salvar, o IMC deve ser calculado e a avaliação deve passar a "REALIZADO". |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1L49K38IjbDTWb1ZzaJw9g-j8JLeKQ_j1/view?usp=sharing |

---

## Caso de Teste 07: Comparação entre Avaliações

| ID | Descrição |
| --- | --- |
| **C13-CT07** | Validar o modal "Comparar Avaliação" entre uma avaliação antiga e uma nova do mesmo aluno. |

| **Pré-condições** |
| --- |
| Existir avaliação realizada (ex.: Rhanielly Gabrielly Oliveira – 29/10/2026 17:31). |

| **Passos** |
| --- |
| **DADO** que o usuário acionou a ação de comparar na linha da avaliação realizada |
| **QUANDO** selecionar "Avaliação Antiga" e "Avaliação Nova" nos campos de data |
| **E** clicar em "Comparar" |
| **ENTÃO** o sistema deve exibir a comparação com as colunas das duas datas e a "Diferença" (Idade, Altura, Peso, IMC, Resultado, % Massa Magra, Massa Gorda, % Gordura) |
| **E QUANDO** navegar pelas abas "Circunferência", "Subcutânea" e "Composição Corporal" |
| **ENTÃO** cada aba deve exibir os dados comparativos correspondentes |
| **E QUANDO** clicar em "Fechar" |
| **ENTÃO** o modal deve ser fechado e o usuário retornar à listagem. |

| **Critérios de aceitação** |
| --- |
| A comparação deve apresentar os valores das duas avaliações e a diferença entre eles em todas as abas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KTLbavxMGWXBPCgc4r3pyKLA2XWZ8b34/view?usp=sharing |

---

## Caso de Teste 08: Visualização Detalhada da Avaliação Física

| ID | Descrição |
| --- | --- |
| **C13-CT08** | Validar a página "Sua Avaliação Física" com dados pessoais, nível de gordura, composição corporal, índices e gráficos. |

| **Pré-condições** |
| --- |
| Existir avaliação realizada (ex.: Rhanielly Gabrielly Oliveira). |

| **Passos** |
| --- |
| **DADO** que o usuário acionou a visualização da avaliação realizada |
| **QUANDO** a página "Sua Avaliação Física" for carregada |
| **ENTÃO** o sistema deve exibir data da avaliação, método utilizado (Pollock 7 dobras), dados pessoais (idade, sexo, altura e peso), "Seu nível de gordura corporal" e "Composição Corporal" (% de gordura, massa gorda, massa óssea e água corporal) |
| **E** exibir a tabela "Índices Corporais" (IMC, Taxa Metabólica Basal, Relação Cintura/Quadril, Percentual de Gordura, Massa Muscular), os "Gráficos Complementares", "Dobras Cutâneas", "Classificação" e os botões de imprimir e "Compartilhar". |

| **Critérios de aceitação** |
| --- |
| Todas as seções devem ser carregadas com os dados da avaliação e os gráficos devem ser renderizados. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ECa62YoTpXKJUUWPf0c5JQnKpqpmOD6S/view?usp=sharing |

---

## Caso de Teste 09: Download do PDF da Avaliação Completa

| ID | Descrição |
| --- | --- |
| **C13-CT09** | Validar a geração e o download do relatório "avaliação completa" em PDF pelo botão verde da linha. |

| **Pré-condições** |
| --- |
| Existir avaliação realizada na listagem (ex.: Lurdes Gabrielly). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de avaliações |
| **QUANDO** clicar no botão verde de documento na linha da avaliação realizada |
| **ENTÃO** o navegador deve baixar o arquivo "avaliacao-completa-[Nome].pdf" |
| **E** ao abrir o PDF, devem constar as seções do relatório (composição, "3. Dobras Subcutâneas (mm)" com o protocolo de 7 dobras Jackson & Pollock, "4. Evolução (últimas avaliações)") e a assinatura do profissional responsável. |

| **Critérios de aceitação** |
| --- |
| O PDF deve ser gerado, baixado e aberto com os dados da avaliação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1cm1mZp_zN-TmF99RXZmMeC5C-ZMbjhI_/view?usp=sharing |

---

## Caso de Teste 10: Impressão do Relatório "Avaliação Física"

| ID | Descrição |
| --- | --- |
| **C13-CT10** | Validar o relatório "Avaliação Física" (Dados Básicos, Circunferências, Dobras Subcutâneas e Composição Corporal) aberto pela ação de impressão da linha. |

| **Pré-condições** |
| --- |
| Existir avaliação realizada na listagem (ex.: Lurdes Gabrielly). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de avaliações |
| **QUANDO** clicar na ação de impressão (ícone da impressora) da avaliação realizada |
| **ENTÃO** o sistema deve abrir o PDF "Avaliação Física" com Dados Básicos (nome, data de nascimento, altura, sexo, idade, peso, IMC e resultado), Medidas de Circunferência, Dobras Subcutâneas e Fracionamento da Composição Corporal. |

| **Critérios de aceitação** |
| --- |
| O relatório deve refletir fielmente os dados registrados na avaliação. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/19_uPyC-KLr65QY5S4uAatzAAIEwBNglL/view?usp=sharing |

---

## Caso de Teste 11: Exclusão de Avaliação

| ID | Descrição |
| --- | --- |
| **C13-CT11** | Validar a exclusão de uma avaliação mediante confirmação no modal. |

| **Pré-condições** |
| --- |
| Existir ao menos uma avaliação cadastrada (ex.: #92 – Raquel Dodge). |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de avaliações |
| **QUANDO** clicar no ícone de lixeira da linha da avaliação |
| **ENTÃO** o sistema deve exibir o modal com a mensagem "Deseja deletar esta avaliação?" e os botões "Cancelar" e "Confirmar" |
| **E QUANDO** clicar em "Confirmar" |
| **ENTÃO** a listagem deve ser recarregada e a avaliação não deve mais aparecer na tabela. |

| **Critérios de aceitação** |
| --- |
| O sistema deve exigir confirmação antes de excluir e remover o registro da listagem após confirmar. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1JXkJnodSZw_3--Seza_O0tMdzP5jfpiA/view?usp=sharing |



