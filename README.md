# finguard-ai

An AI-powered FinTech platform built with React, Node.js, TypeScript &amp; PostgreSQL to automate dispute resolution, fraud analysis, and smart B2B refunds.

# FinGuard AI — Automated FinTech Dispute & Compliance Platform

[![React](https://shields.io)](#)
[![Node.js](https://shields.io)](#)
[![TypeScript](https://shields.io)](#)
[![PostgreSQL](https://shields.io)](#)
[![OpenAI](https://shields.io)](#)

FinGuard AI is a production-ready B2B SaaS platform designed for FinTech companies (e.g., Stripe, Revolut frameworks) to automate the resolution of low-risk customer transaction disputes, chargebacks, and double-billing complaints using Contextual AI [1.1]. 

By deploying an autonomous AI Compliance Agent with **Function Calling capabilities**, the system filters transactions, calculates risk profiles, and executes straight-through refunds under €50 autonomously [1.1]. This shifts up to **74% of redundant ticket volume** away from human compliance operations.

---

## Key Business & AI Automation Features

* Autonomous AI Agent:** Leverages OpenAI Assistants API (v2) with custom system tools to analyze banking transactions in real-time.
* Dynamic Function Calling:** The AI doesn't just reply textually—it securely executes real database queries (`get_user_transactions`) and balance mutations (`process_refund`) via Node.js when conditions match.
* Executive Admin Dashboard:** A rich, responsive monitoring panel built with React, TypeScript, and Tailwind CSS to track automated ROI, fraud risk logs, and system load.
* Real-Time Synchronization:** Uses Socket.io (WebSockets) to dynamically push live customer-bot interaction feeds to human compliance team managers.
* GDPR & Regulatory Compliance:** Built with privacy-first standards. Implements automated PII masking (names, full card numbers) before data payload compilation to external LLM token pipelines, adhering to the Central Bank of Ireland framework.

---

## System Architecture & AI in Action

### 1. Straight-Through Processing (Automated Refund)
*Place your GIF here showing a customer asking for a refund under €50, the AI calling the refund function, and the Admin Dashboard instantly flashing the update via WebSockets.*
`![AI Automation Demo](./path-to-your-gif1.gif)`

### 2. Live Operations Dashboard & High-Risk Escalation
*Place your GIF here showing the React Admin Dashboard tracking the live dispute feed, calculation of AI Risk Scores (0-100), and automated handoff to a human agent when a high-risk score triggers.*
`![Admin Dashboard Demo](./path-to-your-gif2.gif)`

---

## Technical Stack & Project Architecture

*   **Frontend:** React (TypeScript), Vite, Tailwind CSS, Lucide Icons, Component-Driven Feature Architecture.
*   **Backend:** Node.js (TypeScript), Express.js / NestJS architecture, RESTful API routing.
*   **Database:** PostgreSQL (with ACID-compliant multi-row transactional verification).
*   **AI Layer:** OpenAI Assistants API (v2) Thread management, RAG (Retrieval-Augmented Generation) mapping, and Function Tokenizers.

```text
finguard-ai/
├── backend/
│   ├── src/
│   │   ├── config/          # Environment configuration & DB connections
│   │   ├── modules/
│   │   │   ├── auth/        # JWT Authentication & Role-Based Access Control
│   │   │   ├── transactions/# Financial ledger core business logic
│   │   │   ├── disputes/    # AI Decision logs and ticket state machine
│   │   │   └── ai-agent/    # OpenAI Assistants & Tools integration layer
│   │   └── server.ts        # Express entry point + Socket.io hub
└── frontend/
    ├── src/
    │   ├── components/      # Global UI components (Shadcn/ui design patterns)
    │   ├── features/        # Feature-scoped modules (Dashboard, ActiveChat)
    │   └── services/        # Secured Axios client interceptors
```

---

## Local Installation & Setup

### Prerequisites
*   Node.js (v18 or higher)
*   PostgreSQL Instance
*   OpenAI API Key

### 1. Backend Setup
```bash
cd backend
npm install
# Create a .env file based on .env.example with your DATABASE_URL and OPENAI_API_KEY
npm run dev
```

### 2. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```
