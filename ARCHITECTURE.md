Jarvis Architecture

Status

Initial architectural direction. Implementation must be validated against the chosen Android codebase and platform constraints.

Design Goals

- Conversation-first, without a mandatory tool dashboard.
- Modular and testable capabilities.
- Model-provider agnostic.
- User-controlled permissions and sensitive actions.
- Verify actions and report outcomes.
- Keep secrets out of prompts, logs and source control.
- Build incrementally.

Layers

1. Experience Layer

Conversation UI, voice, floating interface, notifications and settings. All entry points should share the same conversation and task context.

2. Assistant Orchestration

Conversation state, intent interpretation, planning, capability selection, execution coordination, retries and user-facing reporting.

3. Model Gateway

Provider adapters, model selection, capability metadata, fallback policy, timeouts and cost controls.

4. Memory and Knowledge

Conversation summaries, user-approved preferences, project notes, searchable records and connections between memories. Memory must be inspectable, editable and deletable.

5. Capability Modules

Independent modules with declared permissions, inputs, outputs and risk levels.

Examples:

- Android interaction
- Research
- Calendar
- Messaging
- Files
- Reminders
- Security assistance

6. Android Platform Bridge

Use permitted Android APIs and declared services, including AccessibilityService where appropriate. Never assume privileged access.

7. Safety and Authorization

Permission checks, confirmation gates, policy checks, data minimization and audit records for sensitive actions.

8. Verification

Action results, safe diagnostics and testing. Avoid recording secrets or unnecessary personal data.

Task Execution Lifecycle

Request → Clarify → Plan → Authorize → Execute → Verify → Report → Learn from correction.

Capability Contract

Each capability must document:

- Identifier and purpose
- Inputs and outputs
- Required permissions
- Risk level
- Confirmation requirements
- Failure modes
- Verification strategy
- Tests

Sensitive Actions

Sending communications, purchases, destructive operations, account/security changes and other consequential actions require appropriate explicit user authorization.

Android Constraints

Background execution, overlays, accessibility, microphone and system interactions are subject to Android version, manufacturer and permission restrictions.

Root or Shizuku must never be silently assumed.

Architecture Evolution

Do not merge repositories or rewrite a foundation before a baseline build, dependency review, license review and architecture assessment.

All changes must remain isolated and reversible.
