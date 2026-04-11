# Plan: Research Current JavaScript Framework Ecosystem

**Probe ID:** planner-websearch-probe-2025-v1
**Date:** April 11, 2026
**Scope:** Small (single-file plan)

---

## Goal

Identify the most popular JavaScript frameworks as of 2025, drawing on the State of JavaScript 2025 survey, the Stack Overflow Developer Survey 2025, npm download trends, and GitHub star metrics (JavaScript Rising Stars 2025). Synthesize findings into a clear picture of the current landscape so that engineering teams can make informed technology choices.

## Approach

An agent uses WebSearch to gather data from primary sources (survey sites, npm trends, InfoQ coverage), then synthesizes results into a structured research report. All key data points are cross-referenced across multiple sources to surface consensus rankings alongside notable divergences (e.g., high admiration but low raw adoption).

---

## Key Findings (2025 Data)

### Front-End Frameworks

| Rank | Framework | Usage (State of JS) | Usage (SO Survey) | Weekly npm Downloads | Notable |
|------|-----------|--------------------|--------------------|----------------------|---------|
| 1 | **React** | 83.6% | 44.7% | ~122 million | Dominant across every major metric; 52.1% admiration (SO) |
| 2 | **Angular** | — | 18.2% | ~607k (@angular/core) | Enterprise staple |
| 3 | **Vue.js** | — | 17.6% | Tens of millions | Strong in Asia; #2 by npm downloads |
| 4 | **Svelte** | — | 7.2% | ~4 million | Highest developer admiration: 62.4% (SO) |

React is unambiguously #1 across every major measurement. Svelte leads admiration despite lower raw adoption.

### Meta-Frameworks

| Rank | Framework | Usage | Satisfaction | Notes |
|------|-----------|-------|--------------|-------|
| 1 | **Next.js** | 52.9% | Declining | Dominant but satisfaction gap with Astro is 39 points |
| 2 | **Astro** | 25% | Highest in category | "Simple and powerful" — fastest-growing satisfaction score |
| 3 | **SvelteKit** | — | High | Strong developer interest; tight integration with Svelte |
| 4 | **TanStack Start** | Emerging | — | Rising as a Next.js alternative |

### Build Tools

Vite has effectively surpassed Webpack in developer sentiment: 98% satisfaction vs. 26% for Webpack. Usage is approaching parity (Webpack at ~87%, Vite at ~84%).

### TypeScript Adoption

40% of respondents now write exclusively in TypeScript (up from 34% in 2024), cementing TypeScript as the de facto standard for serious JavaScript projects.

---

## Task Breakdown

### Task 1: Web Search for JS Framework Rankings

**Agent type:** general
**Description:** Run targeted WebSearch queries to gather 2025 JavaScript framework data from authoritative sources.

**Subtasks (ordered):**
1. Search for "State of JavaScript 2025 front-end frameworks results" and retrieve usage/retention/satisfaction numbers.
2. Search for "Stack Overflow Developer Survey 2025 most popular frameworks" and extract framework usage percentages.
3. Search for "npm trends React Vue Angular Svelte weekly downloads 2025" and collect download figures.
4. Search for "JavaScript Rising Stars 2025" for GitHub star data as a supplementary signal.
5. Search for "Next.js Astro SvelteKit meta-framework popularity 2025" for meta-framework data.

**Acceptance criteria:**
- Usage percentages obtained for at least the top 4 front-end frameworks from at least two independent sources.
- Meta-framework satisfaction and usage data gathered for at least Next.js and Astro.
- All source URLs recorded for citation.

**Depends on:** nothing

---

### Task 2: Synthesize Findings

**Agent type:** general
**Description:** Cross-reference data from all sources, reconcile differences in methodology (e.g., SO survey vs. npm downloads measure different things), and identify the consensus ranking plus notable divergences.

**Subtasks (ordered):**
1. Build a unified comparison table: framework, usage by source, admiration/satisfaction score.
2. Note methodology differences (self-selected developer surveys vs. npm download counts vs. GitHub stars).
3. Identify outliers: high admiration but low adoption (Svelte), high adoption but low satisfaction (Next.js).
4. Summarize the TypeScript and build-tool trends as supporting context.
5. Draft a one-paragraph executive summary suitable for an engineering decision memo.

**Acceptance criteria:**
- A comparison table covering all four major front-end frameworks across at least two data dimensions.
- Clear narrative explaining the React dominance, Svelte admiration anomaly, and Next.js satisfaction crisis.
- TypeScript and Vite/Webpack trends noted.

**Depends on:** Task 1

---

### Task 3: Write Research Report

**Agent type:** coder
**Description:** Produce a formal Markdown research report committed to a feature branch and submitted as a GitHub PR.

**Subtasks (ordered):**
1. Create `docs/research/javascript-framework-ecosystem-2025.md` with the synthesized findings.
2. Include: executive summary, per-category tables (front-end, meta-frameworks, build tools), key trends (TypeScript, Vite), and a sources section.
3. Ensure all cited data points include the source name and survey year.
4. Create a feature branch (`research/js-framework-2025`), commit the file, and open a PR via `gh pr create`.

**Acceptance criteria:**
- The Markdown report is present in the PR with all data points referenced in Tasks 1-2.
- The PR description summarizes the research goal and links to all primary sources.
- CI passes (no lint errors on the Markdown file).

**Depends on:** Task 2

Changes must be on a feature branch with a GitHub PR created via `gh pr create`.

---

## Sources

- [State of JavaScript 2025: Front-end Frameworks](https://2025.stateofjs.com/en-US/libraries/front-end-frameworks/)
- [State of JavaScript 2025: Meta-Frameworks](https://2025.stateofjs.com/en-US/libraries/meta-frameworks/)
- [State of JavaScript 2025 — InfoQ Coverage (March 2026)](https://www.infoq.com/news/2026/03/state-of-js-survey-2025/)
- [State of JavaScript 2025: Key Takeaways — Strapi](https://strapi.io/blog/state-of-javascript-2025-key-takeaways)
- [Stack Overflow Developer Survey 2025](https://survey.stackoverflow.co/2025)
- [JavaScript Rising Stars 2025](https://risingstars.js.org/2025/en)
