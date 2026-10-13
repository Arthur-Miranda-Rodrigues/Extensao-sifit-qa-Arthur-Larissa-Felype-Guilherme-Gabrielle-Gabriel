

---

## Cenário de teste: Aplicação de Fichas de Anamnese no sistema SIFIT

### Caso de Teste 01: Buscar aluno para aplicação de anamnese

| ID | Descrição |
| --- | --- |
| C14-CT01 | O sistema deve filtrar e exibir os alunos correspondentes ao nome informado no modal de seleção. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado e na tela **Fichas de Anamnese**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela "Fichas de Anamnese"

 |
| **E** clica no botão "Nova Anamnese" no canto superior direito

 |
| **QUANDO** digita o nome do aluno no campo "Nome do aluno" (ex: "Rhaniely")

 |
| **E** clica no botão de busca (ícone de lupa)

 |
| **ENTÃO** o sistema deve listar o aluno encontrado para seleção.

 |

| **Critérios de aceitação** |
| --- |
| Caso o aluno não exista, deve ser exibida a mensagem "Nenhum aluno encontrado". Ao encontrar o aluno, suas informações devem ser apresentadas com uma seta de seleção.

 |

---

### Caso de Teste 02: Selecionar modelo de anamnese e preencher respostas

| ID | Descrição |
| --- | --- |
| C14-CT02 | O sistema deve permitir a seleção de um modelo de anamnese e o preenchimento de suas perguntas. |

| **Pré-condições** |
| --- |
| O aluno deve ser selecionado no modal "Aplicar Anamnese".

 |

| **Passos** |
| --- |
| **DADO** que o usuário selecionou o aluno (ex: "Rhaniely Gabriely Oliveira") e avançou para a etapa "Selecionar Modelo"

 |
| **E** escolhe um modelo de anamnese disponível (ex: "Esteira") e clica em "Iniciar"

 |
| **QUANDO** digita a resposta da pergunta exibida (ex: "2") no campo "Digite sua resposta aqui..."

 |
| **ENTÃO** o sistema exibe o indicador "Resposta registrada" abaixo do campo de texto.

 |

| **Critérios de aceitação** |
| --- |
| O sistema deve aceitar e registrar as respostas inseridas no formulário dinâmico.

 |

---

### Caso de Teste 03: Salvar rascunho da anamnese em andamento

| ID | Descrição |
| --- | --- |
| C14-CT03 | O sistema deve permitir que o progresso da anamnese seja salvo como rascunho. |

| **Pré-condições** |
| --- |
| O usuário deve estar no processo de preenchimento ou revisão da anamnese.

 |

| **Passos** |
| --- |
| **DADO** que o usuário preencheu ou editou uma resposta na anamnese

 |
| **QUANDO** clica no botão "Salvar rascunho" no canto inferior esquerdo do modal

 |
| **ENTÃO** o botão exibe temporariamente o status "Salvando..."

 |
| **E** em seguida retorna ao estado "Salvar rascunho", garantindo a gravação do progresso sem finalizar a ficha.

 |

| **Critérios de aceitação** |
| --- |
| Os dados preenchidos até o momento devem ser gravados sem concluir formalmente o status da anamnese.

 |

---

### Caso de Teste 04: Revisar e finalizar a ficha de anamnese

| ID | Descrição |
| --- | --- |
| C14-CT04 | O sistema deve permitir a revisão das respostas antes de concluir definitivamente a anamnese. |

| **Pré-condições** |
| --- |
| As perguntas obrigatórias do modelo de anamnese devem estar respondidas.

 |

| **Passos** |
| --- |
| **DADO** que o usuário respondeu às perguntas do modelo

 |
| **E** clica no botão "Revisar"

 |
| **E** visualiza a tela "Revisar e Finalizar" com a síntese das respostas inseridas

 |
| **QUANDO** clica no botão "Finalizar Anamnese"

 |
| **ENTÃO** o modal é encerrado e a anamnese é concluída no sistema.

 |

| **Critérios de aceitação** |
| --- |
| A anamnese finalizada deve ser salva e contabilizada nos cards de indicadores da tela "Fichas de Anamnese".

 |

 https://jam.dev/c/116c178d-30f4-43ed-b9d8-8aaf8ffb0864
