
---

# Cenário de teste:Alternância de Tema da Interface (Claro / Escuro)

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 19 (RF19) - Alternância de Tema da Interface** no sistema **SiFit**. O objetivo é validar o funcionamento da alteração do modo de visualização entre o tema claro e o tema escuro (Dark Mode) por meio dos botões de navegação e do painel superior.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão do Tema da Interface

#### Caso de Teste 01: Alternância para o Tema Escuro (Dark Mode)

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar a alteração do tema visual da interface do modo Claro para o modo Escuro.

 |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit com a interface em modo Claro.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está navegando no sistema SiFit com o tema Claro ativo

 |
| **QUANDO** clicar no botão/seletor de tema escuro (ícone da lua no menu lateral ou no botão "Escuro" do cabeçalho)

 |
| **ENTÃO** a interface do sistema deve aplicar o esquema de cores escuro em todas as telas e componentes visuais

 |
| **E** o estado do tema deve persistir ao navegar entre os diferentes módulos do sistema (ex.: Contas a Pagar).

 |

| **Critérios de Aceitação** |
| --- |
| * As cores de fundo, cards, menus e textos devem mudar imediatamente para o padrão escuro.

 |
| * A preferência de tema deve ser mantida durante a navegação entre as páginas.

 |

---

#### Caso de Teste 02: Alternância para o Tema Claro (Light Mode)

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Validar o retorno da interface do modo Escuro para o modo Claro.

 |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit com a interface em modo Escuro.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está navegando no sistema SiFit com o tema Escuro ativo

 |
| **QUANDO** clicar no botão/seletor de tema claro (ícone do sol no menu lateral ou no botão "Claro" do cabeçalho)

 |
| **ENTÃO** a interface do sistema deve aplicar o esquema de cores claro em todas as telas e componentes visuais

 |
| **E** a tabela de dados e elementos de navegação devem retornar ao contraste original.

 |

| **Critérios de Aceitação** |
| --- |
| * O layout deve ser re-renderizado instantaneamente para a versão clara.

 |
| * Todos os textos e botões de ação devem manter a legibilidade adequada.

 |

https://jam.dev/c/21696cd1-a6e3-4a85-8f07-1fb3bc46b5c3
