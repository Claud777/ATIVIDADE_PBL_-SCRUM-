ADR-004 — Estratégia de Deploy e Observabilidade
Status: Aceito

Data: 28/04/2026

Decisores: Claud

Contexto
Orçamento de R$ 0 e apenas uma VPS disponível para rodar Banco de Dados, Open Claw e Frontend.

Decisão
Uso de Docker Compose para orquestração de containers e Nginx como Reverse Proxy.

Alternativas consideradas

Deploy Manual (Bare Metal): Difícil de replicar e manter (o famoso "na minha máquina funciona").

PaaS (Heroku/Vercel): Limitações no uso de bancos de dados persistentes ou custos ocultos.

Justificativa
O Docker garante que o ambiente de desenvolvimento seja idêntico ao de produção. Com o Docker Compose, subimos toda a stack (BD + Automação + Web) com um único comando, facilitando o cumprimento do prazo da Sprint 04.

Consequências

Positivas: Facilidade de backup; isolamento de processos; portabilidade total.

Negativas: Pequeno overhead de recursos (RAM/CPU) devido à camada de virtualização do Docker.