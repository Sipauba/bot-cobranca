# Integrações

## Oracle Database

Origem dos títulos financeiros e dos dados de cliente usados pelo workflow. Configure a Credential Oracle no n8n. O export sanitizado não contém host ou segredo.

## PostgreSQL

Armazena resultados de validação de telefone e estado operacional dos títulos. Configure a Credential PostgreSQL no n8n e prepare a tabela descrita em `banco-de-dados.md`.

## API de WhatsApp

O workflow usa requisições HTTP para verificar números e enviar mensagens. A exportação contém host e identificadores de instância mascarados e valores de autenticação substituídos. Configure URL, instância e autenticação por Credential no n8n.

Consulte `.env.example` para nomes de configuração de referência. Nenhuma variável tem valor preenchido.
