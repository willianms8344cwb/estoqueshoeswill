# Modelo de dados conceitual

Este documento é conceitual, não uma migração executável.

- users, roles, permissions: identidade e acesso.
- products: nome, descrição, categoria, marca e status.
- product_variants: produto, SKU, código de barras, tamanho, cor, modelo, custo e preço.
- warehouses: depósito/loja.
- stock_balances: variante, depósito, disponível, reservado e versão.
- stock_movements: variante, origem/destino, tipo, quantidade, motivo, referência, autor e data.
- customers, suppliers: cadastros de clientes e fornecedores.
- sales, sale_items: pedido, cliente, vendedor, status, totais e itens.
- purchases, purchase_items: fornecedor, recebimento, custo e itens.
- shipments, shipment_events: entrega, transportadora, rastreio e eventos.
- payments, receivables, payables: financeiro, conforme escopo.
- audit_logs: ator, ação, entidade, data e metadados não sensíveis.

## Integridade
- UNIQUE(product_variants.sku); código de barras único quando informado.
- Movimentações confirmadas são append-only; saldo deve ser reconciliável.
- Venda e movimentação/reserva de estoque na mesma transação.
- Dinheiro em centavos (inteiro) ou NUMERIC/DECIMAL, nunca float.
- Chaves estrangeiras e índices em SKU, código de barras, status e datas.
- Dados pessoais com acesso restrito, retenção e anonimização conforme LGPD.
