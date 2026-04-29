![[C4-CONTAINERS.png]]

**Detalhamento dos Containers:**

1. **Web App (Flutter Web):**
    
    - **Papel:** Interface do usuário responsiva.
        
    - **Responsabilidade:** Coleta de dados do chamado, exibição do dashboard de BI e autenticação via JWT.
        
    - **Interação:** Envia comandos e recebe dados do Open Claw via HTTPS/JSON.
        
2. **Motor de Automação (Open Claw):**
    
    - **Papel:** Backend Orquestrador.
        
    - **Responsabilidade:** Receber o JSON do frontend, aplicar regras de prioridade (ex: se o laboratório for o 'Lab 04', prioridade = alta), e gerenciar o fluxo de status.
        
    - **Interação:** Lê e escreve dados no PostgreSQL.
        
3. **Banco de Dados (PostgreSQL):**
    
    - **Papel:** Persistência de Dados.
        
    - **Responsabilidade:** Armazenar usuários, logs de chamados, anexos (caminhos de arquivos) e métricas de tempo de atendimento.
        
4. **Servidor de Arquivos/Proxy (Nginx):**
    
    - **Papel:** Entrada e Segurança.
        
    - **Responsabilidade:** Servir os arquivos estáticos do Flutter e atuar como Proxy Reverso para o Open Claw, garantindo o uso de HTTPS.