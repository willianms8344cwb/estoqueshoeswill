# Requisitos do produto

## Produtos
- Cadastro de calçados, roupas e acessórios com SKU, código de barras, categoria, marca, descrição, custo, preço e fotos.
- Variantes por tamanho, cor e modelo; cada variante possui SKU único e saldo próprio.

## Estoque
- Saldo por variante e depósito/local.
- Entradas por compra, devolução e ajuste; saídas por venda, perda e ajuste.
- Transferências, inventário físico, estoque mínimo e alertas de reposição.
- Bloqueio de saldo negativo por padrão; histórico imutável e auditável.

## Vendas e pedidos
- Orçamentos, pedidos, vendas, itens, descontos, frete e pagamentos.
- Reserva/baixa de estoque transacional, cancelamentos e devoluções rastreáveis.

## Compras e cadastros
- Fornecedores, pedidos de compra, recebimento parcial/total e custo de aquisição.
- Clientes e histórico de compras com minimização de dados pessoais.

## Logística
- Separação, embalagem, expedição, retirada e entrega com status, responsável, data e rastreio.

## Financeiro e relatórios
- Contas a pagar/receber a definir; receita, custo, margem, ticket médio, giro, ruptura e curva ABC.

## Segurança e qualidade
- Autenticação, papéis/permissões, auditoria, backup e controles LGPD.
- Interface responsiva em pt-BR; validação no servidor; paginação e testes automatizados.
- Valores monetários em centavos ou decimal exato; operações idempotentes e transacionais.

## Critérios de aceite
1. Saldo deve reconciliar com o ledger de movimentações.
2. Reenvio de venda não pode baixar estoque duas vezes.
3. Toda alteração de saldo registra origem, autor, data e motivo.
4. Devolução referencia a venda original e gera movimento compensatório.
5. Consulta filtra por produto, SKU, tamanho, cor e depósito.
