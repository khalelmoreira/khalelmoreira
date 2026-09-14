### Hi, I'm Khalel 👋

Junior Backend Developer, studying Computer Science, based in Brazil.

I build and maintain, on my own, a production system for **NFS-e automation** — Brazilian electronic service invoices issued through WhatsApp, with a Python/Flask backend and an AI-assisted conversation layer. The repository for that project is private (it belongs to the company I work with), so here's a rundown of what it's about.

#### What I built

- **Layered architecture with a deterministic boundary**: `routes → handlers → services → managers → database`. AI is only used for extraction/classification of what the user says — every business decision and side effect (like issuing an invoice) is handled by deterministic code. That separation matters in a system that emits fiscally and legally binding documents.
- **Independent state machines** for onboarding, in-progress invoice drafts, and invoice lifecycle, so a change in one flow doesn't ripple into the others.
- **Race-condition-safe status transitions**, using conditional database updates instead of optimistic state changes.
- **Multi-provider AI layer** (Anthropic, OpenAI) with automatic fallback.
- **Production hardening on a Linux VPS**: OS-level privilege isolation between the app and the AI coding agent I use, SSH/firewall hardening, HTTPS, automated encrypted backups, and structured logging with PII redaction.
- **46 test files** covering real edge cases — duplicate messages, repeated webhooks, server restarts mid-job — not just the happy path.

#### How I got here

Between March and September 2026, I wrote the entire foundation of this system by myself, using Claude's free plan. That meant I couldn't paste large chunks of code into a chat without burning my token budget — so I had to break every problem down to its smallest piece before asking for help. It slowed me down at first, but it's the reason I actually understand the code I write.

#### Currently

Looking for a remote **Junior Backend Developer** role where I can keep growing alongside a team.

- 🔧 Python, Flask, SQLite, Docker, Linux (Fedora/Debian/Ubuntu), Git
- 📫 Reach me through [LinkedIn](https://www.linkedin.com/in/khalel-moraes/)
