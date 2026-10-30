---

## Cenário 16: Gerenciamento de Fichas de Treino

---

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
| **QUANDO** preencher o campo **Código** (ex.: "236") ou selecionar um status específico no filtro (Ativo, Inativo, Cancelado, Finalizado).|
| **E** clicar no botão **Buscar**<br> |
| **ENTÃO** a tabela deve processar a consulta, porém os filtros de listagem por status ou código nada fazem ou retornam a mensagem *"Nenhuma ficha encontrada"* na grade de dados. |

| **Critérios de Aceitação** |
| --- |
| * Identificar e registrar o comportamento da interface onde a filtragem da listagem por Status e Código não atualiza os registros esperados na tabela. |

| **Evidência** |
| --- |
| https://drive.google.com/file/d/1FnE_wPJnHguqWJ5pnR3-VvCgaZcGrTq8/view?usp=sharing |

---

