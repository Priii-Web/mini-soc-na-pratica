# 🚨 Event ID 4625 – Falha de Autenticação (Windows)


## 📌 Objetivo

Documentar e analisar eventos de **falha de autenticação no Windows (Event ID 4625)**, utilizando o Visualizador de Eventos, com foco em aprendizado prático e simulação das atividades de um **SOC Nível 1**.

> **Observação:**
> Este projeto possui fins exclusivamente educacionais e de portfólio. Os eventos, usuários e dados apresentados não correspondem a ambientes reais de produção e não contêm informações sensíveis.

---

## 🛠️ Ambiente

* **Sistema Operacional:** Windows
* **Ferramenta:** Visualizador de Eventos (Event Viewer)
* **Log analisado:** Windows Logs → Security (Segurança)

---

## 🔍 Evento Analisado

**Event ID:** 4625 – Falha de Autenticação

Foram identificadas **múltiplas ocorrências** do evento 4625 conforme exibido na lista de eventos filtrados no Visualizador de Eventos.

A análise foi baseada exclusivamente nos registros apresentados nos prints coletados durante a atividade prática.

---

## 🧠 Análise Técnica

O Event ID 4625 é registrado quando ocorre uma tentativa de logon malsucedida no sistema Windows.

Com base nas evidências coletadas:

* As falhas de autenticação ocorreram em curto intervalo de tempo
* Os eventos foram registrados no log de Segurança
* A análise detalhada foi realizada por meio das abas **Geral** e **XML** do evento

Não foram identificadas, a partir dos dados disponíveis, evidências suficientes para caracterizar ataque de força bruta ou comprometimento ativo do sistema.

Os eventos analisados permanecem classificados como **atividade operacional**, exigindo monitoramento contínuo e possível correlação com outros eventos.

---

## 🏷️ Classificação

* **Tipo:** Evento de Segurança
* **Evento:** Falha de Autenticação (4625)
* **Severidade:** Baixa
* **Status:** Monitoramento

---

## 📌 Conclusão

A análise dos eventos 4625 demonstra a importância do acompanhamento constante dos logs de segurança no Windows.

Mesmo eventos isolados ou operacionais podem representar indicadores iniciais de comportamento anômalo quando analisados em conjunto.

Esta atividade reforça o papel do **SOC Nível 1** na triagem, documentação e classificação inicial de eventos de segurança.

---


\## 🖼️ Evidências (prints)



\### 📍 Caminho do log

!\[Windows Logs Security](prints/evento-4625/caminho-security.png)



\### 📍 Filtro aplicado (Event ID 4625)

!\[Filtro 4625](prints/evento-4625/filtro-4625.png)



\### 📍 Lista de eventos filtrados

!\[Lista de eventos 4625](prints/evento-4625/lista-4625.png)



\### 📍 Detalhes do evento – Aba Geral

!\[Evento 4625 Geral](prints/evento-4625/evento-4625-geral.png)



\### 📍 Detalhes do evento – XML

!\[Evento 4625 XML](prints/evento-4625/evento-4625-xml.png)

---

Documento finalizado para fins de estudo, documentação técnica e composição de portfólio em Segurança da Informação.


