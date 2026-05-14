# PULSE — PRODUCT DEFINITION
*What it is. What it does. How it works.*
*Version 1.0 | May 2026*

---

## THE ONE-SENTENCE DESCRIPTION

Pulse is a company-specific AI analyst that lives on a dashboard — built through
conversation, fed by whatever data the business actually has.

---

## THE PROBLEM IT SOLVES

Most small business owners run their business across 5–8 disconnected tools.
Sales in Square. Appointments in Vagaro. Team in 7shifts. Reviews on Google.
Promos on Instagram. None of them talk to each other.

At the end of a bad month, they have no idea why it was bad. Every decision
is made on gut feel because pulling the data together takes hours they don't have.

Pulse gives them one place to see what's happening across their whole business —
and an AI they can ask questions to, in plain English, that actually knows their
specific company.

---

## WHAT MAKES THIS DIFFERENT

**From native POS analytics (Square, Vagaro):**
Those tools show you what happened inside that tool.
Pulse shows you what's happening across every tool you use — and explains it.

**From enterprise BI (Looker, Domo):**
Those are built for analysts with IT teams.
Pulse is built for an owner who checks their phone between appointments.

**From replacement platforms (Thryv, Broadly):**
Those ask you to swap your tools.
Pulse connects to what you already have.

**Core positioning:**
*"Your Square dashboard shows you what happened.
Pulse shows you why — and what to do next."*

---

## THE THREE LAYERS

---

### LAYER 1: THE COMPANY MANIFEST

**What it is:**
A structured, persistent profile of the business. The AI's single source of truth.
Nothing is inferred outside of it. Nothing is hallucinated. Ever.

**What it contains:**
- Business name, type, size, locations
- Team structure and roles
- Every tool the business currently uses (the tech stack)
- What decisions the owner makes regularly
- What questions the owner currently can't answer
- What data exists and where it lives
- What data doesn't exist yet
- Permission levels per role (what each person can see)

**How it's built:**
Through a structured onboarding conversation between the owner and an AI guide.
The AI asks questions, the owner answers, and the manifest is built and saved.

In the Wizard of Oz phase, the Founder runs this conversation manually.
In the self-serve phase, this conversation is automated.

**Why it matters:**
The manifest is what makes Pulse company-specific rather than generic.
Every AI interaction — every question answered, every metric displayed,
every insight surfaced — is grounded in this document.

---

### LAYER 2: THE DASHBOARD

**What it is:**
A role-aware display of the metrics that matter to each person on the team.
Not a data dump. Not a report. A curated, confirmed set of numbers the owner
chose because they answer real questions about their business.

**How metrics get on the dashboard:**
1. Owner has a conversation with the AI about what they want to know
2. AI references the manifest to find or reason through where that data lives
3. AI retrieves or estimates the value
4. Owner confirms the value is correct
5. Metric is saved to the dashboard and displayed going forward

**How metrics stay current:**
Each metric is configurable — it can update automatically (via integration),
manually (user enters new value), or on a schedule. The owner controls this
per metric.

**Role-based display:**
- Owner: sees everything
- Manager: sees operations — scheduling, team, floor metrics
- Sales/front desk: sees their own performance metrics
- Custom roles: defined in the manifest during onboarding

**MVP version:**
One owner. One location. Ten metrics. Manual or CSV entry.
No live integrations required for first paying client.

---

### LAYER 3: THE AI CHATBOT

**What it is:**
An in-app AI assistant that is an expert on one specific company.
Not a general-purpose chatbot. Not a generic business advisor.
An AI that knows this business because it has read and internalized
the Company Manifest and has access to every metric on the dashboard.

**What it can do:**
- Answer questions about metrics already on the dashboard
- Explain trends, flag anomalies, suggest what to look at next
- Help a user find data that isn't on the dashboard yet
- When data doesn't exist — reason through where it might be, who on
  the team might have it, and how to start collecting it
- Accept manual data entry from users and store it properly
- Interpret messy, human, qualitative data and integrate it with
  structured metrics
- Respond within the user's role and permission scope

**What it cannot do:**
- Guess, infer, or hallucinate data outside the manifest
- Access any tool or system not documented in the manifest
- Answer questions outside the user's permission level
- Provide information that hasn't been confirmed and stored

**Hard rule:**
When the AI doesn't know something, it says so explicitly.
Then it asks a question that might help locate the answer.
It never fills a gap with a guess.

**Early build version:**
Claude API call with the Company Manifest and current dashboard data
injected as context. A well-prompted conversation with explicit guardrails.
Not an autonomous agent. Not a multi-step pipeline.
One prompt, one response, grounded in real data.

---

## THE ONBOARDING EXPERIENCE

**Step 1 — Industry Preset**
Owner selects their industry (salon/spa in Phase 1).
AI loads industry-specific suggested metrics based on what businesses in
that category typically track. Owner reviews and selects starting point.

**Step 2 — Manifest Conversation**
AI walks owner through a structured conversation:
- What tools do you use?
- What decisions do you make every week?
- What questions do you wish you could answer right now?
- Who else on your team needs to see data?
- What does each person need to see?

Output: a saved Company Manifest.

**Step 3 — First Dashboard**
AI identifies which of the owner's chosen metrics can be pulled from
existing data immediately (CSV, manual entry, or integration).
Owner enters or uploads first data set.
Dashboard displays first 10 metrics.

**Step 4 — First AI Conversation**
Owner asks their first question. AI answers using manifest and dashboard data.
Owner experiences the core value of the product.

**In Wizard of Oz phase:**
The Founder runs Steps 1–4 manually in a live call with the client.
The "onboarding" is a white-glove session.
The experience feels like a product.
The client pays the setup fee for this session.

---

## WHAT IS NOT IN THE PRODUCT (YET)

These are explicitly out of scope until Phase 1 produces paying clients.

| Feature | Why It's Out |
|---|---|
| Live API integrations (except Square) | Integration complexity before validation is a budget trap |
| Automated data refresh | Manual first — proves value before building automation |
| Mobile app | Web app on mobile browser is sufficient |
| Multi-location support | Phase 2 |
| Advanced role permissions | Owner + Manager is enough for MVP |
| Shareable reports | Nice-to-have, not the core value |
| Automated onboarding | Wizard of Oz first — human runs it |
| White-label version | Phase 3 |

---

## THE MVP — FULLY DEFINED

**One owner. One location. Ten metrics. One AI chat.**

The smallest version of Pulse that delivers real value to one real customer:

1. Company Manifest built manually through onboarding conversation
2. Ten metrics defined collaboratively, entered manually or from CSV
3. Dashboard displays those ten metrics, updates manually
4. AI chatbot answers questions about those ten metrics
5. Owner pays setup fee + first month subscription

**Success condition:**
The owner asks the AI a question about their business on Day 1
and gets an answer they couldn't get before.
That's the product working.

---

## DATA AND SECURITY PRINCIPLES

- All client data is stored in a dedicated, isolated environment per company
- OAuth tokens (when integrations are added) are stored encrypted, never exposed
- Role-based access is enforced at the database level, not just the UI
- Manual data entered by users is attributed and timestamped
- No client data is used to train models or shared across accounts
- Compliance requirements (GDPR, CCPA) will be addressed before any
  client data is held at scale — this is an open question requiring a
  dedicated legal review session

---
*Version 1.0 | May 2026*
