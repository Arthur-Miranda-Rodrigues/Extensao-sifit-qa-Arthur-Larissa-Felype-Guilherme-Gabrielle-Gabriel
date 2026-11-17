# Achados complementares do trabalho individual anterior

Este registro preserva duas observações do repositório individual anterior (`C:\Trabalho-QA\extensao-qa-sifit`), realizadas em 27/10/2026. Elas **não** integram os 255 casos nem os 37 bugs consolidados neste repositório de grupo: ocorreram em execuções e ambientes diferentes e precisam de reteste antes de entrar no relatório principal.

## Matrícula com período invertido aceita

- **Ambiente registrado:** `https://sifit.centrion.com.br`.
- **Passos:** no cadastro de matrícula, selecionar cliente e demais dados exigidos, informar Data Inicial **29/10/2026** e Data Final **27/10/2026** e salvar.
- **Esperado:** impedir o cadastro com data final anterior à inicial e informar a inconsistência.
- **Observado na gravação anterior:** a interface confirmou “Matrícula salva” e abriu a conta a receber de ID 1620.
- **Evidência anterior:** [vídeo Jam do caso MAT-02](https://jam.dev/c/8e8d97e0-154e-4eae-9fc9-a05665f4e883).
- **Próximo passo:** repetir no ambiente de referência do grupo com dados descartáveis, verificar a gravação e, se persistir, abrir bug próprio. O BUG-003 do relatório principal trata de **datas no filtro de aulas do SifitBox**, portanto não cobre este fluxo de matrícula.

## Mensagem de Avaliações durante falha de matrícula

- **Ambiente registrado:** `https://sifitalfa.centrion.com.br`.
- **Passos:** abrir Nova Matrícula, selecionar um cliente, preencher o formulário e salvar.
- **Esperado:** caso o cadastro seja rejeitado, a mensagem deve se referir à matrícula e explicar a rejeição.
- **Observado na gravação anterior:** resposta HTTP 400 e modal “Não foi possível concluir” com o detalhe “Erro ao Cadastrar em Avaliações”. A causa da rejeição não foi isolada.
- **Evidência anterior:** [vídeo Jam do caso MAT-01](https://jam.dev/c/2f0ded45-dc0c-434b-99ed-993644db0bc5).
- **Próximo passo:** repetir com massa válida e identificar a causa do HTTP 400. Se a mensagem continuar citando Avaliações, registrar defeito de texto/feedback sem atribuir causa ao erro do servidor.

Os demais testes do repositório antigo foram um recorte individual anterior. Seus resultados não substituem os casos e evidências do grupo.
