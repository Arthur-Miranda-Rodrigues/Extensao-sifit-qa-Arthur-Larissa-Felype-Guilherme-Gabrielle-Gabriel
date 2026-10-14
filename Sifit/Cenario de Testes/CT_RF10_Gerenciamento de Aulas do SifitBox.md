
---

# Cenário 10: Gerenciamento de Aulas do SifitBox

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo **SifitBox > Aulas** do sistema **SiFit**. O objetivo é validar as diferentes formas de interação de busca e ações da tela (busca por período digitando manualmente, busca por período selecionando no calendário, tentativa com data final anterior à inicial e o botão de gerar aulas), documentando o comportamento observado em que as ações acionadas não geram retorno ou alteração na interface (*nada acontece*).

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Aulas do SifitBox

#### Caso de Teste 01: Busca por Período Digitando a Data Manualmente

| ID | Descrição |
| --- | --- |
| **C10-CT01** | Validar a tentativa de filtragem de aulas inserindo o intervalo de datas de forma manual nos campos correspondentes. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **SifitBox - Aulas** (`/sifitbox/aulas`). |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **SifitBox - Aulas**<br> |
| **QUANDO** digitar manualmente uma nova data inicial e/ou final nos campos de período (ex.: alterando os dias ou anos pelo teclado). |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** o sistema não executa a filtragem esperada ou mantém o comportamento estático onde **nada acontece** na tela. |

| **Critérios de Aceitação** |
| --- |
| A funcionalidade de digitação manual de datas deve processar a pesquisa corretamente ou registrar o comportamento atual de ausência de resposta para ajuste futuro. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1ur0S1lqeUewf-7JjUdG8A7UQDedM6fG-/view?usp=sharing |

---

#### Caso de Teste 02: Busca por Período Selecionando as Opções de Calendário

| ID | Descrição |
| --- | --- |
| **C10-CT02** | Validar a tentativa de filtragem de aulas utilizando o componente de calendário interativo para escolha das datas. |

| **Pré-condições** |
| --- |
| Usuário posicionado na tela **SifitBox - Aulas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **SifitBox - Aulas**<br> |
| **QUANDO** clicar no ícone de calendário e selecionar os dias/meses desejados através do pop-up (ex.: navegando entre diferentes meses e anos). |
| **E** confirmar a seleção e clicar em **Buscar**<br> |
| **ENTÃO** o sistema exibe o calendário interativo, mas ao submeter a busca **nada acontece** na grade de resultados.|

| **Critérios de Aceitação** |
| --- |
| A seleção de datas via calendário deve atualizar a listagem de aulas de forma integrada e responsiva. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1UIIlC-LJzgxh4_FljfFwLVdNQu6s38rs/view?usp=sharing |

---

#### Caso de Teste 03: Validação de Data Inválida (Data Final Anterior à Inicial)

| ID | Descrição |
| --- | --- |
| **C10-CT03** | Validar o comportamento do sistema ao definir incorretamente a data final como um período cronologicamente anterior à data inicial. |

| **Pré-condições** |
| --- |
| Usuário na tela **SifitBox - Aulas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **SifitBox - Aulas**<br> |
| **QUANDO** preencher o campo de data final com uma data que acontece antes da data inicial estipulada. |
| **E** acionar o botão **Buscar**<br> |
| **ENTÃO** o sistema não bloqueia o envio com mensagem de erro de validação e **nada acontece** (ou a tela permanece inalterada sem processar a regra de negócio). |

| **Critérios de Aceitação** |
| --- |
| O sistema deve implementar validação restritiva para impedir intervalos de datas ilógicos (data fim menor que data início), exibindo feedback adequado ao utilizador. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1nk7_GCZVk_qjFUQzqTWe3PwbjEzkIzDi/view?usp=sharing |

---

#### Caso de Teste 04: Acionamento da Funcionalidade de Gerar Aulas

| ID | Descrição |
| --- | --- |
| **C10-CT04** | Validar o acionamento do botão **Gerar aulas** localizado no canto superior direito da tela. |

| **Pré-condições** |
| --- |
| Usuário na tela **SifitBox - Aulas**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **SifitBox - Aulas**<br> |
| **QUANDO** clicar no botão **Gerar aulas**<br> |
| **ENTÃO** o botão é acionado visualmente, mas **nada acontece** (nenhum modal é aberto, nenhum processo em background é disparado e a grade de aulas permanece idêntica). |

| **Critérios de Aceitação** |
| --- |
| O botão de geração de aulas deve executar o fluxo automatizado de criação de turmas/aulas ou apresentar feedback de indisponibilidade caso esteja em desenvolvimento. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1eYJda_JSQM0i3tcBcWGAhPR-JWK89ElN/view?usp=sharing |

