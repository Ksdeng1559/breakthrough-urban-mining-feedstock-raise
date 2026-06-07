# ROADMAP.md

## Objective

Deploy a RIOS/OpenClaw-style feedstock acquisition intelligence workspace for Breakthrough Urban Mining / MineTeck.

The system should help identify, qualify, validate, value, and pursue electronic feedstock opportunities before they reach public auctions or commodity recyclers.

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
- Source validation framework

---

## Phase 2: Source Validation Layer

### Goal

Prevent the system from overstating potential feedstock sources as confirmed suppliers.

### Deliverables

- Source confidence ladder: Speculative → Potential → Qualified → Verified → Confirmed → Recurring Source
- Feedstock source validation framework
- Source validation worker
- Investor-safe language rules
- Human approval rules for naming sources in investor materials

### Priority Source Categories

- Existing recycling depots and recycling centres
- E-waste collection networks
- ITAD firms
- OEM return/refurbishment channels such as Samsung, Dell, HP, Lenovo, and Cisco
- Telecom infrastructure sources
- Data centres and MSPs
- Government and defence surplus pathways, including U.S. Department of Defense-style channels where legally and commercially accessible

Important note:

These categories should be treated as potential or verified channels only until evidence confirms direct access, material availability, or a relationship pathway.

---

## Phase 3: Worker Setup

### Goal

Create OpenClaw-style worker files that can be used by RIOS/Hermes.

### Deliverables

- Worker 00: Domain Knowledge Capture
- Worker 01: Feedstock Signal Hunter
- Worker 02: Feedstock Classifier
- Worker 03: Recovery Economics
- Worker 04: Relationship Mapper
- Worker 05: Opportunity Ranker
- Worker 06: Source Validation

---

## Phase 4: Manual Pilot

### Goal

Validate the system manually before automating outreach or purchase decisions.

### Pilot Targets

- Research 50 potential sources
- Classify each source by confidence level
- Identify 20 qualified feedstock opportunities
- Review 10 with Gilbert
- Create 5 high-priority acquisition briefs
- Validate at least 3 source access pathways

---

## Phase 5: RIOS Integration

### Goal

Move structured data into RIOS infrastructure.

### Components

- Supabase for organizations, contacts, opportunities, source confidence status, yield assumptions, and lot results
- MotherDuck/DuckDB for analytics and margin modeling
- Markdown/Wiki memory for domain knowledge
- Hermes Agent for coordination
- Python workers for repeatable research, scoring, and validation

---

## Phase 6: Capital Raise Support

### Goal

Use the feedstock intelligence system as part of the investor story.

### Investor Narrative

Breakthrough / MineTeck is not only building an Urban Mining operation. It is building a proprietary feedstock intelligence engine that can identify, validate, evaluate, and secure high-value electronic material before competitors know it is available.

### Investor-Safe Source Language

Use:

- Potential source category
- Qualified source
- Verified disposal pathway
- Confirmed source
- Recurring source

Avoid claiming that major enterprises, OEMs, government agencies, or defence organizations are suppliers unless verified by evidence, relationship access, contract, or direct confirmation.
