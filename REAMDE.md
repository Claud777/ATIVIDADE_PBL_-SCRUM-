🛠️ SGL-Lab: Sistema de Gestão de Laboratórios de TI
Status do Projeto: MVP Funcional (Simulação Acadêmica) 🚀

Prazo de Desenvolvimento: 4 Sprints (1 mês)

Este projeto foi desenvolvido para solucionar a falta de controle e previsibilidade na manutenção dos laboratórios de TI do campus. Utilizando o motor de automação Open Claw e um dashboard responsivo em Flutter Web, transformamos solicitações informais em uma operação orientada a dados e SLAs.

📋 Sumário do Projeto
Visão Geral

Arquitetura e Tecnologias

Estrutura do Repositório

Como Executar (Simulação)

Documentação Completa

🌟 Visão Geral
O SGL-Lab permite que professores e alunos abram chamados rapidamente via web, anexem evidências fotográficas e acompanhem o status em tempo real. Para a coordenação, o sistema oferece um Dashboard de BI que identifica os laboratórios com maior índice de falhas e calcula o tempo médio de atendimento (TMA).

Métrica Principal: Redução do tempo de resposta inicial para menos de 4 horas úteis.

🏗️ Arquitetura e Tecnologias
O projeto segue os princípios de Clean Architecture e desacoplamento entre interface e motor de regras.

Frontend: Flutter Web (Interface Responsiva)

Motor de Automação: Open Claw (Triagem, Priorização e Fluxo)

Banco de Dados: PostgreSQL (Persistência e BI)

Infraestrutura: Docker & Nginx (Containerização)

📁 Estrutura do Repositório
Seguindo os requisitos da atividade, o repositório está organizado da seguinte forma:

Plaintext
/
├── README.md                 <-- Você está aqui
├── /docs/                    <-- Documentação técnica e estratégica
│   ├── DOSSIE_DO_PROJETO.md  <-- Resumo, requisitos e matrizes
│   ├── /discovery/           <-- Logs de aprendizado e evidências
│   ├── /decisoes/            <-- ADRs e Matriz Tecnológica
│   ├── /arquitetura/         <-- Diagramas C4 (Contexto e Container)
│   ├── /seguranca/           <-- Checklist OWASP ASVS
│   └── /sprints/             <-- Registros de cerimônias Scrum
└── /src/                     <-- Código-fonte simulado do MVP
🚀 Como Executar (Simulação)
Para rodar a stack completa na sua máquina local ou VPS, utilizamos Docker Compose para garantir que todas as dependências (Banco, Automação e Web) subam corretamente.

Clone o repositório:

Bash
git clone https://github.com/seu-usuario/sgl-lab.git
cd sgl-lab
Suba os containers:

Bash
docker-compose up -d
Acesse as interfaces:

Dashboard Web: http://localhost:8080

Painel Open Claw: http://localhost:9000

📂 Documentação Completa
Para uma compreensão profunda das decisões de engenharia e do processo ágil, acesse os links abaixo:

📖 Dossiê do Projeto: Requisitos, User Stories e Matriz de Decisão.

🏗️ Arquitetura C4: Como o sistema foi desenhado.

📜 Registros de Sprint: O que foi feito em cada etapa do Scrum.

🛡️ Checklist de Segurança: Controles aplicados contra vulnerabilidades.

Nota Crítica: Este projeto foi desenvolvido sob a premissa de custo zero de licenciamento, priorizando ferramentas Open Source e agilidade na entrega do MVP.