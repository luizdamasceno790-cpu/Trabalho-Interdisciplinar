# 2. Especificações do Projeto

## 2.1 Personas

### Administradora

- Responsável pelo atendimento e organização financeira.
- Necessita visualizar pedidos, confirmar pagamentos e acompanhar a entrega.

### Responsável pela produção

- Planeja produções e utiliza os insumos disponíveis.
- Precisa saber se há estoque suficiente antes de liberar uma produção.

### Responsável pelo estoque e compras

- Atualiza entradas e ajustes de ingredientes.
- Consulta itens em nível mínimo e registra recebimentos.

## 2.2 Histórias de usuário

| ID | História | Critério de aceitação |
|---|---|---|
| US01 | Como administradora, quero cadastrar um pedido | O pedido deve incluir cliente, canal, itens e promoção aplicável |
| US02 | Como administradora, quero acompanhar o status | A interface deve impedir transições inválidas |
| US03 | Como administradora, quero confirmar o pagamento | O pedido só deve seguir para preparo após confirmação |
| US04 | Como responsável pelo estoque, quero registrar entradas | O saldo do ingrediente deve ser atualizado |
| US05 | Como responsável pela produção, quero planejar um lote | O sistema deve verificar os insumos necessários |
| US06 | Como responsável pelas compras, quero gerar uma lista | Itens em nível baixo ou faltantes devem aparecer na lista |
| US07 | Como usuária, quero copiar mensagens do WhatsApp | A mensagem deve corresponder ao status atual do pedido |

## 2.3 Requisitos funcionais

- RF01: autenticar o usuário administrador.
- RF02: cadastrar, alterar, consultar e cancelar pedidos.
- RF03: controlar o fluxo de status dos pedidos.
- RF04: cadastrar clientes e produtos.
- RF05: cadastrar promoções e associá-las a pedidos.
- RF06: controlar estoque, entradas e ajustes.
- RF07: cadastrar receitas e planejar produções.
- RF08: baixar ingredientes automaticamente na produção.
- RF09: gerar e receber listas de compras.
- RF10: apresentar painel com indicadores e alertas.

## 2.4 Requisitos não funcionais

- RNF01: interface responsiva para computador e celular.
- RNF02: comunicação entre frontend e backend por API HTTP.
- RNF03: dados persistidos em SQLite.
- RNF04: senha armazenada com hash.
- RNF05: respostas de erro padronizadas.
- RNF06: Node.js 22.13 ou superior.
