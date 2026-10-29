
---

## Cenário 10: Gerenciamento de Aulas do SifitBox



### Caso de Teste 03: Validação de Data Inválida (Data Final Anterior à Inicial)

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

### Caso de Teste 04: Acionamento da Funcionalidade de Gerar Aulas

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

