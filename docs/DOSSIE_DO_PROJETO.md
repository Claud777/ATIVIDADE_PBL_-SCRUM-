## 1.1 Resumo Executivo

  

O projeto visa digitalizar a gestão de manutenção dos laboratórios de TI, substituindo solicitações informais por um fluxo automatizado via **Open Claw**. A solução integra a captura de chamados com um dashboard web responsivo para visualização de métricas de desempenho (SLA) e recorrência de falhas. O foco é a entrega de um MVP funcional em 4 semanas, utilizando ferramentas _open source_ e _free tier_ para manter o custo zero de licenciamento.

  

## 1.2 Problema e Objetivos

  

- **Problema:** Centralização ineficiente de chamados, falta de histórico e previsibilidade para aulas práticas.

- **Objetivo:** Implementar um sistema de triagem automática e relatórios de suporte.

- **Métrica de Sucesso:** Redução do Tempo Médio de Atendimento (TMA) em 30% nos primeiros dois meses de uso.

  

## 1.3 Stakeholders e Perfis

  

- **Solicitante (Professor/Aluno):** Abre chamados e anexa evidências.

- **Técnico de TI:** Gerencia a fila, altera status e executa a manutenção.

- **Coordenador:** Analisa relatórios e decide sobre investimentos em infraestrutura.

  

## 1.4 Jornada AS-IS e TO-BE

  

- **AS-IS (Hoje):** Professor identifica falha -> Manda WhatsApp -> Técnico esquece -> Falha persiste na próxima aula.

    - _Dor:_ Falta de registro e esquecimento.

- **TO-BE (Com Sistema):** Professor abre chamado via Web/QR Code -> Open Claw notifica técnico e prioriza por criticidade -> BI gera alerta de recorrência -> Coordenador visualiza o gargalo.

    - _Ganho:_ Histórico auditável e transparência.

  

## 1.5 Requisitos Funcionais (User Stories)

  

1. **US01:** Eu, como solicitante, quero fazer login para acompanhar meus pedidos.

2. **US02:** Eu, como solicitante, quero abrir um chamado com foto para detalhar o defeito.

3. **US03:** Eu, como técnico, quero visualizar uma fila única para não perder solicitações.

4. **US04:** Eu, como técnico, quero alterar o status do chamado (Em andamento/Concluído).

5. **US05:** Eu, como coordenador, quero ver um gráfico de chamados por laboratório.

6. **US06:** Eu, como técnico, quero atribuir um chamado a mim mesmo para evitar duplicidade de trabalho.
    
7. **US07:** Eu, como solicitante, quero receber notificações de mudança de status para ter previsibilidade.
    
8. **US08:** Eu, como coordenador, quero filtrar relatórios por data para analisar períodos específicos.
    
9. **US09:** Eu, como técnico, quero adicionar notas técnicas ao histórico para documentar a solução.
    
10. **US10:** Eu, como solicitante, quero poder cancelar um chamado caso o problema se resolva sozinho.
    
11. **US11:** Eu, como técnico, quero visualizar o anexo em tela cheia para diagnosticar falhas visuais.
    
12. **US12:** Eu, como coordenador, quero visualizar o Tempo Médio de Resolução (TMR) por técnico.

## 1.6 Requisitos Não funcionais



- **Desempenho:** O sistema deve carregar o dashboard inicial em menos de 2 segundos.
    
- **Segurança:** Toda comunicação deve ser criptografada via HTTPS e autenticada via JWT.
    
- **Disponibilidade:** O sistema deve estar operacional 99% do tempo durante o horário letivo.
    
- **Responsividade:** A interface deve ser adaptável para smartphones e desktops.

  
## 1.7 Priorização Backlog (RICE)



|**Feature**|**Reach**|**Impact**|**Confidence**|**Effort**|**Score**|

|---|---|---|---|---|---|

|Abertura de Chamado|5|5|100%|2|**12.5**|

|Dashboard de BI|2|4|80%|3|**2.1**|

## 1.8 Arquitetura C4 (Resumo)

  

- **Contexto:** O usuário interage com o Web App que se comunica com o motor do Open Claw.

- **Containers:** * **Frontend:** React/Flutter Web (Responsivo).

    - **Automation Layer:** Open Claw (Processamento de Regras).

    - **Database:** PostgreSQL (BI e Logs).