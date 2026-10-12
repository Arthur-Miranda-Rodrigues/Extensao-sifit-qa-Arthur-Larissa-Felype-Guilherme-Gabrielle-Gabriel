---

# Cenário de Testes: Gerenciamento de Avaliações Físicas

**Descrição:** Validação do módulo de Avaliações do SIFIT, contemplando filtros de busca e indicadores da listagem, cadastro de avaliação (busca de aluno e seleção do personal), validações de campos obrigatórios, preenchimento das medidas (IMC, Circunferências, Subcutâneas e Composição Corporal), alteração de data/hora, comparação entre avaliações, visualização detalhada, geração de PDF/impressão e exclusão de registros.

---

## Caso de Teste 01: Filtros de Busca e Indicadores na Listagem de Avaliações

| ID | Descrição |
| --- | --- |
| **RF06-CT01** | Validar os filtros por Código, Nome e Status (Todos / Pendente / Realizado) e a exibição dos indicadores no topo da tela "Avaliações". |

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

| **Resultado obtido** |
| --- |
| Os três filtros retornaram apenas os registros correspondentes (nome → 3 avaliações do aluno; código → 1 avaliação; status "Realizado" → somente realizadas). |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1GzFSkiPYJp2B7jHmFxCPelhPwI07ibEl/view?usp=sharing |

---

## Caso de Teste 02: Cadastro de Avaliação com Busca de Aluno e Seleção do Personal

| ID | Descrição |
| --- | --- |
| **RF06-CT02** | Validar o fluxo do modal "Cadastrar Avaliação": busca do aluno por código ou nome, seleção do personal responsável, data e hora. |

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

| **Resultado obtido** |
| --- |
| A busca e a seleção do aluno funcionaram; o modal foi concluído e o indicador "Avaliação no Mês" passou de 1 para 2. |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1eDHQUO1sXqc3Rf2Jx6bPcJaqvyd26kfS/view?usp=sharing |

---

## Caso de Teste 03: Validação dos Campos Obrigatórios no Cadastro de Avaliação

| ID | Descrição |
| --- | --- |
| **RF06-CT03** | Verificar as mensagens de aviso ao tentar salvar a avaliação sem aluno, sem personal ou sem hora. |

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

| **Resultado obtido** |
| --- |
| Os três avisos foram exibidos na ordem esperada (aluno → personal → hora) e o cadastro não foi concluído. |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DRwKU8DjIcf1Y2W6hqIyrQYFX6raTZLw/view?usp=sharing |

---

## Caso de Teste 04: Preenchimento de Circunferências, Subcutâneas e Composição Corporal

| ID | Descrição |
| --- | --- |
| **RF06-CT04** | Validar o lançamento das medidas em centímetros e milímetros e a exibição automática da aba "Composição" na avaliação de um aluno. |

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

| **Resultado obtido** |
| --- |
| As medidas foram aceitas e a composição foi calculada (Densidade 1,06 g/cm³; 15,89%; Peso da Gordura 11,92 kg; Peso em Excesso 9,11 kg; Resultado "Muito Bom"). **Inconsistência:** o IMC aparece como 0,00 kg/m² e a Classificação Visual indica "Abaixo do Peso" ao mesmo tempo em que o resultado de gordura é "Muito Bom". |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (inconsistência de IMC/classificação) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1yIEklGcQNw3Cc8v-e9_UPLAEYJrIRdVT/view?usp=sharing |

---

## Caso de Teste 05: Alteração de Data e Hora de uma Avaliação Pendente

| ID | Descrição |
| --- | --- |
| **RF06-CT05** | Validar o modal "Alterar Data / Hora da avaliação" para uma avaliação com status Pendente. |

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

| **Resultado obtido** |
| --- |
| Os campos aceitaram os valores digitados, porém, após "Salvar", o modal permaneceu aberto e a avaliação continuou listada com 07/11/2026 07:30 nas gravações seguintes. A hora "7:00" também foi aceita sem formato fixo. |

| **Status** |
| --- |
| FALHOU (a confirmar: alteração não refletida na listagem) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1hHRLjP7s7nbUKiq2rVbNZ7NuxxhOvSIj/view?usp=sharing |

---

## Caso de Teste 06: Registro de IMC e Conclusão de Avaliação Pendente

