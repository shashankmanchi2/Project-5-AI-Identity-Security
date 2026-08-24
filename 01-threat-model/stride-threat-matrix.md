# STRIDE Threat Matrix – SecureNova AI Identity Security

## Scope

This matrix applies STRIDE analysis to the major identity flows in the SecureNova AI platform.

### Identity Types
- Human User
- AI Agent
- OAuth M2M Client
- LLM API Key
- RAG Pipeline Service Identity
- MCP Server Identity

---

## STRIDE Matrix

| Identity / Flow | Spoofing | Tampering | Repudiation | Information Disclosure | Denial of Service | Elevation of Privilege |
|---|---|---|---|---|---|---|
| Human User → AI Chat | Stolen credentials or session token used to impersonate user | User request or identity claims modified in transit | User denies submitting a request if audit logs are incomplete | User data or JWT claims exposed through prompt injection | Repeated login/chat requests exhaust resources | User manipulates authorization to obtain admin functions |
| AI Agent → Internal REST APIs | Forged agent identity or stolen agent token | Agent API request or authorization claims modified | Agent actions cannot be attributed without
