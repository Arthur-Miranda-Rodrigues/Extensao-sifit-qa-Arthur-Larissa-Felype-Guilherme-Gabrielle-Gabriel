
---

# Cenário 19: Gerenciamento de Objetivos Treino

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Cenário 19: Gerenciamento de Objetivos Treino** do módulo **Treinamento > Objetivos** do sistema **SiFit**. O objetivo é validar o comportamento do cadastro de novos objetivos com validação de erros e o funcionamento dos filtros de busca por nome.

---

## 2. Casos de Teste

### Caso de Teste 01: Validação de Erro no Cadastro de Novo Objetivo

| ID | Descrição |
| --- | --- |
| **C19-CT01** | Verificar o comportamento do sistema ao tentar cadastrar um novo objetivo de treino e simular uma mensagem de erro no processamento. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Objetivos Treino**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Objetivos Treino**<br> |
| **E** clica no botão **+ Novo Objetivo**<br> |
| **QUANDO** preencher o campo **Nome** com "Perder Peso" no modal **Objetivo**<br> |
| **E** preencher o campo **Descrição** com "Perder Peso". |
| **E** clicar no botão **Salvar**<br> |
| **ENTÃO** o sistema deve exibir um modal de alerta informando falha ao salvar (ex.: *"Erro: Erro ao salvar objetivo"*). |

| **Critérios de Aceitação** |
| --- |
| * O sistema deve tratar falhas de gravação exibindo uma mensagem de erro clara em formato modal com opção de fechamento. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1tYtIn2lU4Xf79VkMmJ1bmJ-wGZJWbfy3/view?usp=sharing |

---

### Caso de Teste 02: Filtragem e Busca por Nome de Objetivo de Treino

| ID | Descrição |
| --- | --- |
| **C19-CT02** | Validar o funcionamento da ferramenta de busca e filtragem utilizando o campo **Nome** na listagem de Objetivos de Treino.|

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Objetivos Treino**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Objetivos Treino**<br> |
| **QUANDO** preencher o campo **Nome** com "ganhar músculos". |
| **E** clicar no botão **Buscar**<br> |
| **E** limpar o campo de busca e clicar novamente em **Buscar** para resetar a visualização. |
| **ENTÃO** o sistema deve executar a consulta correspondente ao filtro informado e permitir limpar os parâmetros de busca com sucesso. |
| **E** nada acontece por não ter nenhum objetivo treino.|

| **Critérios de Aceitação** |
| --- |
| * Os filtros devem responder corretamente ao termo pesquisado e permitir o restablecimento da tela ao limpar os campos. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1Si8R7Ssru47puuoupZFh5B-KEhhabY4F/view?usp=sharing |
