## Cenário 50: Alternância de Tema da Interface (Claro / Escuro)

### Caso de Teste 01: Alternância para o Tema Escuro (Dark Mode)

| ID | Descrição |
| --- | --- |
| **C50-CT01** | Validar a alteração do tema visual da interface do modo Claro para o modo Escuro. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT, posicionado na tela do módulo **Aplicativo** (`/aplicativo`) com a interface em modo Claro. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela do **Aplicativo** com o tema Claro ativo.<br> |
| **QUANDO** clicar no botão **"Escuro"** do cabeçalho.<br> |
| **ENTÃO** a interface deve aplicar imediatamente o esquema de cores escuro, alterando o fundo da página, os cards, as tabelas e os textos.<br> |
| **E** o botão **"Escuro"** deve ficar destacado como opção ativa, com o seletor do menu lateral refletindo o mesmo estado. |

| **Critérios de Aceitação** |
| --- |
| As cores de fundo, cards, tabelas, menus e textos devem mudar imediatamente para o padrão escuro, sem recarregar a página e mantendo a legibilidade do conteúdo. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1DsVebJeP_qkUDGnHqzXE7el8buGOz9H1/view?usp=sharing |

---

### Caso de Teste 02: Alternância para o Tema Claro (Light Mode)

| ID | Descrição |
| --- | --- |
| **C50-CT02** | Validar o retorno da interface do modo Escuro para o modo Claro. |

| **Pré-condições** |
| --- |
| O usuário deve estar autenticado no SIFIT, posicionado na tela do módulo **Aplicativo** (`/aplicativo`) com a interface em modo Escuro. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela do **Aplicativo** com o tema Escuro ativo.<br> |
| **QUANDO** clicar no botão **"Claro"** do cabeçalho.<br> |
| **ENTÃO** a interface deve aplicar imediatamente o esquema de cores claro, restaurando o fundo, os cards, as tabelas e os textos ao contraste original.<br> |
| **E** o botão **"Claro"** deve ficar destacado como opção ativa, com o seletor do menu lateral refletindo o mesmo estado. |

| **Critérios de Aceitação** |
| --- |
| O layout deve ser renderizado instantaneamente na versão clara, e todos os textos e botões de ação devem manter a legibilidade adequada. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1UZvsqtUhsUy0FRVqNGc0NLelvH8lja4d/view?usp=sharing |
