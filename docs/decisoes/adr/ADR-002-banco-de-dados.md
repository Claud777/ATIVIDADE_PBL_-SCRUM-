ADR-002 — Persistência e Estrutura de Dados (BI)
Status: Aceito

Data: 28/04/2026

Decisores: Claud

Contexto
O sistema precisa armazenar históricos, fotos (links) e metadados para gerar relatórios de "laboratórios problemáticos" e "tempo médio de atendimento".

Decisão
Uso do PostgreSQL como banco de dados principal.

Alternativas consideradas

MongoDB: Bom para JSON, mas dificulta relatórios relacionais complexos (JOINs) necessários para o BI do coordenador.

SQLite: Leve, mas limitado para acessos concorrentes e escalabilidade futura.

Justificativa
O PostgreSQL é o padrão ouro para dados relacionais open source. Sua capacidade de lidar com campos JSONB permite que o output do Open Claw seja armazenado de forma flexível, mantendo a integridade referencial para os relatórios de BI.

Consequências

Positivas: Consultas performáticas para o dashboard; suporte nativo a tipos de dados complexos.

Negativas: Exige maior configuração de memória na VPS em comparação ao SQLite.