| ID | Descrição |
| --- | --- |
| **RF06-CT06** | Validar o preenchimento da aba "IMC" (idade, altura e peso) em uma avaliação pendente e a mudança de status ao salvar. |

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

| **Resultado obtido** |
| --- |
| O campo "IMC kg/m²" permaneceu vazio durante o preenchimento (não houve cálculo em tempo real); após "Salvar", a avaliação passou para "REALIZADO" e o IMC (21,27) apareceu nas telas seguintes. |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (IMC só calculado após salvar) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1L49K38IjbDTWb1ZzaJw9g-j8JLeKQ_j1/view?usp=sharing |

---

## Caso de Teste 07: Comparação entre Avaliações

| ID | Descrição |
| --- | --- |
| **RF06-CT07** | Validar o modal "Comparar Avaliação" entre uma avaliação antiga e uma nova do mesmo aluno. |

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

| **Resultado obtido** |
| --- |
| Aba IMC exibida com diferença 0,00 (única avaliação disponível comparada com ela mesma: peso 68,9; IMC 21,27; Peso Normal). A aba "Circunferência" apareceu em branco no momento da navegação. O modal fechou normalmente. |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (aba Circunferência sem conteúdo; só havia uma avaliação para comparar) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1KTLbavxMGWXBPCgc4r3pyKLA2XWZ8b34/view?usp=sharing |

---

## Caso de Teste 08: Visualização Detalhada da Avaliação Física

| ID | Descrição |
| --- | --- |
| **RF06-CT08** | Validar a página "Sua Avaliação Física" com dados pessoais, nível de gordura, composição corporal, índices e gráficos. |

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

| **Resultado obtido** |
| --- |
| Página carregada com os dados da avaliação (27 anos, feminino, 1,80 m, 68,90 kg; % de gordura 2,66%; IMC 21,27 – Normal; TMB 1525 kcal; Massa Muscular 67,07 kg) e gráficos exibidos. Observações: RCQ 0,00 ("Baixo") e dobras com soma 0 mm por falta de medidas; nível de gordura "Abaixo" convive com classificação "Excelente". |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ECa62YoTpXKJUUWPf0c5JQnKpqpmOD6S/view?usp=sharing |

---

## Caso de Teste 09: Download do PDF da Avaliação Completa

| ID | Descrição |
| --- | --- |
| **RF06-CT09** | Validar a geração e o download do relatório "avaliação completa" em PDF pelo botão verde da linha. |

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

| **Resultado obtido** |
| --- |
| Download concluído (14,2 KB) e PDF aberto com 1 página; a evolução indicou "Primeira avaliação registrada" e o relatório foi assinado por Santhago. |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1cm1mZp_zN-TmF99RXZmMeC5C-ZMbjhI_/view?usp=sharing |

---

## Caso de Teste 10: Impressão do Relatório "Avaliação Física"

| ID | Descrição |
| --- | --- |
| **RF06-CT10** | Validar o relatório "Avaliação Física" (Dados Básicos, Circunferências, Dobras Subcutâneas e Composição Corporal) aberto pela ação de impressão da linha. |

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

| **Resultado obtido** |
| --- |
| PDF aberto com os dados básicos (1,80 m; 27 anos; 68,90 kg; IMC 21,27 – Peso Normal) e fracionamento (Densidade 1,09354; 2,66% de gordura; Peso Ideal 89,42 kg). Circunferências exibidas como "0 cm" e dobras como "- mm" (não preenchidas). O campo "Resultado Gordura" aparece como "Muito Bom", enquanto o relatório do CT09 e a tela do CT08 indicam "Abaixo". |

| **Status** |
| --- |
| PASSOU COM OBSERVAÇÃO (divergência na classificação de gordura entre relatórios) |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/19_uPyC-KLr65QY5S4uAatzAAIEwBNglL/view?usp=sharing |

---

## Caso de Teste 11: Exclusão de Avaliação

| ID | Descrição |
| --- | --- |
| **RF06-CT11** | Validar a exclusão de uma avaliação mediante confirmação no modal. |

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

| **Resultado obtido** |
| --- |
| O modal de confirmação foi exibido, a tabela passou por carregamento e a avaliação #92 deixou de ser listada. |

| **Status** |
| --- |
| PASSOU |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1JXkJnodSZw_3--Seza_O0tMdzP5jfpiA/view?usp=sharing |



