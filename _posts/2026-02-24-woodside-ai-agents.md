---
title: "Industrial AI at Woodside Energy: Architecting 5 Production-Ready AI Workflows"
date: 2026-02-24 20:00:00 +0530
categories: [Experience, Industrial AI]
tags: [rag, copilot-studio, power-automate, llm-evaluation, data-engineering]
---

**Role:** Data & AI Intern  
**Location:** Perth, Australia  
**Timeline:** Nov 2025 – Feb 2026  

During my 12 weeks with Woodside Energy's AI Team, my objective was to bridge the gap between raw Large Language Model capabilities and complex organizational bottlenecks. I moved beyond simple prompt engineering to architect and deploy five distinct, production-ready AI solutions across Strategy, Corporate Affairs, and Engineering.

### 1. Lumina AI Platform: Automated Feedback & Triage System
**The Problem:** Woodside’s internal AI platform (Lumina) received weekly user feedback via an Excel drop. A Principal Product Lead and 15 Engagement Leads spent hours manually reviewing chat histories, classifying issues, and assigning ownership in weekly meetings, with no system for outcome tracking.  

**The Solution:** I built an automated classification and triage pipeline using Copilot Studio, Microsoft Lists, and Power BI. 
* **The Workflow:** When feedback drops, a flow triggers an AI agent that analyzes the conversation history and user comment. 
* **RAG Integration:** The agent uses RAG against an internal agent catalogue to identify the specific agent, determine if the issue is a bug, user error, or expected knowledge gap, and assign the correct owner.
* **Security & Action:** The AI flags sensitive information (routing it to a secure list) and automatically pings the assigned owner via Teams.  

**Impact:** Weekly manual triage meetings were canceled and replaced with a Power BI dashboard tracking issue resolution and agent health metrics.

### 2. PBO Benchmarking Knowledge Agent
**The Problem:** The Benchmarking Lead in Houston possessed a massive knowledge base of 120 transcribed, hour-long interviews with Woodside VPs and project leads. Accessing this strategic knowledge required manual review and days of waiting.  

**The Solution:** I developed a specialized RAG Knowledge Agent deployed on the Lumina platform.  
* **Iterative Engineering:** I built and tested multiple agents using different LLMs and retrieval methods (single folder vs. combined files) to optimize response accuracy across 26 test questions.
* **Structured Output:** The agent doesn't just chat; it returns structured data including summaries, anonymized quotes, answer confidence (based on stakeholder consensus), and response metadata (recency and roles of interviewees).  

**Impact:** Project managers globally can now instantly query 120 leadership viewpoints on topics like green hydrogen and decommissioning practices.  

### 3. Corporate Affairs: SI Report Automation
**The Problem:** The Environment team spent hours manually copy-pasting and formatting 500-600 page Sensitive Information (SI) reports from raw Excel exports of stakeholder communications.  

**The Solution:** I architected an automated document generation flow using Copilot Studio.
* **Data Processing:** The flow parses the Excel data, groups communications by unique stakeholders, and uses an AI node to clean and reformat raw email text (fixing spacing, adding bullets, removing signatures).
* **Document Generation:** It then loops through the structured data to automatically populate repeating sections in a Microsoft Word template, generating hundreds of perfectly formatted, date-ordered documents ready for merging.

### 4. Strategy Team: LLM Chart Data Extraction
**The Project:** The Strategy team needed to extract underlying data tables from static charts in reports and PDFs.  

**The Execution:** I designed a test harness with 15 charts and ~350 data points to benchmark 5 models (GPT 5.1 Fast, GPT 5.1 Think, Copilot Chat, Gemini 3, Claude 4.5).  

**The Outcome:** I delivered a technical report calculating Accuracy, RMSE, and MAPE, alongside a company-wide blog post detailing AI capabilities, shortfalls, and advanced prompting techniques (e.g., forcing visualization rendering) for data extraction tasks.

### 5. Engineering: SPI Drawing Governance Checks
**The Project:** Automating governance checks for Smart Plant Instrumentation (SPI) drawings by comparing Yellow Copy (YC), Check Print (CP), and As-Built (AB) PDFs.  

**The Execution:** I trained a custom AI model using Power Automate AI Builder to detect title block fields. The flow groups related drawings, extracts the JSON data, and performs 26 deterministic engineering standard checks (comparing YC to CP to AB), updating a tracking list with pass/fail statuses.

---

### Scaling AI Literacy
Beyond building infrastructure, driving user adoption is critical. I designed and led a hands-on technical workshop for 50 interns, taking them from basic prompting to architecting their own functional, knowledge-based AI tools.