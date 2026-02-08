\# 🛡️ Mini-SOC – Fase 2 (Linux Ubuntu)

\## Detalhes das Evidências de Eventos



Este documento apresenta as evidências técnicas coletadas durante a Fase 2 do Mini-SOC,

com foco em monitoramento de serviços, análise de autenticação e auditoria de logs

em Linux Ubuntu, simulando atividades de um SOC Nível 1.



---


# Evento – Monitoramento e Análise de Logs (Linux)

Este evento documenta a coleta, monitoramento e análise de logs de autenticação e sistema em ambiente Linux, com foco em visibilidade, auditoria e resposta inicial a incidentes.

---

## 01 – Visão Geral dos Logs de Autenticação

**Objetivo:**  
Obter uma visão geral dos registros de autenticação do sistema para identificar padrões de acesso e possíveis anomalias.

**Print:**

![Visão geral auth.log](auth_log_visao_geral.png)

---

## 02 – Monitoramento em Tempo Real

**Objetivo:**  
Acompanhar eventos de autenticação em tempo real para detectar tentativas suspeitas imediatamente.

**Print:**

![Monitoramento em tempo real](monitoramento_realtime_log.png)

---

## 03 – Status do Serviço SSH

**Objetivo:**  
Verificar se o serviço SSH está ativo e operando corretamente, garantindo acesso remoto seguro.

**Print:**

![Status do serviço SSH](ssh_status_servico.png)

---

## 04 – Eventos Recentes do Syslog

**Objetivo:**  
Analisar eventos recentes do sistema registrados no syslog para identificar erros, alertas ou atividades incomuns.

**Print:**

![Eventos recentes do syslog](syslog_eventos_recentes.png)

---

## 05 – Uso do Comando SUDO para Análise de Logs

**Objetivo:**  
Demonstrar o uso de privilégios administrativos para acessar e analisar arquivos de log sensíveis.

**Print:**

![Uso de sudo para análise](uso_sudo_para_analise_auth_log.png)

---

## Conclusão

A análise dos logs permite identificar comportamentos suspeitos, validar o funcionamento dos serviços críticos e reforçar boas práticas de monitoramento contínuo, fundamentais para atividades de SOC e Segurança da Informação.



