# Segurança

- Nunca versione tokens, API keys, senhas ou arquivos de credenciais.
- Guarde senhas em Credentials do n8n; use variáveis de ambiente quando adequado.
- Mantenha arquivos `.env` fora do Git; o `.env.example` contém somente chaves vazias.
- Não inclua telefones de clientes nem resultados reais de banco no repositório.
- Audite toda exportação de workflow antes de publicar, inclusive Code nodes, URLs, headers, metadados, nomes de Credential e comentários SQL.
- Restrinja o acesso às credenciais e use ambientes de teste para validar alterações.
- Execute ferramentas de detecção de segredos, como [gitleaks](https://github.com/gitleaks/gitleaks), antes de publicar.

Caso uma credencial seja exposta, revogue e rotacione a credencial e remova o segredo do histórico Git antes da publicação.
