# 3. Modelagem dos Processos de Negócio

## 3.1 Processo AS-IS

No cenário anterior, pedidos podem ser recebidos por WhatsApp, Instagram e aplicativos de entrega, enquanto registros de clientes, produtos, pagamentos e produção podem ficar separados entre conversas e planilhas. Essa fragmentação dificulta conferir os dados, calcular a necessidade de insumos e acompanhar todos os pedidos.

## 3.2 Processo TO-BE

No processo automatizado, o pedido é registrado no sistema, associado ao cliente e ao canal de venda e acompanhado por uma sequência controlada:

`AGUARDANDO_PAGAMENTO -> PAGO -> EM_PREPARO -> CONFERIDO -> SAIU_PARA_ENTREGA -> ENTREGUE`

Em paralelo, o sistema apresenta saldo e validade de ingredientes, gera necessidades de compra e permite registrar produção e recebimento.

## 3.3 Regras de negócio

- Cada pedido deve possuir um cliente, canal e pelo menos um item.
- A confirmação do pagamento é necessária para iniciar o preparo.
- A conferência exige checklist completo.
- A produção só é liberada quando há estoque suficiente.
- Cancelamentos exigem motivo e são limitados até etapas permitidas.
- Pedidos finalizados não podem voltar para etapas anteriores.

## 3.4 Processo 1: Venda por delivery

O processo inicia com o atendimento pelo WhatsApp, Instagram, iFood ou 99Food. O pedido é associado ao cliente, aos itens e, quando aplicável, à promoção. O pagamento pode ser confirmado manualmente por Pix. Em seguida, o pedido percorre as etapas previstas até a entrega.

As mensagens de atendimento são montadas pelo sistema a partir de modelos configuráveis e abertas no WhatsApp.

## 3.5 Processo 2: Gestão de estoque e reposição

Os ingredientes possuem saldo atual, estoque mínimo e validade mais próxima. Entradas e ajustes alteram o estoque, que é consultado pelo planejamento da produção. Ao liberar uma produção, o sistema confere as fichas técnicas e dá baixa nos ingredientes.

A lista de compras é gerada automaticamente para ingredientes abaixo do mínimo ou ausentes no planejamento. Cotação, compra e recebimento são registrados no fluxo de reposição.
