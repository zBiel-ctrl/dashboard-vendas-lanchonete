# Dicionário de Dados — Projeto Operação de Lanchonete (dados fictícios)

Dataset fictício simulando a operação de uma unidade de fast food ao longo de 2025,
inspirado em métricas reais de gestão de loja (turnos, canais de venda, atendimento e satisfação).

## Arquivo: `vendas_lanchonete_2025.csv`
Uma linha = um canal de venda, em um turno, em um dia específico. (3.285 linhas)

| Coluna | Tipo | Descrição |
|---|---|---|
| data | data (AAAA-MM-DD) | Dia da venda |
| dia_semana | texto | Segunda a Domingo |
| turno | texto | Manhã, Tarde ou Noite |
| canal | texto | Salão, Drive-Thru ou Delivery/App |
| pedidos | inteiro | Quantidade de pedidos naquele turno/canal |
| faturamento | decimal (R$) | Faturamento total do turno/canal |
| ticket_medio | decimal (R$) | Faturamento ÷ pedidos |
| tempo_medio_atendimento_min | decimal | Tempo médio de atendimento, em minutos |
| funcionarios_no_turno | inteiro | Nº de funcionários escalados no turno (mesmo valor para os 3 canais do turno) |
| avaliacao_media_cliente | decimal (1–5) | Nota média de satisfação do cliente naquele turno/canal |

## Arquivo: `funcionarios.csv`
Uma linha = um funcionário fictício. (30 linhas) — usar para praticar JOIN com a tabela de vendas
(ex: relacionar `turno_padrao` com `turno`).

| Coluna | Tipo | Descrição |
|---|---|---|
| funcionario_id | inteiro | Identificador único |
| nome | texto | Nome fictício |
| cargo | texto | Atendente, Cozinha, Líder de Turno ou Gerente de Turno |
| turno_padrao | texto | Turno em que o funcionário costuma trabalhar |
| data_admissao | data | Data de admissão fictícia |
| avaliacao_desempenho | decimal (1–5) | Nota de desempenho interno |

## Padrões propositalmente embutidos nos dados (para você "descobrir" e contar essa história no post)
- Fins de semana (sexta, sábado, domingo) têm volume de pedidos maior.
- Dezembro/Janeiro têm faturamento mais alto; Junho/Julho são mais fracos (sazonalidade).
- Há uma leve tendência de crescimento de pedidos ao longo do ano.
- Turnos com **menos funcionários** tendem a ter **tempo médio de atendimento maior**.
- Tempo de atendimento maior tende a puxar a **avaliação do cliente para baixo**.
- Delivery/App tem ticket médio mais alto, mas tempo de preparo maior que Drive-Thru.
