# Modelo de dados relacional — proposta inicial

## Granularidade
- `venda`: uma linha por transacção comercial.
- `item_venda`: uma linha por produto distinto incluído numa venda (ou por linha comercial, caso o mesmo produto apareça mais de uma vez).
- `pagamento`: uma linha por pagamento associado a uma venda.

## Entidades e chaves
| Entidade | Chave primária | Chaves estrangeiras | Atributos principais |
|---|---|---|---|
| `loja` | `id_loja` | — | nome, localizacao |
| `categoria` | `id_categoria` | — | nome |
| `produto` | `id_produto` | `id_categoria` | nome, codigo_produto |
| `cliente` | `id_cliente` | — | identificador anonimizado (opcional) |
| `venda` | `id_venda` | `id_loja`, `id_cliente` (opcional) | data_venda, estado |
| `item_venda` | `id_item_venda` | `id_venda`, `id_produto` | quantidade, preco_unitario, custo_unitario, desconto |
| `metodo_pagamento` | `id_metodo_pagamento` | — | descricao |
| `pagamento` | `id_pagamento` | `id_venda`, `id_metodo_pagamento` | valor_pago, data_pagamento, estado |

## Relacionamentos
- Uma `loja` possui muitas `venda` (1:N).
- Uma `venda` possui muitos `item_venda` (1:N).
- Um `produto` pode aparecer em muitos `item_venda` (1:N).
- Uma `categoria` possui muitos `produto` (1:N).
- Uma `venda` pode ter muitos `pagamento` (1:N).
- Um `metodo_pagamento` pode ser utilizado em muitos `pagamento` (1:N).
- Um `cliente` pode ter muitas `venda` (1:N), sendo a identificação opcional.

## Regras de integridade propostas
- `quantidade > 0` para itens de venda normais;
- `preco_unitario >= 0`, `custo_unitario >= 0`;
- `desconto >= 0` e não superior ao valor bruto do item;
- chaves estrangeiras devem referenciar registos existentes;
- identificadores de venda devem ser globalmente únicos, mesmo quando originados em lojas distintas.

## Observações
- O preço e o custo de cada item são históricos e não devem ser recalculados com base no preço actual do produto.
- Cancelamentos, devoluções parciais e regras fiscais serão especificados antes de implementar o processamento.
- Este é um modelo preliminar, sujeito a revisão e testes na próxima fase técnica.
