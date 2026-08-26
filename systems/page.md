# Systems

PamAI’s systems estate covers persistent work context, AI request routing, user-selected integrations, and operational support services.^\[1\]^ (`data:9`)

## Core work context
The product stores and retrieves workspaces, projects, messages, files, and memory, runs user-requested integrations and imports, and uses operational logs and error reports to secure and debug the service.^\[2\]^ (`data:9`)

## AI request path
User content is sent to AI models through the Vercel AI Gateway. Requests use Zero Data Retention by default: providers do not retain prompts or outputs after the request is served or use them to train their models. Provider pinning restricts inference to a vetted allowlist of US/EU or Western/GDPR-aligned hosts, and requests fail rather than routing outside that allowlist; PamAI does not route user data to first-party China AI endpoints.^\[3\]^ (`data:9`)

Interactive conversation training requires an explicit profile opt-in and is off by default. Background and system jobs remain Zero Data Retention even when a user opts in for their own interactive conversations.^\[4\]^ (`data:9`)

## Integrations and service dependencies
The documented integration surface includes Telegram, WhatsApp, Google Calendar, Notion, ClickUp, and coding-agent client data. Supporting subprocessors span hosting, storage, authentication, AI inference, messaging, email, sandbox compute, error monitoring, and payment providers.^\[5\]^ (`data:9`)

Google Calendar is a concrete external dependency: when connected, PamAI accesses only the Google data needed for requested features, including basic profile and email for authentication and calendar events for scheduling. Google OAuth access and refresh tokens are encrypted at rest, Google data is transmitted over HTTPS/TLS, and access is limited to authorized systems and personnel. Disconnecting the account stops new Google Calendar sync and deletes or deactivates stored OAuth tokens.^\[6\]^ (`data:9`)

## Sources
- [https://pamai.pm/privacy](https://pamai.pm/privacy) (`data:9`)
