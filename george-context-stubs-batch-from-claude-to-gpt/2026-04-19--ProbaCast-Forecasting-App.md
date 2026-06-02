# ProbaCast — Probabilistic Forecasting App Build

**Date Range:** 2026-04-19  
**Primary Category:** AI Research & Experiments — Prompt Engineering & Workflow Design  
**Tags:** probacast, react, forecasting, two-pass-ai, vercel  
**Related Stubs:** `2026-04-09--NerdyMugs-Automated-Content-Engine.md`, `2026-04-18--OpenClaw-VIKTA-Hermes-Ecosystem.md`

---

## Context

George wanted to build a tool that automates the probabilistic forecasting workflow he uses manually — compiling data, running scenario analysis, and producing probability estimates. The session began with a real tornado forecasting exercise, evolved into defining the methodology, and ended with a React app (ProbaCast v0.2) with a two-pass AI architecture.

## Key Decisions Made

- **Core insight:** The app must do the reasoning on intake — not a manual form wizard. George uses other LLMs to compile data blobs and needs ProbaCast to parse and reason, not prompt him for structured inputs.
- **Two-pass AI architecture:**
  - Pass 1 (Extraction): Claude parses raw pasted data blob into structured forecast inputs.
  - Pass 2 (Forecast): Claude reasons over that structure to produce scenarios, probability estimates, and written analysis.
- **Framework:** React (built as Claude artifact, deployable to Vercel).
- **Methodology defined:** Scenario analysis + analog comparison + trend extrapolation + Bayesian reasoning = subseasonal-to-seasonal (S2S) forecasting.
- **UI approach:** Transparent background, dark mode. All text elements need explicit `color: "var(--color-text-primary)"` to prevent dark-on-dark issues.

## Action Items / Deliverables

- **Built:** ProbaCast v0.2 (React app, two-pass AI architecture, scenario output, probability estimates, written analysis).
- **Built:** Full session transcript as structured markdown export.
- **Roadmap items (not yet built):**
  - Vercel deployment
  - Persistent prediction tracking (history of past forecasts)
  - Web search integration for live data pull
  - Behavior pattern mode (predicting individual performance trajectories, not just events)

## Important Details

- **Real forecasting session completed:** US tornado count by end of April 2026.
  - Initial target: 200 tornadoes — ~40% probability (below George's 65% threshold).
  - Revised target: 175 tornadoes — ~55–60% probability (accepted).
  - Method: ~80 confirmed as of April 17, 13 days remaining, required ~5.5–6.2/day vs. long-term April average of 6.1/day.
- **v0.1 failure mode:** Too manual — required user to enter structured inputs field by field. George rejected this.
- **v0.2 fix:** Single large textarea for pasting raw data blob; AI does the parsing and structuring before forecasting.
- **CSS fix critical:** `color: "var(--color-text-primary)"` must be applied explicitly on every text element throughout the component tree. Flex gap behaves differently from margin in some rendering contexts — use margin for reliability.
- **UI iteration history:** 3 rounds — padding, transparent background fix, dark mode text contrast fix.

## Relevant Links / References

- Session transcript: delivered as markdown export
- ProbaCast v0.2: Claude artifact (session)
- SPC outlooks: https://www.spc.noaa.gov

---

## Summary for Another LLM

The user (George Featherstone) built ProbaCast — a React forecasting app powered by a two-pass Claude AI architecture. Pass 1 extracts structured forecast parameters from a raw pasted data blob. Pass 2 reasons over that structure to produce scenario analysis, probability estimates, and written narrative. The critical design constraint is that the app must do the reasoning on intake — do not rebuild it as a form wizard that asks the user to enter structured data manually.

The methodology is subseasonal-to-seasonal (S2S) forecasting: scenario analysis + analog comparison + trend extrapolation + Bayesian reasoning. The app is built in React and is intended for Vercel deployment. The roadmap includes persistent prediction tracking, web search integration for live data, and a behavior pattern mode. When helping with ProbaCast, assume the two-pass architecture is locked. The main outstanding items are deployment, persistence layer, and web search integration. Known CSS gotcha: all text elements need explicit `color: "var(--color-text-primary)"` in dark mode components to prevent invisible text.
