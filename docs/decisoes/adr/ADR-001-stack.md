ADR-001 — Escolha da Stack Frontend e Motor de Regras
Status: Aceito

Data: 28/04/2026

Decisores: Claud

Contexto
O projeto exige um sistema web responsivo para uso em laboratórios (mobile/desktop) com prazo de 4 semanas. O orçamento para licenças é zero. Há necessidade de automação de fluxo de chamados que não demande meses de desenvolvimento de backend.

Decisão
Utilizar Flutter Web para a interface do dashboard e Open Claw como motor de automação e orquestração de dados.

Alternativas consideradas

React.js: Excelente ecossistema, mas demandaria mais tempo para atingir a consistência de UI que o Flutter entrega "out-of-the-box".

Desenvolvimento 100% Nativo: Inviável pelo prazo e custo de manutenção de múltiplas bases de código.

Justificativa
A escolha do Flutter permite reaproveitamento de componentes e alta velocidade de prototipagem. O Open Claw entra como o "cérebro" que recebe o input do usuário e aplica as regras de prioridade e SLA sem a necessidade de codificar uma API complexa do zero.

Consequências

Positivas: UI altamente responsiva; lógica de negócio centralizada no motor de automação.

Negativas: O bundle inicial do Flutter Web pode ser maior que o do React; dependência da estabilidade do Open Claw.