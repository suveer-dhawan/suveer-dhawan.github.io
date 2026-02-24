---
title: "AI Sales Assistant: 3-Day Hackathon Prototype"
date: 2026-02-24 21:27:00 +0530
categories: [Projects, SaaS & Product]
tags: [python, streamlit, firebase, oauth2, gemini, hackathon]
pin: true
---

**Role:** Sole Architect / Hackathon Project (Founders Hack)  
**Location:** Melbourne, Australia  
**Timeline:** Aug 2025  

Built over a 3-day sprint at the Founders Hackathon (accelerated using the Cursor AI code editor), this project is a functional proof-of-concept for an AI-powered sales automation platform. The goal was to see how rapidly I could wire together a system that converts raw Google Sheet leads into personalized cold emails. 

While it remains a prototype with room for structural refinement, it successfully demonstrates end-to-end API automation and data handling.

### The Architecture & Stack

To build a working prototype in just 72 hours, I used a modular Python approach:

* **Frontend:** Streamlit (Chosen for rapid UI development and prototyping).
* **Database:** Firebase Firestore (Admin SDK for quick CRUD operations and data persistence).
* **AI Engine:** Google Gemini 2.0 Flash (Optimized for JSON generation).
* **Integrations:** Google Sheets API, Gmail API, and Calendly.

### Core Technical Achievements

**1. Rapid OAuth Integration**
Handling multiple Google APIs within a hackathon time limit is notoriously tricky. I successfully implemented isolated Google OAuth 2.0 flows, separating token storage and scope management for Gmail and Google Sheets to prevent token conflicts.

**2. Intelligent Lead Pipeline**
The system acts as a smart filter. I integrated an ML-based lead scoring model to classify leads as Hot, Warm, or Cold. The platform performs bulk extraction from Google Sheets and writes these statuses directly back to the Firebase database.

**3. Structured AI Generation**
I engineered the Gemini model to output personalized email content and sentiment analysis strictly as structured JSON. The generation engine was also programmed to automatically inject the user's Calendly links into the email payload.

**4. The Campaign UI**
I built a functional campaign manager interface within Streamlit to trigger email sequences and provide a visual dashboard for the lead pipeline.

### The Takeaway

This 3-day sprint was a deep dive into rapid prototyping. By successfully wiring together predictive ML, generative AI, secure OAuth flows, and data persistence into a cohesive tool, I proved how quickly modern AI development tools like Cursor can be leveraged to build complex microservices from scratch.