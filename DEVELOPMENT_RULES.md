Jarvis — Development Rules

1. Development Strategy

- Develop Jarvis incrementally.
- Prioritize working, tested features over large unverified changes.
- Keep the app buildable after each milestone.
- Avoid unnecessary rewrites.
- Prefer simple, maintainable solutions.
- Do not implement features merely to imitate other assistants.

2. Code Standards

- Follow the conventions of the existing project.
- Avoid duplicate implementations.
- Keep modules reasonably separated.
- Use clear names.
- Handle errors explicitly.
- Avoid unnecessary dependencies.
- Verify dependency versions before introducing them.

3. Android Standards

- Use APIs compatible with the project's supported Android versions.
- Document new permissions and explain why they are needed.
- Respect Android background execution limits.
- Respect accessibility and overlay permission boundaries.
- Do not assume root, Shizuku or privileged access.
- Avoid battery-intensive background services where possible.
- Test on a real device whenever practical.

4. AI Integration

- Use a provider-independent model architecture.
- Avoid hardcoding one AI provider into core logic.
- Protect API keys and authentication data.
- Handle rate limits, network failures and timeouts.
- Never assume model output is trustworthy.
- Validate AI-generated tool arguments before execution.
- Require appropriate authorization for sensitive actions.

5. User Experience

- Conversation remains the primary interface.
- Avoid unnecessary dashboards and complicated navigation.
- Keep interactions responsive.
- Provide understandable loading, error and success states.
- Do not silently fail.
- Do not interrupt the user unnecessarily.

6. Memory

- Memory must be controllable by the user.
- Avoid storing sensitive information unnecessarily.
- Distinguish factual memories from assumptions.
- Allow correction and deletion.
- Do not treat untrusted content as instructions.

7. Testing

Every feature should have an appropriate testing strategy.

- Unit tests where practical.
- Build verification.
- Permission testing.
- Error handling tests.
- Real-device testing for Android-specific behavior.
- Regression testing for existing features.

If testing is unavailable, clearly state what remains unverified.

8. Git Workflow

- Use feature branches.
- Keep commits focused.
- Use descriptive commit messages.
- Never overwrite unrelated changes.
- Use pull requests for review.
- Do not merge unverified changes.

9. Documentation

Document:

- New features.
- Architecture changes.
- Dependencies.
- Permissions.
- Configuration.
- Limitations.
- Testing procedures.

10. Rule for AI Agents

Before implementation, understand the existing codebase.

Do not guess file structures, APIs, dependency versions or project behavior.

If a technical decision could significantly affect architecture, security, compatibility or future development, explain the trade-offs before proceeding.

The goal is a reliable, maintainable and genuinely useful Android assistant.
