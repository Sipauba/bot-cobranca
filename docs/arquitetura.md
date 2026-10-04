# Arquitetura

O n8n coordena duas trilhas de cobrança semelhantes. Cada trilha consulta títulos no Oracle, normaliza o telefone, consulta a API de WhatsApp e grava o resultado da validação no PostgreSQL. Os títulos elegíveis seguem para reconsulta, composição de mensagem e envio em lote com espera entre itens. Ao final, o PostgreSQL recebe a atualização do estado de notificação.

```mermaid
flowchart LR
    O[(Oracle)] --> Q[Consulta e filtros]
    Q --> N[Normalização BR]
    N --> W{WhatsApp disponível?}
    W -->|Sim| PV[(PostgreSQL: válido)]
    W -->|Não| PI[(PostgreSQL: inválido)]
    PV --> R[Reconsulta do título]
    R --> M[Mensagem dinâmica]
    M --> L[Lote]
    L --> D[Delay]
    D --> API[API WhatsApp]
    API --> U[(PostgreSQL: notificado)]
```

Os endpoints e alguns filtros comerciais foram substituídos por placeholders no workflow deste repositório. Consulte `docs/fluxo-cobranca.md` antes de adaptar a execução.
