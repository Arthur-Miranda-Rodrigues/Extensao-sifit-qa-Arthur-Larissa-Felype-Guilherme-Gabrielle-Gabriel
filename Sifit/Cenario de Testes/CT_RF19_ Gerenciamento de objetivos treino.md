
---

# Cernário de teste:Gerenciamento de Objetivos de Treino

## 1. Descrição

Este documento especifica os casos de teste referentes ao **Requisito Funcional 12 (RF12) - Gerenciamento de Objetivos de Treino** do módulo **Treinamento > Objetivos** do sistema **SiFit**. O objetivo é validar a busca e filtragem de objetivos, a criação de novos registros, a edição de descrições e o tratamento de erros e restrições de integridade referencial.

---

## 2. Cenários de Teste

### Cenário 01: Operações e Gestão de Objetivos de Treino

#### Caso de Teste 01: Filtragem e Busca de Objetivos de Treino

| ID | Descrição |
| --- | --- |
| **C01-CT01** | Validar o funcionamento dos filtros por Código e Nome na listagem de Objetivos de Treino. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Objetivos Treino**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Objetivos Treino** |
| **QUANDO** preencher o campo **Código** com "1" e clicar em **Buscar** |
| **E** limpar o campo **Código**, preencher o campo **Nome** com "crescer" e clicar em **Buscar** |
| **E** limpar os campos e clicar novamente no botão **Buscar** |
| **ENTÃO** a tabela deve filtrar e apresentar apenas os registros correspondentes ao parâmetro buscado em cada etapa |
| **E** recarregar a lista completa ao buscar sem parâmetros. |

| **Critérios de Aceitação** |
| --- |
| * Apenas os registros equivalentes ao código ou nome informados devem ser exibidos na grade. |
| * A limpeza dos filtros seguida de busca deve restabelecer a listagem completa. |

---

#### Caso de Teste 02: Validação no Cadastro de Novo Objetivo

| ID | Descrição |
| --- | --- |
| **C01-CT02** | Verificar a validação do sistema ao cadastrar um novo objetivo de treino. |

| **Pré-condições** |
| --- |
| Usuário autenticado na tela **Objetivos Treino**. |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Objetivos Treino** |
| **E** clica no botão **+ Novo Objetivo** |
| **QUANDO** preencher o campo **Nome** com "Emagrecer" no modal **Objetivo** |
| **E** mantiver os demais campos com os valores padrão |
| **E** clicar no botão **Salvar** |
| **ENTÃO** o novo objetivo deve ser gravado e incluído na listagem principal |
| **E** em caso de falha de validação ou erro de processamento, o sistema deve exibir uma mensagem de alerta amigável (ex.: *"Erro ao salvar objetivo"*). |

| **Critérios de Aceitação** |
| --- |
| * O cadastro deve ser salvo com sucesso gerando a identificação do novo objetivo. |
| * Erros operacionais ou de persistência devem ser informados de forma clara em tela. |

---

#### Caso de Teste 03: Edição e Atualização de Descrição do Objetivo

| ID | Descrição |
| --- | --- |
| **C01-CT03** | Validar a alteração e atualização dos dados cadastrais de um objetivo existente. |

| **Pré-condições** |
| --- |
| Existir ao menos um objetivo cadastrado na base de dados (ex.: "Crescer", Código 1). |

| **Passos** |
| --- |
| **DADO** que o usuário localiza o objetivo "Crescer" (Código 1) na listagem |
| **QUANDO** clicar no ícone de visualização/edição (lupa) na coluna de ações |
| **E** alterar o campo **Descrição** para "Crescer Músculos" no modal **Objetivo** |
| **E** clicar no botão **Salvar** |
| **ENTÃO** as alterações devem ser gravadas na base de dados |
| **E** a nova descrição ("Crescer Músculos") deve constar na listagem principal. |

| **Critérios de Aceitação** |
| --- |
| * O campo de descrição deve aceitar alterações e persistir os novos dados. |
| * O modal deve fechar e atualizar as informações diretamente na grade. |

---

#### Caso de Teste 04: Tentativa de Exclusão de Objetivo Vinculado

| ID | Descrição |
| --- | --- |
| **C01-CT04** | Verificar o tratamento de integridade referencial que impede a exclusão de um objetivo de treino em uso/vinculado. |

| **Pré-condições** |
| --- |
| Existir um objetivo de treino vinculado a alunos ou fichas de treino (ex.: "Crescer"). |

| **Passos** |
| --- |
| **DADO** que o usuário identifica o objetivo vinculado na tabela principal |
| **QUANDO** clicar no ícone de exclusão (**X**) na linha do registro |
| **E** confirmar a ação clicando no botão **Confirmar** dentro do modal *"Deseja deletar o Objetivo?"* |
| **ENTÃO** o sistema deve tratar a restrição de integridade referencial |
| **E** exibir um modal de aviso informando a impossibilidade de exclusão (ex.: *"Erro ao deletar Objetivo"*). |

| **Critérios de Aceitação** |
| --- |
| * Registros vinculados a fichas de treino ativas não podem ser excluídos da base. |
| * O alerta de erro deve impedir a remoção indevida e manter a consistência dos dados. |

https://jam.dev/c/47aadfe2-569d-413e-a2a4-0d5a7f5f1cff
