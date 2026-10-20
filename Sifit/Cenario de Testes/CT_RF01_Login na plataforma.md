

---

# Cenário 1: Login na plataforma.

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

| **Evidências** |
| --- |
| <img width="1916" height="900" alt="Caso login com sucesso" src="https://github.com/user-attachments/assets/4d35c4f7-a09c-4689-9676-7aeb94dc20f8" /> |
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

| **Evidências** |
| --- |
| <img width="1919" height="926" alt="image" src="https://github.com/user-attachments/assets/60274840-12ff-428c-ae5e-6955c90cde31" /> |
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
| <img width="1915" height="893" alt="Captura de tela 2026-10-14 221649" src="https://github.com/user-attachments/assets/1fd2c394-7fcb-4e06-b0e4-cb97e943fd28" /> |
| https://drive.google.com/file/d/15jQmL5k1DMN9DpuNNUPi9_B7Yh9MQPnx/view?usp=sharing  |
  

