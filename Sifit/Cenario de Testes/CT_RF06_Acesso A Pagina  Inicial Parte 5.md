
---

# Cenário de 5: Página Inicial (Parte 5)

### Caso de Teste 01: Acesso ao Perfil do Cliente a partir do Modal de Personais

| ID | Descrição |
| --- | --- |
| **C06-CT01** | Validar o direcionamento do modal "Personais" para a tela "Visualizar Cliente" ao clicar na ação correspondente do profissional cadastrado.

 |

| **Pré-condições** |
| --- |
| Utilizador autenticado na Página Inicial do SIFIT com o modal "Personais" aberto.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está visualizando a listagem de profissionais no modal "Personais"

 |
| **QUANDO** clicar no botão de ação "Visualizar cliente" (ícone de olho) na linha do personal selecionado (ex.: *Marcelo Longo Zandonadi*)

 |
| **ENTÃO** o sistema deve fechar o modal e direcionar o utilizador para a tela "Visualizar Cliente" com o perfil completo do profissional.

 |

| **Critérios de aceitação** |
| --- |
| O clique na ação "Visualizar cliente" dentro do modal de Personais deve abrir corretamente a página de detalhes do cliente/personal selecionado.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1L5U0OH2l2EDG-Ah_aKNJr5MXOxeP4pHu/view?usp=sharing |

---

### Caso de Teste 02: Aplicação e Finalização de Anamnese no Perfil do Cliente

| ID | Descrição |
| --- | --- |
| **C06-CT02** | Validar o fluxo de aplicação de anamnese para o aluno, selecionando o modelo disponível, preenchendo o questionário e finalizando o processo.

 |

| **Pré-condições** |
| --- |
| Utilizador na tela "Visualizar Cliente" do aluno posicionado no bloco "Anamnese".

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela "Visualizar Cliente"

 |
| **QUANDO** clicar no botão "Aplicar Anamnese" no painel de Anamnese

 |
| **E** o modal "Aplicar Anamnese" for aberto

 |
| **E** selecionar um modelo (ex.: *Triplet*) e clicar em "Iniciar"

 |
| **E** na etapa "Revisar e Finalizar", clicar em "Finalizar Anamnese"

 |
| **ENTÃO** o sistema deve salvar as respostas e registrar a anamnese concluída para o cliente.

 |

| **Critérios de aceitação** |
| --- |
| O fluxo de anamnese deve permitir a seleção de modelo, navegação entre as etapas do formulário e a finalização com sucesso.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1kfNzLepkHSXVFFA062olzSlX_v36EaP2/view?usp=sharing |

---

### Caso de Teste 03: Consulta ao Histórico Completo de Presenças do Cliente

| ID | Descrição |
| --- | --- |
| **C06-CT03** | Garantir a visualização do modal de histórico de presenças a partir do painel de desempenho do cliente.

 |

| **Pré-condições** |
| --- |
| Utilizador na tela "Visualizar Cliente" do aluno.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela "Visualizar Cliente"

 |
| **E** visualiza a seção "Resumo do desempenho"

 |
| **QUANDO** clicar no botão "Ver histórico completo"

 |
| **ENTÃO** o sistema deve exibir o modal "Histórico de presenças" contendo as entradas do aluno ou a mensagem explicativa quando não houver registros.

 |

| **Critérios de aceitação** |
| --- |
| O modal de histórico de presenças deve abrir corretamente exibindo os registros de entrada do aluno ou o estado vazio correspondente.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/15JutYTkA5feIDt5d2zQWtdZ-UsUHNZmR/view?usp=sharing |

---

### Caso de Teste 04: Validação de Registro de Pagamento sem Pendências Financeiras

| ID | Descrição |
| --- | --- |
| **C06-CT04** | Validar o comportamento do modal "Registrar pagamento" através das Ações Rápidas do cliente quando o aluno não possui contas pendentes.

 |

| **Pré-condições** |
| --- |
| Utilizador na tela "Visualizar Cliente" de um aluno sem mensalidades ou débitos em aberto.

 |

| **Passos** |
| --- |
| **DADO** que o utilizador está na tela "Visualizar Cliente"

 |
| **E** localiza o painel lateral de "Ações rápidas"

 |
| **QUANDO** clicar na opção "Registrar pagamento"

 |
| **ENTÃO** o sistema deve abrir o modal "Registrar pagamento" e exibir a mensagem informando que o aluno não possui pendências (ex.: *"Nenhuma conta pendente encontrada - Este aluno não possui mensalidades pendentes para recebimento."*).

 |

| **Critérios de aceitação** |
| --- |
| O modal de pagamento deve validar o status financeiro do aluno e alertar adequadamente quando não houver títulos a receber.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1qxgAm1SSvoi2gJN-eKXkLcg0Sn8CMTli/view?usp=sharing |
