# Catálogo de indicadores (KPIs)

## Convenções
- Moeda: metical (MT).
- Período: data de realização da venda.
- Base de análise: vendas concluídas, ajustadas por devoluções válidas quando aplicável.
- A receita não é sinónimo de lucro.
- O lucro bruto não inclui despesas operacionais, juros ou impostos sobre o rendimento.
- Os preços/custos históricos são guardados nos itens de venda.

| KPI | Definição / fórmula | Unidade |
|---|---|---|
| Receita de vendas | Soma de quantidade × preço unitário histórico, menos descontos e devoluções aplicáveis | MT |
| Custo dos produtos vendidos | Soma de quantidade × custo unitário histórico, ajustada por devoluções aplicáveis | MT |
| Lucro bruto | Receita de vendas − custo dos produtos vendidos | MT |
| Margem bruta | (Lucro bruto ÷ receita de vendas) × 100, quando receita > 0 | % |
| Quantidade vendida | Soma das quantidades líquidas vendidas | Unidades |
| Número de vendas | Contagem distinta de identificadores de vendas concluídas | Vendas |
| Ticket médio | Receita de vendas ÷ número de vendas, quando número de vendas > 0 | MT/venda |
| Receita por loja | Receita de vendas agrupada por loja | MT |
| Receita mensal | Receita de vendas agrupada por mês | MT |

## Exemplo validado
Uma venda de 100 unidades a 500 MT cada, com custo unitário de 350 MT, produz receita de 50.000 MT, custo de 35.000 MT, lucro bruto de 15.000 MT e margem bruta de 30%.

## Cuidados analíticos
- Não contar linhas de itens como se fossem vendas distintas.
- Não somar o total de uma venda repetidamente ao juntar vendas e itens.
- Não confundir o total recebido em pagamentos com a receita reconhecida.
- Tratar divisões por zero como indicador não aplicável.
- Definir regras de devoluções, descontos e impostos antes dos cálculos finais.
