
---

## Cenário de Teste: Controle de Presença e Registro de Check-in

### Caso de Teste 01: Realizar Check-in manual de presença com sucesso.

| ID | Descrição |
| --- | --- |
| C40-CT01 | O sistema deve permitir que o usuário realize o check-in do aluno com sucesso. |

| **Pré-condições** |
| --- |
| O usuário deve estar logado no sistema SiFit com acesso ao menu "Check-ins" e a opção "Controle de Presença" deve incluir "Check-in" ou "Ambos" nas Configurações. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu lateral em **Check-ins** |
| **E** visualiza a área de entrada rápida ou digita o código do aluno/cliente |
| **QUANDO** clicar no botão **Realizar check-in** (ou **+ Check-in manual**) |
| **ENTÃO** o sistema deve registrar a presença do aluno e atualizar a lista |

| **Critérios de aceitação** |
| --- |
| O registro de check-in deve ser salvo com sucesso e exibido na listagem de presenças. |

---

### Caso de Teste 02: Tentar realizar Check-in quando o controle de presença está configurado apenas como Biometria.

| ID | Descrição |
| --- | --- |
| C40-CT02 | O sistema deve ocultar ou restringir o check-in manual caso o controle seja exclusivo por Biometria. |

| **Pré-condições** |
| --- |
| A opção **Controle de Presença** no menu **Configurações > Home** deve estar definida como **Biometria**. |

| **Passos** |
| --- |
| **DADO** que o controle geral de presença está configurado como "Biometria" |
| **QUANDO** o usuário tentar acessar as rotinas de registro manual de check-in |
| **ENTÃO** o sistema deve exigir o uso da biometria ou ocultar a funcionalidade de check-in manual. |

| **Critérios de aceitação** |
| --- |
| O registro manual deve ser bloqueado/indisponível quando apenas a Biometria estiver ativada. |

---

### Caso de Teste 03: Consultar histórico de presenças e check-ins efetuados.

| ID | Descrição |
| --- | --- |
| C40-CT03 | O sistema deve permitir a consulta do histórico de presenças e check-ins. |

| **Pré-condições** |
| --- |
| Devem existir registros prévios de entrada/presença de alunos no sistema. |

| **Passos** |
| --- |
| **DADO** que o usuário acessa o menu **Presenças** ou **Check-ins** |
| **QUANDO** selecionar o período desejado no filtro de datas (Ex: DE / ATÉ) |
| **ENTÃO** o sistema deve listar todos os registros de presença/check-in correspondentes |

| **Critérios de aceitação** |
| --- |
| O sistema deve exibir os horários, nomes dos clientes e contadores de presença dentro do período selecionado. |

https://jam.dev/c/0b9ab8de-b012-49f5-aea7-4f3e7af5153c
