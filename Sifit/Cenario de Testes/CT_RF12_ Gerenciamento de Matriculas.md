
---

# Cenário 12: Gerenciamento de Matrículas

**Descrição:** Validação do módulo de gerenciamento de matrículas na operação da academia, englobando consultas por nome e código, validação de obrigatoriedade de cliente no cadastro, alteração e salvamento de observações no perfil da matrícula, e os fluxos de cancelamento e exclusão com tratamento de erros do servidor.

---

## Caso de Teste 01: Pesquisa de Matrículas por Nome e por Código

| ID | Descrição |
| --- | --- |
| **C12-CT01** | Validar a filtragem da listagem de matrículas utilizando os campos de busca por nome (ex.: "Rafaela Andrade") e por código numérico (ex.: "232"). |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SIFIT e posicionado na tela de **Matrículas** (`/matriculas`). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de Matrículas.|
| **QUANDO** preencher o campo de busca por nome (ex.: "Rafaela Andrade") ou digitar o código da matrícula (ex.: "232") e clicar em **Buscar**<br> |
| **ENTÃO** a tabela deve filtrar e apresentar com precisão apenas o(s) registro(s) correspondente(s) aos critérios informados. |

| **Critérios de aceitação** |
| --- |
| Os filtros de busca por nome e código devem retornar exatamente os registros esperados na listagem de matrículas. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1rTCdn-9jvOL6T1w9BMy0GRBqrubF90R5/view?usp=sharing |

---

## Caso de Teste 02: Validação de Obrigatoriedade de Cliente ao Cadastrar Matrícula

| ID | Descrição |
| --- | --- |
| **C12-CT02** | Garantir que o sistema bloqueie a gravação e exiba aviso quando o utilizador tentar cadastrar uma matrícula sem selecionar um cliente associado. |

| **Pré-condições** |
| --- |
| Usuário posicionado na tela de Matrículas após acionar o botão **"Cadastrar Matrícula"**. |

| **Passos** |
| --- |
| **DADO** que o usuário está no formulário de cadastro de matrícula. |
| **QUANDO** preencher os campos obrigatórios de valores, datas e taxas (ex.: Taxa de Matrícula: 200, Valor Parcela, Desconto, Valor Total). |
| **E** deixar o campo de seleção de cliente/código em branco. |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** o sistema deve interromper o processo e exibir o modal de alerta com a mensagem: *"Aviso: Selecione o cliente!"*. |

| **Critérios de aceitação** |
| --- |
| A tentativa de submeter uma nova matrícula sem vincular um cliente deve ser impedida, apresentando o alerta descritivo adequado. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1G0Xwi2bZEDgvBByJl1qFrvvK1Q6oT6g7/view?usp=sharing |

---

## Caso de Teste 03: Visualização e Edição de Observações da Matrícula

| ID | Descrição |
| --- | --- |
| **C12-CT03** | Verificar se é possível abrir os detalhes de uma matrícula existente, habilitar a edição, alterar o campo de observação e persistir as modificações. |

| **Pré-condições** |
| --- |
| Matrícula previamente cadastrada e visível na listagem principal. |

| **Passos** |
| --- |
| **DADO** que o usuário está na listagem de matrículas. |
| **QUANDO** clicar no ícone de visualização (lupa/olho) na linha de uma matrícula (ex.: Código 236). |
| **E** no modal "Visualizar Matrícula", acionar o modo de edição dos campos. |
| **E** inserir ou atualizar informações no campo de observação (ex.: digitando "lesão" ou notas de controle). |
| **E** clicar em **Salvar** e, posteriormente, em **Fechar**<br> |
| **ENTÃO** o sistema deve salvar as alterações e exibi-las corretamente atualizadas no sistema. |

| **Critérios de aceitação** |
| --- |
| A edição e salvamento do campo de observação no modal de detalhes da matrícula devem funcionar sem falhas de persistência. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1h7s-SbE9KS5FLaRu3QZDwikyaqGkBRM9/view?usp=sharing |

---

## Caso de Teste 04: Cancelamento de Matrícula Ativa

| ID | Descrição |
| --- | --- |
| **C12-CT04** | Validar o fluxo de cancelamento de uma matrícula ativa através da ação específica na listagem de registros. |

| **Pré-condições** |
| --- |
| Existir uma matrícula com status ativo na tabela (ex.: vinculada ao aluno *Rafael Santos*). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela de Matrículas. |
| **QUANDO** clicar na opção de cancelamento de matrícula na linha do registro desejado. |
| **E** no modal de confirmação ("Cancelar Matrícula"), clicar no botão de confirmação ("Confirmar"). |
| **ENTÃO** o sistema deve processar a solicitação e atualizar o status visual da matrícula para "Cancelado". |

| **Critérios de aceitação** |
| --- |
| A função de cancelamento de matrícula deve alterar o estado do registro de forma correta após a confirmação do operador. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tN4gYpZwr3xkNc7ptgtGyCn7iGhnZGvp/view?usp=sharing |

---

## Caso de Teste 05: Tratamento de Exceção na Exclusão de Matrícula

| ID | Descrição |
| --- | --- |
| **C12-CT05** | Validar o comportamento do sistema ao acionar a exclusão de um registro de matrícula na listagem, tratando eventuais falhas do servidor (*Erro no servidor*). |

| **Pré-condições** |
| --- |
| Usuário na tela de listagem de matrículas. |

| **Passos** |
| --- |
| **DADO** que o usuário localiza um registro na tabela de matrículas. |
| **QUANDO** clicar no ícone de exclusão (lixeira) e confirmar a ação no modal de aviso ("Confirmar").  |
| **ENTÃO** caso ocorra instabilidade ou restrição no backend, o sistema deve capturar a exceção e exibir o modal de erro com a mensagem: *"Erro no servidor - Erro interno inesperado"* acompanhado do botão **Fechar**. |

| **Critérios de aceitação** |
| --- |
| Erros de exclusão no servidor devem ser tratados de maneira controlada, exibindo uma interface de feedback amigável ao utilizador. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1X9xK6XSKGRbmEC3EHtsq96WgOTXHjnoK/view?usp=sharing |
