# 🧪 SIFIT — Testes Manuais

Repositório do trabalho de extensão em Qualidade de Software: testes manuais do sistema **SIFIT** (gestão para academia/box), com foco em:

* Aprendizado de QA
* Organização de casos de teste
* Rastreabilidade entre requisitos, cenários, casos, evidências e bugs
* Melhoria contínua na análise e cobertura de testes

---

## 🎯 Objetivo

Este projeto foi criado com o objetivo de:

* Consolidar conhecimentos de testes manuais
* Avaliar uma aplicação já existente (sem desenvolvê-la), identificar defeitos e documentá-los de forma rastreável
* Criar um portfólio técnico bem estruturado para futuras oportunidades profissionais

---

## 📊 Resumo do trabalho

| Indicador | Valor |
| --- | :---: |
| Requisitos funcionais (RF01–RF48) | 48 |
| Cenários de teste | 48 |
| Casos de teste na pasta de cenários | 218 |
| Casos registrados só no Relatório de Bugs | 37 |
| Total de casos documentados | 255 |
| Casos aprovados / reprovados | 218 / 37 |
| Bugs registrados | 37 (17 altos, 17 médios, 3 baixos) |

---

## 🧱 Estrutura do repositório

Todo o material está na pasta [`Sifit/`](Sifit), organizada em documentos numerados que representam cada etapa, mais a pasta de cenários:

📄 **[1-Analise de Requisitos.md](Sifit/1-Analise%20de%20Requisitos.md)** ↳ Requisitos funcionais RF01–RF48, derivados dos cenários de teste

📄 **[2-Plano de Testes.md](Sifit/2-Plano%20de%20Testes.md)** ↳ Escopo, estratégia, critérios, cronograma, módulos e riscos

📁 **[Cenario de Testes](Sifit/Cenario%20de%20Testes/README.md)** ↳ 48 cenários (`CT_RF01` a `CT_RF48`) com 218 casos de teste em BDD; o índice na pasta permite abrir cada cenário pelo código RF

📄 **[3-Relatorio de Bugs.md](Sifit/3-Relatorio%20de%20Bugs.md)** ↳ 37 bugs, com passos para reproduzir, resultado esperado/obtido, severidade e evidência

📄 **[4-Relatorio de Testes.md](Sifit/4-Relatorio%20de%20Testes.md)** ↳ Relatório final: resumo da execução, cobertura por módulo, bugs e conclusão

📁 **[Historico](Sifit/Historico/Achados%20do%20trabalho%20individual%20anterior.md)** ↳ Achados do trabalho individual anterior, registrados à parte e fora da contagem do grupo

📹 **Evidências** ↳ Vídeos curtos do Jam ou gravações de tela no Google Drive, linkados dentro de cada caso de teste e de cada bug

---

## 🧪 Metodologia

* **Técnicas aplicadas:** caminho feliz, testes negativos, particionamento de equivalência, análise de valor limite, integridade referencial, testes de interface e exploratório
* **Ferramentas:** Markdown, Git/GitHub, navegador (Chrome/Firefox/Brave) com DevTools, MySQL Workbench (apoio), Jam e Google Drive (evidências)
* **Formatos:** BDD (Dado / Quando / Então), tabelas e checklist
* **Processos:** planejamento de teste, execução, registro de bugs e relatório final

---

## 👥 Equipe

* Arthur Miranda Rodrigues
* Larissa Fernanda O.
* Felype Augusto Dos Santos Silva
* Guilherme Felipe de Morais
* Gabrielle Bonini Barbosa
* Gabriel de Abreu da Silva

---

## 📌 Status do Projeto

✅ Documentação concluída e revisada

📋 Feedbacks são bem-vindos!

---

## 🚀 Sistema testado

* **SIFIT:** [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)
