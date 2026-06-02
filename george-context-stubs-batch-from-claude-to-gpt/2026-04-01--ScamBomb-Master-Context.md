# ScamBomb — Master Context & Architecture

**Date Range:** 2026-02-25 – 2026-06-01  
**Primary Category:** Growing Side Hustles — ScamBomb (primary)  
**Tags:** scambomb, saas, fraud-prevention, seniors, bootstrap  
**Related Stubs:** `2026-04-01--ScamBomb-90Day-Revenue-Sprint.md`, `2026-03-16--ScamBomb-Facebook-Marketing.md`, `2026-03-14--ScamBomb-GHL-Stack-Tushar.md`, `2026-04-08--ScamBomb-Public-Speaking-Lane.md`

---

## Context

George Featherstone is the solo founder of ScamBomb.com, a bootstrapped SaaS scam detection platform targeting seniors and their adult children. The product allows users to paste suspicious text or upload photos and receive a plain-English danger score. ScamBomb operates as a brand under Featherstone Web Solutions LLC (formed ~March 2026 via Northwest Registered Agent, Texas).

## Key Decisions Made

- **Legal structure:** Featherstone Web Solutions LLC is the parent entity; ScamBomb is a brand under it (no separate LLC needed). PO Box obtained for ScamBomb to separate it from home address.
- **Pricing locked:** $5/mo senior (age 60+), $10/mo standard, $49/yr senior annual, $99/yr standard annual. Age-based tier routing via required age dropdown at signup.
- **Primary target demographic:** Adults 55–65+ (seniors first, then caregivers 30–45 in later phase).
- **Brand voice:** Calm. Clear. Protected. Non-judgmental, shame-free, practical.
- **Tagline:** "Knowledge Over Fear."
- **Tech stack:** Bolt.new (app build), Stripe (payments), GoHighLevel/GHL (CRM + automation), Beehiiv (newsletter), Canva + CapCut (content), Vercel/Next.js (newer builds), Google Stitch (ad creative generation).
- **Chrome extension:** Exists as part of the ScamBomb ecosystem.
- **Free scan limit:** Changed from 3/day to 5/month (implemented via Cline).
- **Tripwire products:** AI Clone Scam Jammer ($7 PDF), ScamBomb Arsenal ($14 PDF).
- **Lead magnets (3):** Phishing Link Survival Guide, AI Voice Cloning Defense Guide, Don't Let a Text Steal Everything (smishing guide).
- **Landing pages:** `/protect-parents` (primary acquisition), `/ai-clone-scam-jammer` (tripwire sales page).
- **GHL critical discovery:** GHL cannot initiate Facebook cold DMs. Workaround = comment-reply flows directing users to landing pages.
- **Facebook objective:** Leads campaign (not boost), targeting adults 45–65, US, with AARP Medicare interest layering.

## Action Items / Deliverables

- **Built and live:** ScamBomb.com app, Stripe products (4 active), all 4 resource landing pages, 3 lead magnets, 2 tripwire PDFs, GHL workflows (in draft/live), Beehiiv newsletter, Facebook ads campaign.
- **Built:** 9-tab Google Sheets sprint tracker (Mission Control KPIs, 90-Day Sprint, Content Calendar, FB Ad Tracker, Email List Growth, Tripwire Sales, Subscriber MRR, Brand Voice Lab, GHL Automations Checklist).
- **Built:** 7-day email nurture sequence (5 emails written in full).
- **Outstanding:** Chrome extension roadmap, mobile app (future), YouTube channel, paid speaking pipeline.

## Important Details

- **Company:** Featherstone Web Solutions LLC, Gilmer TX
- **GHL account structure:** Featherstone Web Solutions = parent; ScamBomb = sub-account. Niche: "Consulting."
- **Facebook Page:** Connected to GHL. Required full disconnect + reconnect to gain proper Messenger permission scopes.
- **Sharon Brightwell (Dover FL) case:** Real, sourced scam victim story used in sales copy — FOX 13 Tampa Bay, July 2025. Used as substitute for fabricated testimonials (FTC compliance).
- **Key stat used in ads:** Seniors lost $4.8 billion to fraud in 2024 (FBI IC3); average loss for 60+: $83,000.
- **Brand colors:** Dark navy #0B1324, yellow #F5C84C, Montserrat font, rounded cards.
- **VA Tushar:** Async. Works from detailed written briefs George prepares. Handles GHL builds and Facebook scheduling. Based remotely (not Philippines).
- **VA Brooke:** Philippines-based (Gene's Apparell on PayPal), handles ShirtNerdXL operations — separate from ScamBomb.

## Relevant Links / References

- Live app: https://scambomb.com
- Primary landing page: https://scambomb.com/protect-parents
- Tripwire page: https://scambomb.com/ai-clone-scam-jammer
- Beehiiv newsletter: (ScamBomb brand)
- Sharon Brightwell source: https://www.fox13news.com (FOX 13 Tampa Bay, July 2025)

---

## Summary for Another LLM

The user is George Featherstone, solo founder of ScamBomb.com — a bootstrapped SaaS scam detection platform targeting adults 55+ (primarily seniors) and their adult children. ScamBomb lets users paste suspicious messages or upload images to get a plain-English danger score. It operates under Featherstone Web Solutions LLC (Gilmer, TX). The brand voice is calm, protective, and non-judgmental ("Calm. Clear. Protected.").

The tech stack is Bolt.new (app), Stripe (4 products active), GoHighLevel/GHL (CRM, automation, social scheduling), Beehiiv (newsletter), Canva/CapCut (content), and Vercel/Next.js for newer builds. Pricing is locked: $5/mo senior, $10/mo standard, $49/yr senior, $99/yr standard. There are two tripwire PDFs ($7 and $14) and three free lead magnets. The async VA named Tushar handles GHL builds from detailed written briefs — do not suggest he can be reached in real time. A critical infrastructure constraint: GHL cannot initiate Facebook cold DMs; all cold-traffic flows must use comment-reply → landing page → email capture. Do not suggest Facebook DM outreach as a strategy. George's development tool is Cline (VS Code extension) with the OpenClaw/VIKTA agentic setup for local AI workflows.
