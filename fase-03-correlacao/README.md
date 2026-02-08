
# Mini-SOC – Fase 3 (Correlação Windows x Linux)

## Objetivo

Nesta fase, foi realizada a correlação dos eventos coletados nas fases anteriores:

- **Fase 1:** Windows (eventos de autenticação, falhas de login 4625, uso de privilégios)
- **Fase 2:** Linux/Ubuntu (SSH, auth.log, sudo, syslog)

O objetivo é identificar padrões, possíveis incidentes e comportamentos suspeitos que se manifestam de forma correlacionada entre diferentes sistemas.

---

## 01 – Preparação dos Dados

- Organização dos logs de Windows e Linux em uma mesma linha do tempo.
- Seleção dos eventos considerados críticos para análise:
- Tentativas de login falhas (Evento 4625 no Windows e falhas de autenticação via SSH no Linux).
- Uso de privilégios elevados, como sudo no Linux.
- Eventos relacionados a serviços de acesso remoto, como SSH.

---

## 02 – Tabela de Correlação

| Horário           | Usuário | Evento Windows        | Evento Linux            | Observação SOC |
|-------------------|---------|-----------------------|-------------------------|----------------|
| 2026-02-05 08:12  | admin   | Falha de login (4625) | Tentativa SSH falha     | Tentativa de autenticação falha em ambos os sistemas no mesmo intervalo de tempo |
| 2026-02-05 08:14  | admin   | Falha de login (4625) | Tentativa SSH falha     | Repetição de falhas consecutivas, indicando possível tentativa automatizada |
| 2026-02-05 08:16  | admin   | Falha de login (4625) | Tentativa SSH falha     | Padrão persistente de falhas de autenticação |
| 2026-02-05 09:02  | user01  | Falha de login (4625) | Uso de sudo registrado  | Tentativa falha no Windows seguida de atividade privilegiada no Linux |
| 2026-02-05 10:22  | user02  | Falha de login (4625) | Nenhum evento correlato | Tentativa isolada no Windows, sem padrão correlacionado |
| 2026-02-05 10:30  | admin   | Falha de login (4625) | Tentativa SSH falha     | Continuidade do padrão de falhas para o mesmo usuário |

---

## 03 – Análise SOC

1. **Padrões de Tentativas Falhas**  
   A repetição de falhas de autenticação em curto intervalo de tempo, tanto no Windows quanto no Linux, indica possível tentativa automatizada de acesso não autorizado.

2. **Correlação entre Sistemas**  
   A ocorrência de falhas simultâneas em ambientes distintos sugere que o mesmo usuário ou origem pode estar sendo testado em múltiplos sistemas.

3. **Uso de Privilégios**  
   O registro de uso de sudo no Linux após falhas de login no Windows reforça a necessidade de monitoramento, pois pode indicar tentativa de acesso privilegiado.

4. **Linha do Tempo**  
   A organização cronológica dos eventos facilita a identificação de padrões suspeitos e apoia uma resposta mais rápida por parte do SOC.

---

## 04 – Conclusão da Correlação

A análise correlacionada dos logs de Windows e Linux permitiu identificar padrões de tentativas falhas de autenticação que não seriam tão evidentes se analisados de forma isolada. Embora não haja evidência de acesso bem-sucedido, o comportamento observado exige atenção e monitoramento contínuo.

---

## 05 – Classificação do Evento (SOC)

**Tipo de Evento:** Tentativa de acesso não autorizado  
**Categoria:** Autenticação / Controle de Acesso  
**Origem:** Windows e Linux (ambiente correlacionado)

**Descrição:**  
Foram identificadas múltiplas tentativas de autenticação falhas (Evento 4625 no Windows e falhas de autenticação via SSH no Linux), ocorrendo de forma repetitiva e em curto intervalo de tempo. Esse padrão é compatível com tentativa de força bruta ou teste automatizado de credenciais.

**Status do Evento:** Suspeito

---

## 06 – Severidade do Evento

**Nível de Severidade:** Média

**Justificativa:**  
Apesar de não haver evidência de login bem-sucedido, o volume e a repetição das tentativas falhas indicam possível tentativa de acesso não autorizado, justificando monitoramento contínuo.

---

## 07 – Ações Recomendadas (SOC Nível 1)

- Monitorar continuamente eventos de falha de autenticação (4625 e SSH Failed).
- Criar alertas para múltiplas tentativas de login falhas em curto período.
- Verificar políticas de bloqueio de conta após tentativas inválidas.
- Analisar origem das tentativas, como usuário, horário e possível endereço IP.
- Documentar o evento e manter as evidências organizadas.

---

## 08 – Próximos Passos (Escalonamento)

- Manter o evento sob observação.
- Caso o padrão se intensifique, escalar para SOC Nível 2.
- Avaliar a implementação de uma ferramenta SIEM para correlação automática.
- Considerar a criação de um playbook para eventos de autenticação suspeitos.

---

## Observações Finais

- Sempre documentar horário, usuário e tipo de evento com precisão.
- A correlação deve ser revisada periodicamente para ajuste de padrões e sinais de alerta.
- Este modelo permite a inclusão de novos eventos conforme novas evidências sejam coletadas.



