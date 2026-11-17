# SIFIT — trabalho de QA

Documentação dos testes manuais do SIFIT para a atividade de extensão em Qualidade de Software. **Comece pelo índice de cenários** se estiver procurando uma funcionalidade específica.

## Guia de leitura

| Etapa | Documento | Para que serve |
| --- | --- | --- |
| 1 | [Análise de requisitos](Sifit/1-Analise%20de%20Requisitos.md) | Define o comportamento esperado e relaciona os requisitos aos casos. |
| 2 | [Plano de testes](Sifit/2-Plano%20de%20Testes.md) | Explica escopo, estratégia, critérios e cobertura. |
| 3 | [Índice dos cenários](Sifit/Cenario%20de%20Testes/README.md) | Localiza os 48 arquivos de cenário por módulo e código RF. |
| 4 | [Relatório de bugs](Sifit/3-Relatorio%20de%20Bugs.md) | Descreve os defeitos, passos de reprodução e evidências. |
| 5 | [Relatório de execução](Sifit/4-Relatorio%20de%20Testes.md) | Consolida os resultados por módulo e o total do trabalho. |

Os **48 cenários** documentam **218 casos**. Outros **37 casos falhos distintos** constam no relatório de bugs: **255 casos no total**. Os links de vídeo e print ficam junto dos respectivos casos ou bugs.

**Evidência pendente:** C47-CT01 não tem vídeo ou print vinculado. O resultado desse caso consta na consolidação, mas ainda precisa de comprovação.

## Organização

```text
README.md                      ← este guia
Sifit/
  1-Analise de Requisitos.md   ← o que testar
  2-Plano de Testes.md         ← como testar
  Cenario de Testes/
    README.md                  ← índice por módulo
    CT_RF01 ... CT_RF48.md     ← casos e evidências
  3-Relatorio de Bugs.md       ← defeitos
  4-Relatorio de Testes.md     ← resultados
  Historico/                   ← material anterior, fora da contagem do grupo
```

O [trabalho individual anterior](Sifit/Historico/Achados%20do%20trabalho%20individual%20anterior.md) fica separado dos resultados do grupo. O [manual do sistema no Google Drive](https://docs.google.com/document/d/1_DrvjEBYbNv-c4Z-IgYSq38t17iIv9HAx9Vvx0tgoCs/edit?usp=drivesdk) é outro entregável da disciplina.

## Integrantes

- Arthur Miranda Rodrigues — RA 14538
- Larissa Fernanda O. — RA 14536
- Felype Augusto Dos Santos Silva — RA 14537
- Guilherme Felipe de Morais — RA 5608
- Gabrielle Bonini Barbosa — RA 14506
- Gabriel de Abreu da Silva — RA 14525
