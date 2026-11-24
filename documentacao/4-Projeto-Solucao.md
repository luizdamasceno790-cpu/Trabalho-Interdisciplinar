# 4. Projeto da Solução

## 4.1 Arquitetura

A aplicação possui arquitetura cliente-servidor:

- Frontend em React, Vite e TypeScript.
- Backend em Node.js e Express.
- Banco SQLite persistido em `codigo-fonte/backend/data`.
- API REST disponível no prefixo `/api/v1`.

## 4.2 Tecnologias

| Camada | Tecnologia |
|---|---|
| Interface | React 19, React Router e TypeScript |
| API | Node.js e Express 5 |
| Banco | SQLite embutido no Node.js |
| Autenticação | JSON Web Token e bcryptjs |
| Build | Vite |

## 4.3 Segurança

O backend protege rotas com token JWT, exceto o endpoint de login. Senhas são armazenadas com hash. A configuração sensível fica em variáveis de ambiente e não deve ser enviada ao repositório.

## 4.4 Módulos

- Autenticação e configuração.
- Clientes e cardápio.
- Pedidos e promoções.
- Estoque e compras.
- Receitas e produção.
- Painel e indicadores.

## 4.5 Evidências da implementação

A aplicação entregue contempla telas de login, painel, pedidos, clientes, cardápio, promoções, estoque, receitas, produção, compras e configurações.

O banco SQLite contém 19 tabelas relacionadas. Os registros principais incluem clientes, pedidos, itens, histórico de status, produtos, ingredientes, receitas, compras e usuários.

Os testes automatizados cobrem autenticação, cadastros básicos, fluxo completo de pedidos, regras de status, estoque, produção, compras, promoções e painel.
