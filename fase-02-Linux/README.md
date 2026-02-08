# 🛡️ Mini SOC na Prática – Fase 2 | Linux Ubuntu

## 📌 Objetivo
Documentar e analisar eventos de autenticação e monitoramento de logs em ambiente **Linux Ubuntu**, utilizando arquivos de log nativos do sistema, com foco em aprendizado prático e simulação das atividades de um **SOC Nível 1**.

> 🔒 **Observação**
> Este projeto possui fins exclusivamente educacionais e de portfólio.
> Os eventos, usuários e dados apresentados são simulados e não pertencem a ambientes reais de produção.

---

## 🛠️ Ambiente Utilizado
- **Sistema Operacional:** Ubuntu Linux
- **Ferramentas:**
  - Terminal Linux
  - systemctl
  - tail
  - grep

### Logs Analisados
- `/var/log/auth.log` – Eventos de autenticação e uso de privilégios (sudo)
- `/var/log/syslog` – Eventos gerais do sistema e kernel

---

## 🔍 Eventos Analisados
Foram coletadas evidências dos seguintes eventos e atividades:

- Status do serviço SSH  
  - `systemctl status ssh`

- Tentativas de autenticação e uso de sudo  
  - `/var/log/auth.log`

- Monitoramento em tempo real de logs de autenticação  
  - `tail -f /var/log/auth.log`

- Eventos recentes do sistema  
  - `tail -n 50 /var/log/syslog`

A análise foi baseada exclusivamente nos registros apresentados nos **prints coletados durante a atividade prática**.

---

## 🧠 Análise Técnica
Os eventos analisados permitem:

- Verificar o status de serviços críticos (SSH)
- Identificar falhas de autenticação e uso de privilégios elevados (sudo)
- Observar eventos em tempo real para detecção inicial de comportamentos suspeitos
- Correlacionar eventos de autenticação com atividades gerais do sistema (syslog)

Não foram identificadas evidências de comprometimento ativo do sistema, apenas eventos operacionais e falhas legítimas de autenticação.

---

## 🏷️ Classificação do Evento
- **Tipo:** Evento de Segurança / Auditoria
- **Severidade:** Baixa
- **Status:** Monitoramento
- **Finalidade:** Treinamento e prática SOC Nível 1

---

## 📌 Conclusão
A Fase 2 demonstra a importância de:

- Monitoramento contínuo de serviços críticos
- Auditoria de logs de autenticação em ambientes Linux
- Acompanhamento de atividades privilegiadas (sudo)
- Documentação técnica clara e organizada

Esta etapa reforça o papel do **SOC Nível 1** na triagem, documentação e classificação inicial de eventos de segurança em sistemas Linux.

---

## 🖼️ Evidências (prints)
As evidências coletadas estão organizadas na pasta:

prints/evento/

E detalhadas no arquivo:

evento.md

### Evidências disponíveis:
- Status do serviço SSH
- Auth.log – visão geral
- Uso de sudo para análise de logs
- Monitoramento em tempo real
- Syslog – eventos recentes

---

📄 Documento desenvolvido para fins de estudo, documentação técnica e composição de portfólio em **Segurança da Informação / SOC / Blue Team**.
