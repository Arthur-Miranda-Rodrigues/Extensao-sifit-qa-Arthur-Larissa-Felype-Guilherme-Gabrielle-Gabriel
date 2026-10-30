## Cenário 19: Gerenciamento de Objetivos Treino

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
