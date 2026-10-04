# Melhorias futuras

Estas sugestões não alteram a lógica do workflow sanitizado:

- Revisar as consultas SQL e parametrizar valores interpolados para reduzir risco de SQL injection e problemas de aspas.
- Definir constraints e uma chave de idempotência para evitar registros ou envios duplicados em execuções concorrentes.
- Atualizar o estado de notificação por título/cliente específico, evitando atualização ampla de todos os registros elegíveis.
- Adicionar tratamento explícito de falhas, retries limitados e tratamento de respostas da API.
- Configurar rate limiting conforme os limites do provedor de WhatsApp.
- Adicionar logs sem dados pessoais, métricas e alertas para falhas e filas paradas.
- Remover duplicação entre trilhas quando a configuração por contexto permitir reutilização segura.
- Centralizar endpoints e parâmetros de ambiente em configuração protegida do n8n.
- Validar consentimento, horário permitido e política de retenção aplicável às mensagens.
