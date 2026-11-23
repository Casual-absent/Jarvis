Jarvis — Security Policy

1. Security Principles

- Privacy by default.
- Minimum necessary permissions.
- User control over sensitive actions.
- Secure storage of credentials and personal data.
- Transparent handling of data.
- Security before convenience.

2. Secrets and Credentials

- Never hardcode API keys, passwords, tokens or private credentials into source code.
- Never commit secrets to Git.
- Never expose secrets in logs, screenshots, error reports or AI prompts unnecessarily.
- Use appropriate secure storage mechanisms.
- Provide a way to remove or replace stored credentials.

3. AI Security

- Treat AI-generated output as untrusted.
- Validate arguments before executing tools.
- Treat webpages, messages, files and app content as untrusted input.
- Protect against prompt injection.
- Never allow external content to independently authorize actions.
- Prevent unnecessary disclosure of personal memory or credentials to providers.

4. Authorization

Require explicit user authorization when appropriate for:

- Sending messages or emails.
- Making purchases or payments.
- Deleting important data.
- Changing security or account settings.
- Sharing personal information.
- Executing high-risk device actions.

Authorization must not be bypassed by AI-generated instructions.

5. Android Permissions

- Request permissions only when needed.
- Explain the purpose of sensitive permissions.
- Respect Android permission revocation.
- Respect accessibility and overlay consent.
- Never silently bypass Android security mechanisms.
- Do not assume root access.

6. Memory and Personal Data

- Store only information that provides meaningful value.
- Avoid unnecessary sensitive data collection.
- Allow users to inspect, correct and delete stored memories.
- Avoid storing passwords, authentication codes or payment credentials in AI memory.
- Protect local databases and backups where appropriate.

7. Network Security

- Use HTTPS for network communications wherever supported.
- Validate external data.
- Handle authentication securely.
- Avoid insecure connections.
- Handle network failures safely.
- Never expose internal credentials through external requests.

8. Logging

- Avoid logging personal information.
- Redact credentials and tokens.
- Keep diagnostics minimal.
- Never expose sensitive data through debug logs.

9. Security Review

Security-sensitive features must be reviewed before merging.

Review areas include:

- Permissions.
- Credential handling.
- Data storage.
- Network requests.
- Accessibility actions.
- AI tool execution.
- External integrations.
- Destructive operations.

10. Reporting Vulnerabilities

Security vulnerabilities should be reported privately to the repository owner rather than publicly disclosed before appropriate review.

11. Security Is Continuous

Security is not a one-time feature.

Every new capability, integration, permission and architectural change must be evaluated for potential security implications.
