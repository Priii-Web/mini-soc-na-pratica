# 🛡️ Mini SOC na Prática – SOC N1 | Windows

## 📌 Sobre o Projeto
Este projeto simula, de forma prática e controlada, atividades realizadas por um **Analista de Segurança SOC Nível 1**, com foco na análise de logs de autenticação do Windows.

O objetivo é demonstrar capacidade técnica na identificação, filtragem, análise e documentação de eventos de segurança utilizando ferramentas nativas do sistema operacional.

> 🔒 **Aviso Importante**  
> Este projeto possui fins exclusivamente **educacionais e de portfólio**.  
> Os eventos, usuários e dados apresentados não correspondem a ambientes reais de produção, não representam incidentes reais e não contêm informações sensíveis.

---

## 🧱 Estrutura do Projeto


mini-soc-na-pratica/
├── fase-1-windows/
│   ├── evento-4625.md
│   └── prints/
│       └── evento-4625/
│           ├── caminho-security.png
│           ├── filtro-4625.png
│           ├── lista-4625.png
│           ├── evento-4625-geral.png
│           └── evento-4625-xml.png
├── fase-2-linux/        # (em desenvolvimento)
├── fase-3-correlacao/   # (planejado)
└── README.md



---

## 🎯 Objetivo da Fase 1 – Windows
Analisar eventos de falha de autenticação no Windows (**Event ID 4625**), identificar comportamentos relevantes e documentar tecnicamente os achados, simulando o fluxo de trabalho de um **SOC Nível 1**.

---

## 🛠️ Ambiente Utilizado
- **Sistema Operacional:** Windows  
- **Ferramenta:** Visualizador de Eventos (Event Viewer)  
- **Log analisado:** Windows Logs → Security  

---

## 🔍 Evento Analisado
### Event ID 4625 – Falha de Autenticação

O evento 4625 é registrado quando ocorre uma tentativa de logon malsucedida no sistema Windows.

Foram identificadas **múltiplas ocorrências** do evento, conforme exibido na lista de eventos filtrados no Visualizador de Eventos.

A análise foi realizada com base nos registros apresentados nas abas **Geral** e **XML** do evento.

---

## 🧠 Análise Técnica
Os eventos analisados indicam falhas de autenticação registradas no log de Segurança do Windows.

Com base apenas nas evidências disponíveis nos prints:
- Não há confirmação de ataque de força bruta
- Não há correlação direta com eventos de logon bem-sucedido (Event ID 4624)
- Os registros indicam atividade que deve ser monitorada e correlacionada em análises futuras

Os eventos permanecem classificados como **operacionais**, exigindo acompanhamento contínuo.

---

## 🏷️ Classificação do Evento
- **Tipo:** Evento de Segurança  
- **Evento:** Falha de Autenticação (4625)  
- **Severidade:** Baixa  
- **Status:** Monitoramento  

---

## 📌 Conclusão
Este estudo demonstra a importância do monitoramento contínuo dos logs de autenticação no Windows.

Mesmo eventos classificados como operacionais podem representar indicadores iniciais de comportamento anômalo quando analisados em conjunto.

A documentação e a análise técnica fazem parte das atribuições fundamentais de um **Analista SOC Nível 1**.

---

🖼️ Evidências (prints)

📍 Caminho do log:
Windows Logs → Security

📍 Filtro aplicado:
Event ID 4625

📍 Lista de eventos filtrados

📍 Detalhes do evento – Aba Geral

📍 Detalhes do evento – Aba XML
---

## 🚀 Próximas Etapas
- 🔜 Fase 2 – Análise de autenticação em sistemas Linux  
- 🔗 Fase 3 – Correlação de eventos Windows e Linux  
- 📊 Evolução para classificação de incidentes  

---

## 👤 Perfil Profissional
Projeto desenvolvido com foco em aprendizado prático, evolução técnica e construção de portfólio para atuação em **Segurança da Informação / SOC / Blue Team**.


