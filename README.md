# n8n Self-Hosted Setup (AWS Free Tier + HTTPS)

Setup genérico para rodar o **n8n** em uma instância **AWS EC2 gratuita**, com **HTTPS automático (Let's Encrypt)** via **Caddy**.

## 🧱 Estrutura
- `docker-compose.yml` — define os containers (n8n + Caddy)
- `Caddyfile` — proxy reverso com HTTPS automático
- `.env` — credenciais e domínio local (não versionar)
- `.env.example` — modelo de exemplo
- `.gitignore` — protege dados sensíveis e volumes persistentes

## 🚀 Como usar
```bash
cp .env.example .env
# Edite o arquivo .env e preencha:
# N8N_DOMAIN=seu-dominio.duckdns.org
docker-compose up -d
```

## 🔒 Segurança
- Painel web protegido por usuário/senha (`N8N_USER`, `N8N_PASS`)
- HTTPS válido via Let's Encrypt
- Credenciais criptografadas com `N8N_KEY`
