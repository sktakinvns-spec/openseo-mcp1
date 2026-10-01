# Security

- Never commit a real OpenSEO API key.
- Never commit Google OAuth/client secrets, GSC credentials, WordPress passwords, application passwords, or access tokens.
- Prefer OpenSEO OAuth login for interactive clients.
- For CI/headless use, store `OPENSEO_API_KEY` in an encrypted secrets store.
- If a credential is accidentally committed, revoke/rotate it immediately.
