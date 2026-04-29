ADR-003 — Estratégia de Autenticação e Autorização
Status: Aceito

Data: 28/04/2026

Decisores: Claud

Contexto
O sistema possui três níveis de acesso (Solicitante, Técnico e Coordenador). É necessário garantir que um aluno não visualize métricas de produtividade dos técnicos ou altere chamados alheios.

Decisão
Implementação de JWT (JSON Web Tokens) com controle de acesso baseado em funções (RBAC).

Alternativas consideradas

Firebase Auth: Fácil implementação, mas introduz uma dependência externa que pode gerar custos se o volume crescer.

Sessions (Cookies): Mais complexo de gerenciar em arquiteturas desacopladas (Frontend vs Motor de Automação).

Justificativa
O JWT permite uma comunicação stateless entre o Flutter Web e os serviços de backend/Open Claw, facilitando o deploy em containers e garantindo a segurança mínima exigida pela LGPD.

Consequências

Positivas: Escalabilidade; segurança robusta para os perfis de usuário.

Negativas: Necessidade de gerenciar a expiração e o refresh dos tokens no frontend.