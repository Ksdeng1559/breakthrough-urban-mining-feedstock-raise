# Urban Mining Feedstock Outbound SOP

## Purpose

Build an intelligence-led outbound system that identifies, qualifies, and activates urban mining feedstock opportunities before they reach the open market.

This SOP is designed for demolition, redevelopment, infrastructure replacement, e-waste, industrial asset recovery, and circular economy feedstock acquisition.

## Core Outcome

Create a repeatable system that converts public and private market signals into qualified feedstock relationships, site assessments, recovery agreements, and buyer/offtake opportunities.

```text
Signal Detected
  -> Opportunity Researched
  -> Feedstock Potential Scored
  -> Decision Makers Mapped
  -> Personalized Outreach Created
  -> Campaign Sent
  -> Meeting Booked
  -> Site Assessment
  -> Feedstock Agreement / Recovery Contract
```

## Operating Principles

1. Lead with intelligence, not generic cold email.
2. Prioritize projects before demolition, disposal, or procurement decisions are finalized.
3. Build relationships with repeat feedstock sources, not one-off transactions.
4. Capture every finding as reusable market intelligence.
5. Score opportunities before outreach to protect time, reputation, and sending infrastructure.

---

## Phase 1: Signal Discovery

### Objective

Find early indicators of recoverable materials, asset disposal, or feedstock supply before competitors see the opportunity.

### Primary Signal Sources

- Demolition permits
- Building permits
- Rezoning applications
- Development applications
- Municipal tender portals
- Public asset disposal notices
- Utility upgrade announcements
- Telecom infrastructure upgrades
- Data center decommissioning notices
- Industrial shutdowns
- Warehouse closures
- Manufacturing byproduct streams
- Construction and demolition waste projects
- E-waste collection programs

### Tools

- TinyFish for website and state-change monitoring
- Tavily for web research and source discovery
- Scrapling for structured extraction
- Municipal open data portals
- RSS feeds and tender alerts
- RIOS opportunity database

### Required Output

Each discovered signal creates an `Urban Mining Opportunity Record` with:

```text
Project Name
Address / Region
Signal Type
Source URL
Owner / Developer / Operator
Permit or Tender Status
Estimated Timeline
Potential Material Streams
Confidence Level
Next Action
```

---

## Phase 2: Opportunity Qualification

### Objective

Determine whether the signal is worth outreach.

### Qualification Criteria

Score each opportunity from 1 to 5 across:

- Estimated recovery value
- Material relevance
- Timing urgency
- Accessibility
- Contactability
- Relationship potential
- Repeat opportunity potential
- Strategic value

### Material Categories

- Copper
- Aluminum
- Steel
- Stainless steel
- Electrical equipment
- Switchgear
- HVAC units
- Generators
- Batteries
- Servers and IT equipment
- Telecom equipment
- Industrial machinery
- Construction and demolition material
- E-waste

### Opportunity Grades

```text
A = Immediate outreach
B = Monitor and enrich
C = Archive for future review
D = Ignore unless new signal appears
```

### Required Output

```text
Opportunity Score
Grade
Reason for Grade
Estimated Material Streams
Estimated Decision Window
Recommended Outreach Angle
```

---

## Phase 3: Relationship Mapping

### Objective

Identify the people and organizations most likely to control access to the feedstock opportunity.

### Target Organizations

- Developers
- Property owners
- Demolition contractors
- Construction managers
- Facilities managers
- Asset managers
- Municipal procurement teams
- Electrical contractors
- Telecom operators
- Utility companies
- Industrial plant managers
- Recyclers
- Scrap processors
- Logistics providers
- Offtake buyers

### Target Roles

- Owner
- President
- VP Operations
- Project Manager
- Site Superintendent
- Procurement Manager
- Sustainability Manager
- Facilities Director
- Asset Recovery Manager
- Demolition Manager
- Construction Manager

### Required Output

```text
Company
Contact Name
Role
Email
Phone
LinkedIn URL
Relationship Path
Decision Influence
Recommended First Touch
```

---

## Phase 4: Interpretive Context Research

### Objective

Create relevant outreach based on the opportunity, the recipient's role, and the business context.

### Research Inputs

- Company website
- Project page
- Press releases
- Permit data
- Tender data
- Sustainability reports
- ESG statements
- Prior projects
- LinkedIn activity
- Municipal planning notes

### Interpretive Context Questions

- Why does this opportunity matter now?
- What material recovery angle is most relevant?
- Who benefits from acting early?
- What risk exists if recovery is not planned before demolition or disposal?
- What sustainability, cost recovery, or compliance angle applies?
- Is the target likely motivated by revenue, convenience, ESG, diversion targets, or disposal cost reduction?

### Required Output

```text
Opportunity Narrative
Recipient-Specific Relevance
Problem / Timing Trigger
Likely Motivation
Suggested Offer
Outreach Personalization Notes
```

---

## Phase 5: Outreach Sequence

### Objective

