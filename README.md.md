# 🛡️ Segundo Cérebro em Cibersegurança & Infraestrutura

> **Objetivo:** Servir como um assistente técnico especialista em hardening de servidores Windows e Linux, engenharia e gestão de logs no Graylog, e conformidade com os frameworks NIST e CIS, fundamentando todas as decisões e recomendações estritamente em documentações oficiais e padrões globais de segurança.

---

## 📌 Visão Geral do Projeto
Este projeto consiste na criação de uma base de conhecimento especialista (RAG) desenvolvida no **Google Notebook (NotebookLM)**. O objetivo é apoiar analistas de segurança e administradores de sistemas em tomadas de decisão críticas, diretrizes de endurecimento de sistemas (*hardening*) e auditoria de logs, garantindo rastreabilidade e embasamento teórico/prático.

---

## 📚 Curadoria de Fontes de Dados
A base do conhecimento é composta por 37 fontes rigorosamente selecionadas, divididas entre padrões da indústria, manuais de fabricantes e guias normativos:

* **Hardening Windows:**
  * *CIS Microsoft Windows Server Benchmarks* (Center for Internet Security)
  * Documentações oficiais da Microsoft e linhas de base de segurança (*Security Compliance Toolkit*)
* **Hardening Linux:**
  * *CIS Linux Benchmarks* (Ubuntu / RHEL)
  * *Red Hat Enterprise Linux Security Hardening Guide*
  * Documentações oficiais de segurança da Canonical/Ubuntu
* **Gestão de Logs & SIEM:**
  * Documentação Oficial da Arquitetura e Pipelines do Graylog
  * *NIST SP 800-92: Guide to Computer Security Log Management*
  * Guias de configuração de agentes de auditoria (`auditd` para Linux e `Sysmon` para Windows)
* **Governança & Conformidade:**
  * *CIS Controls Framework v8* (Foco em *Audit Logging & Monitoring*)
  * *NIST SP 800-53: Security and Privacy Controls*

> **Critério de Seleção:** Foram aceitas exclusivamente fontes primárias de fabricantes reconhecidos ou órgãos normativos globais (NIST, CIS, Red Hat, Microsoft). Fontes não verificadas, blogs pessoais sem revisão por pares ou opiniões sem fundamentação foram totalmente descartadas.

---

## 🤖 Diretriz de Comportamento (System Prompt / Persona)
A instrução configurada para calibrar o tom e a profundidade das respostas do notebook foi:

> *"Você é um engenheiro sênior de infraestrutura e cibersegurança especializado em hardening de sistemas operacionais (Windows e Linux), coleta de logs no Graylog e conformidade com NIST e CIS. Responda estritamente com base nos documentos carregados, citando as seções ou benchmarks correspondentes (ex: CIS Benchmark), e forneça justificativas técnicas para cada parâmetro de configuração recomendado."*

---

## 🧪 Validação e Consultas Realizadas (Evidências)

### 1. Hardening em Windows Server
* **Pergunta:** *"Quais são as recomendações do CIS Benchmark para a política de complexidade e expiração de senhas em servidores Windows Server, e qual o racional de segurança dessas diretrizes?"*
* **Resposta obtida (inicio):** [Descreva sucintamente a resposta gerada]
* **Evidência:** https://github.com/emanuelgaio/segundo-cerebro-cyber-infra/blob/main/Hardening%20em%20Windows%20Server.png

### 2. Hardening e Parâmetros de Kernel em Linux
* **Pergunta:** *"Com base nos padrões de segurança para sistemas Linux (como Red Hat ou CIS), como devem ser tratadas as permissões do arquivo `/etc/shadow` e quais parâmetros essenciais de kernel devem ser ajustados no `/etc/sysctl.conf` para mitigação de ataques?"*
* **Resposta obtida (inicio):** Com base nos padrões de segurança e guias de consolidação (*hardening*) do **CIS Benchmark** para distribuições Linux (como Ubuntu e RHEL/Red Hat), o tratamento das permissões do `/etc/shadow` e a parametrização do kernel via `sysctl` obedecem a diretrizes rígidas de proteção da integridade e contenção de ameaças
* **Evidência:** https://github.com/emanuelgaio/segundo-cerebro-cyber-infra/blob/main/Hardening%20e%20Par%C3%A2metros%20de%20Kernel%20em%20Linux.png

### 3. Coleta de Logs e Requisitos NIST / Graylog
* **Pergunta:** *"Segundo as diretrizes do NIST SP 800-92 e as melhores práticas de centralização de logs, quais categorias críticas de eventos de segurança de servidores (Windows e Linux) devem ser obrigatoriamente coletadas e encaminhadas para um SIEM como o Graylog?"*
* **Resposta obtida (inicio):** Segundo as diretrizes do **NIST SP 800-92** (*Guide to Computer Security Log Management*) e os benchmarks de segurança para servidores (como CIS Windows Server e CIS Ubuntu/RHEL Linux), a centralização de logs em uma plataforma SIEM (como o Graylog) é fundamental para garantir a detecção precoce de ameaças, resposta a incidentes e não-repúdio[1].

Como invasores frequentemente tentam apagar seus vestígios nos arquivos locais após comprometer um host, a coleta e o envio em tempo real dos logs para um SIEM garante a preservação e a integridade da evidência
* **Evidência:** https://github.com/emanuelgaio/segundo-cerebro-cyber-infra/blob/main/Coleta%20de%20Logs%20e%20Requisitos%20NIST%20-%20Graylog.png

---

## 📁 Materiais Gerados pelo Estúdio
Os arquivos gerados automaticamente pela ferramenta a partir do corpus do projeto foram exportados e estão disponíveis na raiz deste repositório:
* 🗺️ **Mapa Mental:** `mapa-mental-hardening-logs.png`
* 📊 **Apresentação em Slides:** `slides-estrategia-cybersecurity.pdf

---

## 🔗 Link do Notebook Compartilhado
* [Acessar Notebook no Google NotebookLM]: https://github.com/emanuelgaio/segundo-cerebro-cyber-infra