# NerdyMugs / Automated Content Engine (Dr. Featherstone Template)

**Date Range:** 2026-04-09  
**Primary Category:** Growing Side Hustles — Affiliate & Automated Content Projects  
**Tags:** nerdymugs, affiliate, automation, nextjs, content-engine  
**Related Stubs:** `2026-04-01--ScamBomb-Master-Context.md`

---

## Context

George ("Dr. Featherstone" creative persona) ideated a fully automated affiliate content publishing engine, starting with NerdyMugs.com. The project is explicitly designed to run in the background while ScamBomb takes priority — passive affiliate revenue with zero maintenance overhead. Critically, this is a re-skinnable template, not a one-off site.

## Key Decisions Made

- **Primary constraint:** Legal caution around IP. Will not produce content that risks copyright infringement. Works only with designs in the public creative space.
- **Monetization:** Amazon Associates affiliate links only (at this stage).
- **Template philosophy:** NerdyMugs is the proof-of-concept. The same codebase re-skins for any niche.
- **Scope ruthlessly reduced** by George during session (unprompted):
  - ❌ Removed: Multi-tenant "tool for everyone" ambitions
  - ❌ Removed: AI image generation
  - ❌ Removed: FastAPI
  - ❌ Removed: Scheduling rule complexity
  - ❌ Removed: Community Engagement Agent (no usable API, ban risk)
  - ❌ Removed: Review Aggregator (premature)
- **Stack locked:** Next.js (Vercel), Supabase, Amazon PA-API, Claude API, Vercel Cron.
- **Config-driven:** Single JSON file in repo controls categories, tags, voice rules, rotation weighting. No UI needed for config.
- **Social automation:** Buffer free plan for RSS → X and Facebook auto-post (Zapier free tier as alternative). Setup time ~20 min once RSS feed URL confirmed.
- **RSS feed URL pattern:** `nerdymugs.com/feed.xml` or `/rss.xml`.

## Action Items / Deliverables

- **Built:** Config schema (JSON) — controls categories, tags, voice rules, rotation weighting.
- **Built:** Content agent system prompt (Claude API) — handles all content generation from config.
- **Outstanding (not yet built):**
  - Next.js scaffold on Vercel
  - Supabase schema
  - Amazon PA-API integration
  - Vercel Cron jobs
  - Buffer/RSS auto-post setup
  - First niche content batch

## Important Details

- **Dr. Featherstone persona:** George's creative ideation voice. When he shifts into this mode, expect big swings followed by sharp editorial cuts. Respond with real-talk, not hedged advice.
- **NerdyMugs domain:** NerdyMugs.com
- **Priority:** ScamBomb is primary through June 30 deadline. NerdyMugs runs in background only — do not suggest prioritizing it over ScamBomb.
- **Architecture:** Next.js on Vercel generates product-focused affiliate content. Supabase stores content and tracks what's been published. Amazon PA-API pulls live product data. Claude API writes the posts. Vercel Cron schedules publication.
- **Config JSON location:** In the repo root. Changing the niche = changing the config + a new domain. Same code runs for any niche.
- **Buffer free plan:** 3 channels, RSS auto-post built in. Set and forget. No Zapier workflow needed.
- **"Pure intent" distillation (George's framing):** "A machine that reads a product category, writes useful things about it, posts them automatically, and earns commissions while I sleep."

## Relevant Links / References

- NerdyMugs: https://nerdymugs.com
- Buffer: https://buffer.com
- Amazon Associates: https://affiliate-program.amazon.com
- Vercel: https://vercel.com
- Supabase: https://supabase.com

---

## Summary for Another LLM

The user (George Featherstone, "Dr. Featherstone" creative persona) is building an automated affiliate content engine starting with NerdyMugs.com. This is a re-skinnable template — the same Next.js/Supabase/Claude API/Vercel Cron stack can be re-deployed for any niche by changing a single config JSON file. The monetization model is Amazon Associates.

This project is explicitly a background runner — ScamBomb is George's primary focus through June 30, 2026. Do not suggest deprioritizing ScamBomb for NerdyMugs. The scope has been aggressively trimmed: no FastAPI, no multi-tenant features, no AI image generation, no complex scheduling rules. The stack is Next.js + Vercel + Supabase + Amazon PA-API + Claude API + Vercel Cron. Social distribution uses Buffer free plan (RSS → X and Facebook auto-post). IP caution is strict — content must stay in the public creative space, no infringement risks. When helping with this project, assume the stack and scope are locked. Outstanding work is the actual code scaffold and first content batch.
