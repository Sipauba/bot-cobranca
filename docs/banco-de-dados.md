# Banco de dados

O Oracle é a origem dos títulos e cadastros. O PostgreSQL mantém o controle operacional em uma estrutura semelhante a `bot_cobranca`.

Campos observados no workflow:

| Campo | Uso geral |
|---|---|
| `codcli` | Identificador do cliente na origem |
| `cliente` | Nome associado ao título |
| `telcob` | Telefone de cobrança normalizado |
| `duplic` | Identificador do título |
| `numvalido` | Resultado da validação de WhatsApp |
| `notificado` | Estado de envio da notificação |
| `datanotificado` | Data usada pelo controle do fluxo |
| `tipocobranca` | Categoria/regra de cobrança |

Este repositório não inclui resultados reais nem um dump do banco. Tipos, índices, constraints e estratégia de retenção devem ser definidos pelo responsável pelo ambiente. Os filtros comerciais na cópia do workflow são ilustrativos e precisam ser configurados.
