# Project Rules

## Public Repository — No Sensitive Information

This is a **public GitHub repository**. All code, configuration, and documentation must be safe for public consumption.

### Hard Rules

1. **No secrets or credentials** — Never commit API keys, tokens, passwords, private keys, or any authentication material. Use environment variables or a `.env` file (which is git-ignored) instead.
2. **No personal information** — Do not include real names, email addresses, phone numbers, physical addresses, IP addresses, account IDs, or any other PII in code, comments, config, or documentation.
3. **No internal/private URLs** — Do not reference internal network addresses, private endpoints, or intranet URLs.
4. **No hardcoded environment-specific values** — Hostnames, database connection strings, file paths containing usernames (e.g., `/Users/abhilash/...`) must never appear in committed code. Use relative paths or environment variables.
5. **Use placeholder values in examples** — When documentation or sample configs require values, use obvious placeholders like `YOUR_API_KEY_HERE`, `user@example.com`, `192.168.x.x`, etc.

### Best Practices

- Always reference secrets via environment variables (e.g., `os.environ["API_KEY"]`).
- Use `.env` files for local development and ensure `.env` is in `.gitignore`.
- Before committing, review diffs for any accidentally included sensitive data.
- If a secret is accidentally committed, rotate it immediately — git history preserves it even after removal.
