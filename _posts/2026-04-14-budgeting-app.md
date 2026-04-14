---
title: "Moneyball: Engineering a Mobile-First Fintech PWA"
date: 2026-04-14 10:00:00 +1000
categories: [Projects, Full-Stack Development]
tags: [nextjs, react, supabase, postgresql, tailwindcss, pwa]
pin: true
---

**Role:** Full-Stack Developer (Personal Project)  
**Location:** Melbourne, Australia  
**Timeline:** Apr 2026  

Traditional budgeting apps often suffer from cluttered interfaces and slow data entry, creating friction that prevents daily use. I wanted to build a personal finance application that bridged the gap between a lightning-fast expense tracker and a comprehensive wealth manager. The result is Moneyball: a Progressive Web App (PWA) engineered for speed, secure multi-tenant data architecture, and real-time financial visualization.

### The Architecture & Stack

To ensure a seamless, native-app experience on mobile devices while maintaining a robust and secure backend, I selected a modern serverless stack:

* **Frontend Framework:** Next.js and React (Managing complex client-side state, hooks, and component routing).
* **Styling & UI:** Tailwind CSS (Implementing a highly responsive, custom design system).
* **Database & Auth:** Supabase (PostgreSQL database with built-in Authentication).
* **Data Visualization:** Recharts (Rendering dynamic, interactive SVG charts).
* **Deployment:** Vercel (CI/CD and edge hosting).

### Core Technical Achievements

**1. Secure Multi-Tenant Backend Architecture**

Building a finance app requires strict data privacy. Instead of a basic CRUD setup, I implemented a robust PostgreSQL relational database managed via Supabase. Crucially, I engineered Row Level Security (RLS) policies at the database layer. This ensures that every database transaction (inserts, selects, updates, deletes) is cryptographically verified against the user's Auth ID, guaranteeing that users can only ever access or mutate their own financial data.

**2. Native iOS UX Optimization (PWA)**

A major focus was making the web application feel indistinguishable from a native iOS app. This required solving multiple mobile-web constraints:
* Engineered a custom, oversized numpad for 3-second frictionless data entry.
* Implemented `viewport-fit=cover` and dynamic CSS safe-area padding to seamlessly route the UI around the iPhone hardware notch/Dynamic Island.
* Integrated browser APIs for haptic feedback (`navigator.vibrate`) upon successful transactions.
* Locked the viewport scaling to suppress aggressive iOS auto-zooming on input fields, and hid default CSS scrollbars for fluid touch-swiping.

**3. Complex State Management & Dynamic Visualization**

The app features a "Time Machine" dashboard that required sophisticated React state management. Using optimized `useMemo` hooks, the application aggregates raw transaction and income data, dynamically calculating net savings and dynamically updating Recharts components (Donut charts and Historical Bar charts) without needing to re-ping the database. It also integrates proactive budgeting logic, rendering progress bars that visually warn users (via color-shifting logic) as they approach their custom monthly category caps.

### The Takeaway

This project demonstrates an end-to-end understanding of modern web application development. From designing a clean, user-centric frontend to architecting a secure, relational PostgreSQL backend with strict RLS policies, Moneyball proves the ability to take a complex product requirement and engineer it into a deployed, production-ready application. Additionally, it served as an exercise in modern AI-assisted development, leveraging LLMs for rapid prototyping and debugging to accelerate the engineering lifecycle.