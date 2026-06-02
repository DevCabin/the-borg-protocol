# OpenClaw / VIKTA / Hermes Agent — Local AI Ecosystem

**Date Range:** 2026-02-23 – 2026-06-01  
**Primary Category:** AI Research & Experiments — Local AI Infrastructure & Tooling  
**Tags:** openclaw, vikta, hermes, ollama, local-llm, agentic  
**Related Stubs:** `2026-04-01--ScamBomb-Master-Context.md`

---

## Context

George runs a local AI infrastructure centered on OpenClaw with a custom configuration called VIKTA. Multiple sessions covered initial Claude Pro OAuth integration, SSH tunnel troubleshooting, the Hermes Agent comparison, and the `ollama launch` command semantics. A formal VIKTA handoff document was also built for cross-session context continuity.

## Key Decisions Made

- **OpenClaw + VIKTA:** George's primary local AI assistant setup. VIKTA is a context configuration (persona + ScamBomb context + working preferences) loaded into OpenClaw. This is his most-used agentic tool.
- **Claude Pro OAuth integration:** Claude Pro integrated with OpenClaw via `setup-token` auth method using Claude Code CLI-generated OAuth token. API costs bundled into Pro subscription (not per-token billing). Anthropic confirmed personal use of OpenClaw with own subscription is acceptable.
- **SSH tunnel:** George's setup at `192.168.1.97` (user: george). Tunnel command: `ssh -N -L 18789:127.0.0.1:18789 george@192.168.1.97`. Local port 18789. If tunnel fails with "Address already in use" → OpenClaw is already running locally; no tunnel needed. Fix expired tokens via Settings at `http://localhost:18789`.
- **`ollama launch` semantics:** Session-scoped model router — calls an already-installed application and specifies which model to use for that session. Does NOT reinstall or create a new permanent installation.
- **`:cloud` suffix** on model names (e.g., `minimax-m3:cloud`) = cloud-backed model, not local. Local setup remains untouched.
- **Hermes Agent decision:** Not a replacement for OpenClaw/VIKTA (too much existing investment). Evaluated as a complementary second agent for mobile/async task delegation via platforms like Telegram.
- **Hermes 3 (model) vs. Hermes Agent (framework):** Two distinct things from Nous Research. Hermes 3 = fine-tuned Llama 3.1 405B with agentic capabilities (XML structured output, scratchpads, reasoning tokens). Hermes Agent = open-source framework with 15+ platform messaging support, FTS5 persistent memory, self-improving skill libraries, Honcho user modeling.
- **VS Code OOM fix:** Extension Host JavaScript heap OOM crash caused by Cline accumulating conversation context. Fixed by editing `argv.json` via Command Palette ("Configure Runtime Arguments") and adding `"js-flags": "--max-old-space-size=8192"`. Requires full VS Code restart (not window reload).

## Action Items / Deliverables

- **Built:** VIKTA handoff document (`VIKTA_context_handoff.md`) — full ScamBomb context, 90-day sprint, GHL architecture, people roster, tech stack, 9-tab tracker, working preferences, session history. Delivered to `/mnt/user-data/outputs/`.
- **Resolved:** Claude Pro OAuth token setup in OpenClaw — working.
- **Resolved:** SSH tunnel "Address already in use" — OpenClaw already running locally, no tunnel needed.
- **Resolved:** VS Code Extension Host OOM crash — `argv.json` heap increase applied.
- **Outstanding:** Hermes Agent evaluation as async/mobile companion; Ollama application ecosystem exploration.

## Important Details

- **VIKTA handoff document covers:** George's full business context, ScamBomb architecture, 90-day sprint, pricing, funnel, GHL workflows, VA Tushar, Facebook constraints, key people (Cody = iClassPro supervisor, Tushar = async VA, Rianna = wife), working preferences, tech stack, 9-tab tracker, recent session history (March–early April 2026).
- **argv.json location:** Accessed via VS Code Command Palette → "Configure Runtime Arguments." Key added: `"js-flags": "--max-old-space-size=8192"`. Common error: duplicate keys or missing commas after existing entries — validate JSON before saving.
- **OpenClaw local address:** `http://localhost:18789`
- **Remote machine:** `192.168.1.97`, user: george (gaming rig running Ollama).
- **Authentication error 401:** Usually caused by cached/expired token, whitespace in pasted token, or plan/model access mismatch. Re-login at `http://localhost:18789` Settings.
- **Hermes Agent differentiators:** Cross-platform messaging (15+ platforms), FTS5-based persistent memory with LLM summarization, self-improving skill libraries, Honcho user modeling layer, serverless terminal backend (Modal).

## Relevant Links / References

- OpenClaw: http://localhost:18789 (local)
- VIKTA handoff doc: `VIKTA_context_handoff.md` (outputs folder)
- Hermes Agent: Nous Research (open source)
- Ollama: https://ollama.com
- Claude Code CLI: for OAuth token generation

---

## Summary for Another LLM

The user (George Featherstone) runs a local AI infrastructure built around OpenClaw with a custom configuration called VIKTA. OpenClaw is his primary agentic tool, running locally at `http://localhost:18789` on a machine at `192.168.1.97`. VIKTA is a context config that loads his full ScamBomb business context, working preferences, and project state into every OpenClaw session.

His development environment is VS Code with the Cline extension for agentic coding. The VS Code Extension Host OOM issue has been resolved via `argv.json` heap size increase (`--max-old-space-size=8192`). He evaluated Hermes Agent (Nous Research) as a potential second agent for async/mobile task delegation via Telegram — it was not selected as an OpenClaw replacement. The `ollama launch` command is session-scoped only; it does not reinstall applications. When helping with local AI tooling, assume OpenClaw/VIKTA is the established primary stack. Do not suggest replacing it. Hermes Agent remains a "maybe later" evaluation, not an active project.
