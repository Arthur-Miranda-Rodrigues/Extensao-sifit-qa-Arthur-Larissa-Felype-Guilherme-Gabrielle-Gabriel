---

# Cenário de Teste: Gerenciamento de Fichas de Treino

## 1. Descrição

Este documento especifica os casos de teste referentes ao módulo **Treinamento > Fichas de Treino** do sistema **SiFit**. O objetivo é validar a listagem, os filtros de busca por código, nome e status, e a tentativa de cadastro de novas fichas de treino com tratamento de exceções do sistema.

---

## 2. Cenários de Teste

### Caso de Teste 01: Validação de Filtros da Listagem e Inexistência de Resultados por Código e Status

| ID | Descrição |
| --- | --- |
| **C16-CT01** | Validar o comportamento da listagem ao aplicar filtros por código de ficha (ex.: "236") e diferentes opções de **Status** (Ativo, Inativo, Cancelado, Finalizado), evidenciando que a filtragem por status ou código isolado na tabela não retorna registros correspondentes. |

| **Pré-condições** |
| --- |
| Usuário autenticado no sistema SiFit e localizado na página **Fichas de Treino**.

 |

| **Passos** |
| --- |
| **DADO** que o usuário está na tela **Fichas de Treino**<br> |
| **QUANDO** preencher o campo **Código** (ex.: "236") ou selecionar um status específico no filtro (Ativo, Inativo, Cancelado, Finalizado)

 |
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** a tabela deve processar a consulta, porém os filtros de listagem por status ou código nada fazem ou retornam a mensagem *"Nenhuma ficha encontrada"* na grade de dados.

 |

| **Critérios de Aceitação** |
| --- |
| * Identificar e registrar o comportamento da interface onde a filtragem da listagem por Status e Código não atualiza os registros esperados na tabela.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1FnE_wPJnHguqWJ5pnR3-VvCgaZcGrTq8/view?usp=sharing |

---

### Caso de Teste 02: Tentativa de Cadastro de Nova Ficha de Treino e Tratamento de Erro no Servidor

| ID | Descrição |
| --- | --- |
| **C16-CT02** | Validar o fluxo de abertura do formulário de cadastro de ficha, preenchimento dos dados (aluno, personal, datas, objetivo e observação) e o tratamento de falha ao submeter o registro. |

| **Pré-condições** |
| --- |
| Usuário na página **Fichas de Treino** do SIFIT.

 |

| **Passos** |
| --- |
| **DADO** que o usuário clica no botão **Cadastrar Ficha**<br> |
| **QUANDO** selecionar o aluno (ex.: *Marcelo Longo Zandonadi*), o personal (*Gabriella*), definir o período de datas, preencher o objetivo (*Perder peso*) e a observação

 |
| **E** clicar no botão **Criar Nova Ficha**<br> |
| **ENTÃO** o sistema deve tentar gravar o registro, mas exibir um modal de erro com a mensagem: *"Erro: Erro ao salvar ficha"* acompanhado do botão **Fechar**.

 |

| **Critérios de Aceitação** |
| --- |
| * O formulário deve permitir o preenchimento de todos os campos de controle da ficha de treino.

 |
| * Em caso de falha de persistência no backend, o sistema deve exibir uma mensagem de erro clara ao operador sem corromper a navegação.

 |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1LALWrCOEkAcFrakPxBBUhDb7UygDZnAY/view?usp=sharing |
