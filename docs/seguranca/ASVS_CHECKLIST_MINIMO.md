V2.1 (Autenticação): Garantir que todas as requisições ao BI exijam token JWT.

V4.1 (Controle de Acesso): Somente perfis "Coordenador" podem visualizar métricas financeiras ou de performance de técnicos.

V5.1 (Validação): Sanitização de inputs no campo de "Descrição" para evitar Stored XSS.

[OK] Senhas não são armazenadas em texto plano (BCrypt no banco).

[OK] Logout invalida o token JWT no lado do cliente.

[OK] Limite de tamanho para upload de fotos para evitar estouro de armazenamento na VPS.