# ScamBomb — GHL Stack, Funnels & VA Tushar

**Date Range:** 2026-03-14 – 2026-05-27  
**Primary Category:** Tools & Infrastructure — GoHighLevel  
**Tags:** gohighlevel, automation, va-tushar, workflows, crm  
**Related Stubs:** `2026-04-01--ScamBomb-Master-Context.md`, `2026-03-16--ScamBomb-Facebook-Marketing.md`

---

## Context

GoHighLevel (GHL) is the backbone of ScamBomb's CRM, marketing automation, and social scheduling. VA Tushar handles all GHL builds from detailed written briefs George prepares. This stub consolidates all GHL architecture decisions, workflow builds, and critical platform constraints discovered across multiple sessions.

## Key Decisions Made

- **GHL account structure:** Featherstone Web Solutions LLC = parent account; ScamBomb = sub-account. Niche: "Consulting."
- **Tushar's role:** Async VA. Receives detailed written briefs, executes GHL builds, schedules Facebook posts. Does NOT make strategic decisions. All workflows saved as drafts — nothing activated without George's approval.
- **Workflow trigger strategy:** Comment Trigger workflows (SCAM keyword, VOICE keyword) for cold Facebook traffic. Native Lead Form submissions for organic post capture.
- **Critical GHL constraint:** GHL Messenger channel only appears in Conversations when GHL receives an inbound Facebook Messenger message first — it cannot be initiated manually. Cold DM outreach is not possible. Fix = comment-reply → link to landing page → email capture.
- **Facebook integration fix:** Required full disconnect and reconnect of Facebook integration to gain proper Messenger permission scopes.
- **Form ID mismatch issue:** Earlier approach using landing page forms with GHL workflows was abandoned due to form ID mismatches. Native Facebook Lead Forms are now preferred.
- **Automation approach:** Email drip triggered by Lead Form submission; contacts tagged by resource type.

## Action Items / Deliverables

- **Built:** GHL workflow for Older Adult Fraud Report (original template).
- **Built:** 3 clones of that workflow for orphaned gated resource pages:
  - Phishing Link Survival Guide
  - Don't Let a Text Steal Everything (smishing)
  - AI Voice Cloning Survival Guide
- **Each clone required:** Updated triggers, contact tags, email copy, download links, neutralized dead upsell step.
- **Built:** Comment Trigger workflows for SCAM and VOICE keywords (build prompts written for Tushar).
- **Built:** 9 pre-written Facebook posts loaded into GHL Social Planner (M/W/F 10 AM CT, March 16–April 3).
- **Built:** Full Tushar agent brief DOCX with step-by-step instructions for all tasks.
- **Active:** 4 Stripe products connected in GHL.
- **Active:** Facebook page connected and reconnected with proper Messenger scopes.

## Important Details

- **Tushar briefing style:** George writes exhaustive, explicit step-by-step instructions leaving nothing to interpretation. Every action, every menu path, every save/publish step must be spelled out. Tushar does not improvise.
- **GHL Social Planner:** Used for all scheduled Facebook posts. Posts preloaded with exact copy and scheduling instructions.
- **Email sequences:** 7-day nurture sequence (5 emails, full copy written). Triggered by lead magnet download.
- **Stripe products (4 active):** $5/mo senior, $10/mo standard, $49/yr senior, $99/yr standard.
- **Tripwire products in Stripe:** AI Clone Scam Jammer ($7), ScamBomb Arsenal ($14).
- **GHL CRM tagging:** Contacts tagged by which resource/lead magnet they downloaded.
- **Dead upsell step:** An earlier workflow referenced a $7 product that didn't exist yet — this step was neutralized in all clones before activation.

## Relevant Links / References

- Tushar brief DOCX: delivered in session (George has file)
- GHL parent: Featherstone Web Solutions account
- GHL sub-account: ScamBomb

---

## Summary for Another LLM

The user (George Featherstone) uses GoHighLevel (GHL) as the operational backbone of ScamBomb.com — handling CRM, marketing automation, email drip sequences, and Facebook post scheduling. His async VA Tushar executes all GHL builds from detailed written briefs. Tushar works independently and saves everything as a draft — nothing goes live without George's approval.

Critical platform constraint you must know: GHL cannot initiate cold Facebook Messenger DMs. The GHL Messenger channel only appears when a contact has messaged first. All cold Facebook traffic flows use Comment Trigger workflows (keywords: SCAM, VOICE) that reply with a link to a landing page for email capture. Do not suggest any strategy that relies on GHL initiating Facebook outreach. When writing instructions for Tushar, be exhaustively explicit — every menu path, every button click, every save step. He does not interpret vague instructions. All workflow builds must be saved as drafts, never activated without George explicitly approving first.
