# Arquitetura inicial

A interface começa com React, TypeScript e Vite. Backend, API, banco de dados e autenticação serão escolhidos antes da persistência real. O painel atual é demonstrativo e não contém dados reais.

## Organização
- src/components: componentes reutilizáveis
- src/pages: páginas e rotas
- src/layouts: estruturas visuais
- src/hooks: hooks React
- src/services: API e integrações
- src/contexts: estado compartilhado
- src/utils: utilitários e formatação
- src/styles: estilos e tokens
- modules: domínios de negócio
- database: esquema e migrações
- tests: testes unitários e integração

## Diretrizes
- Separar interface, aplicação, domínio e infraestrutura.
- Validar regras críticas no servidor; validação de tela não é segurança.
- Ledger de estoque append-only; corrigir com lançamentos compensatórios.
- Confirmar venda e reserva/baixa em transação, com controle de concorrência.
- Nunca versionar credenciais; definir backup e observabilidade antes de produção.

## Decisões pendentes
1. Backend e banco (ex.: API Node.js + PostgreSQL).
2. Provedor de autenticação e matriz de permissões.
3. Operação com um ou vários depósitos/lojas.
4. Política de reserva e baixa de estoque.
5. Integrações fiscais, pagamentos e transportadoras.
