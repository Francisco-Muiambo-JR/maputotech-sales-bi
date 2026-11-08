# Requisitos — versão preliminar

## Funcionais
| ID | Requisito | Prioridade | Critério de aceitação |
|---|---|---|---|
| RF01 | Consultar vendas por período | Alta | Filtrar por intervalo de datas e obter totais consistentes |
| RF02 | Comparar lojas | Alta | Visualizar receita e lucro bruto por loja |
| RF03 | Analisar produtos e categorias | Alta | Ordenar por receita, quantidade e lucro bruto |
| RF04 | Calcular KPIs comerciais | Alta | Fórmulas documentadas e resultados testáveis |
| RF05 | Analisar pagamentos | Média | Apresentar valores por método sem duplicar receita de vendas |
| RF06 | Detectar problemas de qualidade | Alta | Identificar duplicados, nulos críticos e valores inválidos |
| RF07 | Exportar resultados | Média | Permitir exportação de tabelas de indicadores |
| RF08 | Considerar estados de venda | Alta | Excluir cancelamentos e tratar devoluções segundo regras definidas |

## Não funcionais
| ID | Requisito | Critério de aceitação |
|---|---|---|
| RNF01 | Reprodutibilidade | Scripts e instruções permitem repetir o processamento |
| RNF02 | Integridade | Chaves e verificações impedem referências inválidas |
| RNF03 | Rastreabilidade | Manter dados de origem e documentar transformações |
| RNF04 | Clareza | Nomes, unidades e definições dos KPIs são visíveis |
| RNF05 | Privacidade | Não publicar dados pessoais reais; usar dados simulados |
| RNF06 | Manutenção | Separar extracção, transformação, consultas e visualização |

## Fora do âmbito inicial
Gestão de stock operacional, facturação fiscal, cálculo de lucro líquido, integração com sistemas reais e previsões de vendas.

## Pendências para validação
- Definir regras detalhadas de devoluções parciais e descontos;
- Definir se impostos estão incluídos nos preços;
- Definir como conciliar pagamentos parcelados;
- Definir tratamento de vendas com data/hora inválida.
