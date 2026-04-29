Decisão 1: Framework Frontend (Dashboard Web):

|**Critério (Peso)**|**Opção A: React**|**Opção B: Flutter Web**|**Evidência/Observação**|
|---|---|---|---|
|Prazo (4)|4|5|Time já possui experiência em Flutter (conforme Perfil).|
|Domínio do time (5)|2|5|Curva de aprendizado nula para a equipe atual.|
|Custo/Licença (3)|5|5|Ambos Open Source.|
|Manutenibilidade (3)|4|5|Facilidade em manter UI consistente (Design System).|
|**Total Ponderado**|**53**|**75**|**Vencedor: Flutter Web**|
Decisão 2: Banco de Dados (BI e Histórico):

|**Critério (Peso)**|**Opção A: PostgreSQL**|**Opção B: MongoDB**|**Evidência/Observação**|
|---|---|---|---|
|Prazo (4)|5|4|SQL é mais rápido para gerar relatórios complexos.|
|Domínio do time (5)|5|3|Equipe domina modelagem relacional.|
|Custo/Licença (3)|5|5|Ambos possuem versões gratuitas.|
|Desempenho em VPS (2)|4|3|Postgres é mais estável em máquinas de baixa RAM.|
|**Total Ponderado**|**68**|**51**|**Vencedor: PostgreSQL**|
Decisão 3: Motor de Automação/Integração:

|**Critério (Peso)**|**Opção A: Open Claw**|**Opção B: Código Puro (Node/Express)**|**Evidência/Observação**|
|---|---|---|---|
|Prazo (4)|5|2|Open Claw já possui módulos de triagem prontos.|
|Custo (3)|5|5|Ambos custo zero.|
|Flexibilidade (2)|3|5|Código puro é mais flexível, mas demanda tempo.|
|Integração (3)|5|4|Open Claw foca em fluxos de dados JSON.|
|**Total Ponderado**|**56**|**45**|**Vencedor: Open Claw**|