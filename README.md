# claude-chrome-extension-developer-skill

A Claude Code skill for building, modernizing, securing, and debugging Chrome extensions with Manifest V3.

## Overview

This skill focuses on the Manifest V3 extension architecture, including service workers, content scripts, popup and options pages, storage, permissions, and cross-context messaging.

It helps developers structure extensions that are maintainable and respect browser security boundaries.

## Main Capabilities

- Create and configure Manifest V3 manifests.
- Implement background service workers.
- Build content scripts and page integrations.
- Develop popup and options interfaces.
- Communicate between extension contexts.
- Use storage and browser extension APIs.
- Configure permissions and host access.
- Handle alarms and lifecycle events.
- Debug service worker and messaging behavior.
- Review extension security.

## Manifest V3 Architecture

| Component | Responsibility |
|---|---|
| Service worker | Background event handling |
| Content script | Interaction with permitted web pages |
| Popup | Short-lived user interface |
| Options page | Persistent user configuration |
| Extension pages | Privileged extension UI |
| Storage | Settings and extension state |

## Installation

```bash
git clone https://github.com/Brajesh31/claude-chrome-extension-developer-skill.git ~/.claude/skills/chrome-extension-developer
```

## Usage

Invoke the skill for Chrome extension development:

```text
/chrome-extension-developer
```

Provide the extension's purpose, target websites, required permissions, user interface, and current manifest or source files.

## Recommended Development Workflow

1. Define the extension's user-facing behavior.
2. Identify the minimum required permissions.
3. Create the Manifest V3 configuration.
4. Separate service worker, content script, and UI responsibilities.
5. Define message contracts between contexts.
6. Store settings and state appropriately.
7. Handle service worker suspension and restart behavior.
8. Test on target pages and browser versions.
9. Review security and privacy behavior.
10. Package and validate the extension.

## Security Checklist

- Request only necessary permissions.
- Restrict host access where possible.
- Validate messages between extension contexts.
- Treat page content as untrusted input.
- Avoid unsafe script injection.
- Protect extension secrets and user data.
- Use secure communication and storage patterns.
- Explain data collection and processing clearly.

## Repository Contents

- `SKILL.md`: Main Manifest V3 development instructions.
- `README.md`: Architecture, workflow, and security guidance.

## Troubleshooting

If an extension fails, inspect the service worker console, extension errors page, manifest validity, permission grants, and message-passing paths. Reproduce the issue with the smallest affected extension component.

## Practical Principle

Permissions are part of the product's trust model. Do not request broad host access or powerful APIs simply to make implementation easier.