Start a practical conversation around recovery, assessment, or feedstock supply.

### Sequence Overview

```text
Day 1: Email 1 - Opportunity awareness
Day 3: Email 2 - Recovery / value angle
Day 6: Phone or voicemail
Day 8: LinkedIn view / connection
Day 11: Email 3 - Assessment offer
Day 16: Final follow-up
```

### Email 1: Opportunity Awareness

Subject options:

```text
Material recovery opportunity at [Project]
Question about [Project] recovery planning
Before demolition begins at [Address]
```

Core message:

```text
Hi [First Name],

I noticed [specific project / permit / redevelopment signal]. Projects like this can contain recoverable copper, aluminum, steel, electrical equipment, HVAC assets, and other material streams if recovery is planned before demolition or disposal.

Would it be worth a quick conversation to see whether there is a recovery or diversion opportunity before the project moves further?

Best,
[Name]
```

### Email 2: Value Angle

Purpose: add a reason to respond.

Possible angles:

- Reduce disposal cost
- Recover material value
- Support diversion targets
- Improve ESG reporting
- Simplify asset removal
- Create a feedstock agreement

### Call / Voicemail

Goal: confirm the correct decision maker and ask whether material recovery is already planned.

### Email 3: Assessment Offer

Offer a simple next step:

```text
We can complete a preliminary urban mining assessment using project details, site type, and likely material streams before anyone commits to a full site review.
```

### Final Follow-Up

Keep it respectful and simple:

```text
Should I close the loop, or is there someone else responsible for recovery, demolition planning, or asset disposition on this project?
```

---

## Phase 6: Pipeline Management

### Pipeline Stages

```text
Signal Detected
Researching
Qualified
Decision Maker Mapped
Outreach Ready
Outreach Sent
Contacted
Meeting Scheduled
Site Assessment
Proposal
Negotiation
Contracted
Completed
Nurture / Monitor
Closed Lost
```

### Required Fields

```text
Opportunity Name
Company
Project Address
Signal Source
Material Streams
Opportunity Grade
Estimated Value Range
Pipeline Stage
Next Action
Next Action Date
Owner
Last Touch
Response Status
Meeting Date
Outcome
```

---

## Phase 7: Referral and Partner Network Development

### Objective

Build a recurring supply network, not just one-off projects.

### Priority Partner Types

- Demolition contractors
- Developers
- Property managers
- Electrical contractors
- Facilities managers
- Municipal procurement contacts
- Telecom contractors
- Utility contractors
- Industrial maintenance firms
- Scrap processors
- Logistics companies
- Environmental consultants

### Partner Outreach Angle

```text
We help identify and monetize recoverable material streams before demolition, disposal, or decommissioning. We are looking for repeat partners where early assessment creates better recovery, diversion, and revenue outcomes.
```

---

## Phase 8: Intelligence Feedback Loop

### Objective

Improve future discovery, scoring, and outreach based on real outcomes.

### Capture After Every Opportunity

```text
Signal Source
Material Found
Estimated vs Actual Value
Decision Maker Accuracy
Sales Cycle Length
Objections
Winning Angle
Lost Reason
Recovery Partner Used
Offtake Buyer Used
Next Similar Opportunity
```

### Knowledge Storage

- Supabase as system of record
- DuckDB / MotherDuck for analysis
- Qdrant for semantic retrieval
- Obsidian for playbooks and field notes
- RIOS knowledge graph for relationship mapping

---

## RIOS Urban Mining Stack

```text
TinyFish / Tavily / Scrapling
  -> Signal Discovery
RIOS Interpretive Context Engine
  -> Opportunity Narrative
Supabase / DuckDB / Qdrant / Obsidian
  -> Knowledge and Memory
Mystrika / DoYouMail
  -> Outbound Execution and Inbox Infrastructure
RIOS CRM
  -> Pipeline, Tasks, Relationships, Outcomes
```

## Success Metrics

### Activity Metrics

- Signals discovered per week
- Opportunities qualified per week
- Decision makers mapped
- Outreach sequences launched
- Meetings booked

### Conversion Metrics

- Positive reply rate
- Meeting booking rate
- Site assessment rate
- Proposal rate
- Contract rate

### Business Metrics

- Feedstock agreements created
- Estimated material value identified
- Actual recovery value
- Revenue per opportunity
- Revenue per relationship
- Repeat partner rate

## MVP Scope

Start with one region and one feedstock category.

Recommended MVP:

```text
Region: Metro Vancouver / Lower Mainland
Feedstock Category: Demolition and redevelopment recovery
Primary Targets: Developers, demolition contractors, property managers
Primary Signals: Demolition permits, development applications, tender notices
```

## Codex Build Notes

Create the following modules first:

```text
/opportunities
  Urban mining opportunity records

/research
  Signal ingestion and enrichment

/scoring
  Feedstock opportunity score

/outreach
  Email sequence generator

/pipeline
  RIOS opportunity stages

/knowledge
  Playbooks, outcomes, and reusable insights
```
