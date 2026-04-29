Sprint 01 — Fundação e Captura de Dados
Sprint Goal: Estabelecer a infraestrutura básica e permitir que um usuário abra um chamado com sucesso.

Itens Selecionados (Sprint Backlog):

Configuração do ambiente Docker (PostgreSQL + Nginx + Open Claw).

Modelagem visual do banco de dados (BR Modelo) e conversão para SQL.

Criação da interface de "Abertura de Chamado" em Flutter Web (Responsivo).

Implementação do upload de anexo (foto do problema).

Daily (Resumo):

Dia 1: Definida a estrutura de pastas conforme o dossiê. Impedimento: ajuste de permissão no Docker.

Dia 3: Concluída a integração do Flutter com o Open Claw para envio do JSON inicial.

Review: Demonstração do formulário mobile funcionando. O chamado é salvo no banco, mas ainda sem triagem automática.

Retrospective:

Ponto Positivo: O uso do Open Claw agilizou a recepção dos dados.

Melhoria: A modelagem SQL precisou de ajustes para suportar o campo de fotos (blob vs link).