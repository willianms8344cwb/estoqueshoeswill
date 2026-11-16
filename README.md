# Estoque Shoes Will

Sistema web de gestão de estoque, vendas e logística para lojas de calçados e roupas.

## Objetivos

- Cadastrar produtos com SKU, código de barras, categoria, marca e fotos.
- Controlar variações de tamanho, cor, modelo e grade por produto.
- Registrar entradas, saídas, ajustes e transferências de estoque.
- Gerenciar vendas, pedidos, clientes, fornecedores e compras.
- Acompanhar separação, expedição e entrega de pedidos.
- Visualizar indicadores de vendas, estoque, custos e lucratividade.
- Manter usuários, permissões e trilha de auditoria.

## Estrutura do projeto

```text
src/                 Aplicação web (componentes, páginas, serviços e estilos)
modules/             Domínios de negócio
database/            Esquema e migrações do banco
docs/                Requisitos, arquitetura e modelo de dados
public/              Arquivos públicos e identidade visual
tests/               Testes unitários e de integração
```

## Princípios

1. O estoque é controlado por variante (produto + tamanho + cor + modelo).
2. Toda movimentação deve registrar motivo, data, usuário e quantidade.
3. Vendas e compras devem atualizar o estoque por meio de operações rastreáveis.
4. Valores monetários devem ser armazenados em centavos ou tipo decimal exato, nunca em ponto flutuante.
5. Dados sensíveis e credenciais nunca devem ser versionados.

## Começando

A base técnica e os comandos de desenvolvimento serão definidos na próxima etapa, junto com a escolha da stack e do provedor de banco de dados.

Consulte [requisitos](docs/requisitos.md), [arquitetura](docs/arquitetura.md) e [modelo de dados](docs/banco-de-dados.md).

## Status

Estrutura inicial do repositório. Funcionalidades de negócio ainda serão implementadas.
