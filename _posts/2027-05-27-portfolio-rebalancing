---
title: "Wealth Command Center: A Personal Finance Dashboard"
date: 2026-05-27 10:00:00 +1000
categories: [Projects, Full-Stack Development]
tags: [nextjs, react, supabase, postgresql, tailwindcss, recharts, vercel]
pin: true
---
 
**Role:** Full-Stack Developer (Personal Project)  
**Location:** Melbourne, Australia  
**Timeline:** May 2026  
 
Most finance apps are built for everyone, which means they are optimised for no one. Brokerage dashboards are data-dense and desktop-first. Stock tracking apps show prices but no context. I wanted a single daily-driver application that combined live market data, portfolio analytics, and rebalancing intelligence in a mobile-first interface I would actually open every morning. The result is Wealth Command Center: a personal finance PWA engineered for correctness, zero-maintenance, and genuine analytical value.
 
### The Architecture & Stack
 
The application is built on a modern serverless stack designed for robustness over scale — a deliberate constraint for a single-user personal tool.
 
* **Frontend Framework:** Next.js 15 App Router with TypeScript (server components, dynamic routes, API route handlers).
* **Styling & UI:** Tailwind CSS with shadcn/ui component library, dark theme only.
* **Database & Auth:** Supabase (PostgreSQL with Row Level Security, Sydney region).
* **Data Visualisation:** Recharts (responsive SVG charts for portfolio analytics).
* **Price Data:** yahoo-finance2 with Supabase-backed price cache for offline resilience.
* **Deployment:** Vercel with automatic CI/CD on push to main.

### Core Technical Achievements
 
**1. Pure Functional Financial Logic Layer**
 
All financial calculations — net worth, cost basis, allocation drift, rebalancer recommendations, HISA comparison — live in `src/lib/finance/` as pure TypeScript functions with no side effects. This made the logic fully unit-testable in isolation from the database and UI, resulting in a 76-test suite that validates every financial computation. The separation also means any component or API route can import and compose these functions without risk of data mutation.
 
**2. Drift-Minimisation Greedy Rebalancer**
 
The core rebalancing algorithm is not a simple "buy the most underweight ticker" approach. Each iteration selects the ticker whose purchase of exactly one unit produces the greatest reduction in total portfolio variance from target weights. The algorithm runs in whole units only — reflecting the reality of ETF investing — and excludes legacy holdings from the rebalancer universe automatically via a database flag. The result is mathematically optimal whole-unit allocation recommendations for any investment amount.
 
**3. Append-Only Ledger with Database-Level Integrity**
 
The transaction ledger is purely append-only — no row is ever mutated or deleted after insertion. Sell transactions are stored as negative units, enforced by a PostgreSQL CHECK constraint at the schema level, meaning no application code can ever bypass the convention. Corrections use reversal pairs (a compensating negative entry on the original date, a new entry on the corrected date), preserving a perfect mathematical audit trail. Holdings are always derived by summing the ledger — never stored directly.
 
**4. Heuristic Signal Engine**
 
Beyond raw prices, the application computes a heuristic classification for each holding daily: 30-day high, 30-day low, dip, or neutral. These signals are surfaced as visual badges on position cards and combined with real-time allocation drift to produce a composite buy signal — highlighting positions that are simultaneously underweight and at a recent price low. This transforms the dashboard from a passive tracker into an active decision-support tool.
 
**5. Data-Driven Portfolio Configuration**
 
The entire portfolio universe — tickers, target weights, legacy flags, display names — is driven from a single `holdings_config` database table. Adding a new ETF requires only a database insert: the price pipeline, rebalancer, dashboard cards, analytics pie chart, and settings UI all pick it up automatically. No code changes required. Display names are fetched from the price data source on first pull and persisted to the database, eliminating hardcoded lookup maps.
 
**6. Analytics Layer**
 
A dedicated analytics tab surfaces portfolio insights beyond simple tracking: a total wealth donut chart decomposing ETF positions and cash savings, cost basis efficiency showing average entry price versus current price per position, savings goal progress tracking, and a HISA comparison chart modelling portfolio growth against a high-interest savings account over the full investment history. A daily snapshot table accumulates net worth history passively on each app load, forming the foundation for future compounding visualisation.
 
### The Takeaway
 
Wealth Command Center demonstrates end-to-end ownership of a production financial application — from database schema design and constraint engineering to pure functional business logic, server-side data assembly, and a mobile-first UI built for daily use. The project required navigating real constraints: unofficial data sources, market hours logic, append-only data integrity, and the UX challenge of making complex financial information immediately readable on a 393px screen. It also served as an extended exercise in AI-assisted development, using LLMs as collaborative engineering partners across architecture decisions, code review, and iterative refinement throughout the full build lifecycle.