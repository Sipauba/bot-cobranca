# Fluxo de cobrança

1. Consultar títulos vencendo e sem baixa no Oracle.
2. Normalizar o telefone do cadastro do cliente.
3. Consultar a API para verificar se o número possui WhatsApp.
4. Gravar o resultado no PostgreSQL, incluindo dados de controle do título.
5. Selecionar títulos válidos ainda não notificados na data e categoria atual.
6. Consultar novamente o título no Oracle antes de montar a cobrança.
7. Gerar uma mensagem escolhida entre variações disponíveis.
8. Enviar itens em lote, aguardando um intervalo entre mensagens.
9. Atualizar o estado de notificação no PostgreSQL.

Os filtros de filial e códigos de cobrança aparecem como valores fictícios no SQL sanitizado. Reveja-os e ajuste as regras ao ambiente autorizado antes da execução. As mensagens de exemplo estão em `examples/mensagens-exemplo.md`.
