# ROADMAP.md

## Objective

Deploy a RIOS/OpenClaw-style feedstock acquisition intelligence workspace for Breakthrough Urban Mining / MineTeck.

The system should help identify, qualify, value, and pursue electronic feedstock opportunities before they reach public auctions or commodity recyclers.

---

## Phase 1: Knowledge Capture

### Goal

Capture Gilbert Jones' feedstock expertise and convert it into reusable worker instructions.

### Deliverables

- Gilbert Jones interview guide
- Feedstock ontology
- Recovery economics assumptions
- Risk rules
- Source maps
- Initial acquisition playbook

---

## Phase 2: Worker Setup

### Goal

Create OpenClaw-style worker files that can be used by RIOS/Hermes.

### Deliverables

- Worker 00: Domain Knowledge Capture
- Worker 01: Feedstock Signal Hunter
- Worker 02: Feedstock Classifier
- Worker 03: Recovery Economics
- Worker 04: Relationship Mapper
- Worker 05: Opportunity Ranker

---

## Phase 3: Manual Pilot

### Goal

Validate the system manually before automating outreach or purchase decisions.

### Pilot Targets

- Research 50 organizations
- Score 20 feedstock opportunities
- Review 10 with Gilbert
- Create 5 high-priority acquisition briefs

---

## Phase 4: RIOS Integration

### Goal

Move structured data into RIOS infrastructure.

### Components

- Supabase for organizations, contacts, opportunities, yield assumptions, and lot results
- MotherDuck/DuckDB for analytics and margin modeling
- Markdown/Wiki memory for domain knowledge
- Hermes Agent for coordination
- Python workers for repeatable research and scoring

---

## Phase 5: Capital Raise Support

### Goal

Use the feedstock intelligence system as part of the investor story.

### Investor Narrative

Breakthrough / MineTeck is not only building an Urban Mining operation. It is building a proprietary feedstock intelligence engine that can identify, evaluate, and secure high-value electronic material before competitors know it is available.
