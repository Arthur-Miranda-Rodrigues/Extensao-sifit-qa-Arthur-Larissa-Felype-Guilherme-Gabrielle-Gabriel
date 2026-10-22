## Cenário 1: Login na plataforma

### Caso de Teste 01: Login com as credenciais válidas.

| ID | Descrição |
| --- | --- |
| **C01-CT01** | O login será realizado com um nome de usuário e uma senha válidos na plataforma SIFIT. |

| **Pré-condições** |
| --- |
| As credenciais fornecidas (`marcelo_zandonadi` / senha) devem ser válidas e cadastradas no sistema. |

| **Passos** |
| --- |
| **DADO** que estamos na página de login do SIFIT |
| **E** preenchemos "marcelo_zandonadi" no campo Login |
| **E** preenchemos a senha válida no campo Senha |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** seremos redirecionados para a Página Inicial / Dashboard do sistema SIFIT |

| **Critérios de aceitação** |
| --- |
| O redirecionamento para a Página Inicial ("Bom dia, Jair!") deve ocorrer corretamente. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/12YnKA9VnajzPptMiPn6LI3pPnC87LwmF/view?usp=sharing   |


---

### Caso de Teste 02: Tentativa de login com credenciais incorretas.

| ID | Descrição |
| --- | --- |
| **C01-CT02** | O login falhará quando o nome de usuário ou a senha forem inválidos. |

| **Pré-condições** |
| --- |
| Nenhuma. |

| **Passos** |
| --- |
| **DADO** que estamos na página de login do SIFIT |
| **E** preenchemos "asfadf" no campo Login |
| **E** preenchemos "********" no campo Senha |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** uma mensagem de erro "O nome de usuário e senha não correspondem." será exibida no topo do formulário |

| **Critérios de aceitação** |
| --- |
| A mensagem de alerta "O nome de usuário e senha não correspondem." deve ser exibida ao usuário. |

| **Evidência** |
| --- |
|  https://drive.google.com/file/d/18LbwX2OkkQhCwBqHVwqWjKxsCmdd2GdA/view?usp=sharing  |

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID | Descrição |
| --- | --- |
| **C01-CT03** | O login falhará quando os campos de login e senha forem apagados ou mantidos em branco. |

| **Pré-condições** |
| --- |
| Nenhuma. |

| **Passos** |
| --- |
| **DADO** que estamos na página de login do SIFIT |
| **E** deixamos os campos Login e Senha em branco |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** o sistema deve impedir a submissão e exibir mensagens de validação solicitando o preenchimento dos campos |

| **Critérios de aceitação** |
| --- |
| Os campos obrigatórios devem impedir o acesso e exibir alertas de validação apropriados. |

| **Evidências** |
| --- |
| https://drive.google.com/file/d/15jQmL5k1DMN9DpuNNUPi9_B7Yh9MQPnx/view?usp=sharing  |

### Caso de Teste 04: Acesso à Funcionalidade de Recuperação de Senha (Extra)

| ID | Descrição |
| --- | --- |
| **C01-CT04** | O sistema deve redirecionar o usuário para a interface de recuperação/redefinição de senha ao acionar o link correspondente na tela de login. |

| **Pré-condições** |
| --- |
| O usuário deve estar na página inicial de autenticação do SIFIT. |

| **Passos** |
| --- |
| **DADO** que estamos na página de login do SIFIT |
| **QUANDO** clicamos no link "Esqueci minha senha" |
| **ENTÃO** o sistema deve direcionar o usuário para a tela ou modal de recuperação de senha da aplicação. |
| **E** nada acontece. |

| **Critérios de Aceitação** |
| --- |
| * O link de recuperação de senha deve estar funcional e direcionar o usuário para o fluxo adequado de redefinição de credenciais. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1UVEJmPtjgyMDTs_6nrJcX1i0ldW5D671/view?usp=sharing |
  

