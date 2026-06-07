# Planned Data Architecture: Urban Mining Feedstock Intelligence System

## Purpose

This document defines the planned data architecture for the Urban Mining Feedstock use case inside the Breakthrough Urban Mining Feedstock Raise repository.

The goal is to build a relationship-driven and context-aware intelligence system for identifying, qualifying, prioritizing, and securing high-value electronic feedstock such as printed circuit boards, retired servers, telecom equipment, enterprise electronics, and related material streams.

This architecture follows the graph, knowledge graph, and context graph methodology:

```text
Graph
= What is connected?

Knowledge Graph
= What do those connections mean?

Context Graph
= What matters right now?

RIOS / Feedstock Intelligence
= What action should we take next?
```

---

## Strategic Objective

Urban mining feedstock is the practical equivalent of ore reserves in conventional mining.

The primary objective of the system is to help Breakthrough Management and its operating partners identify and secure control of high-value electronic waste streams before competitors discover or reprice them.

The system should prioritize:

- PCB-rich material
- retired servers
- data center equipment
- telecom equipment
- enterprise network hardware
- industrial electronics
- UPS systems
- electronic manufacturing scrap
- IT refresh and decommissioning opportunities

The key KPI is not generic lead generation.

The key KPI is:

```text
Dollars of qualified feedstock opportunity identified and secured per month.
```

---

## Architecture Overview

The planned data architecture has four intelligence layers.

```text
1. Graph Layer
   What is connected?

2. Knowledge Graph Layer
   What does it mean?

3. Context Graph Layer
   What matters right now?

4. Action / Execution Layer
   What should be done next?
```

This structure converts raw market data into prioritized feedstock opportunities.

---

## Layer 1: Graph Layer

### Core Question

```text
What is connected?
```

The graph layer stores relationships between entities.

### Core Entities

```text
Company
Facility
Contact
Feedstock
Asset
Broker
Recycler
Investor
Project
Opportunity
Signal
Conversation
LOI
Shipment
Capital Source
Grant Program
Processing Partner
```

### Core Relationships

```text
Company OWNS Facility
Company OPERATES Facility
Facility STORES Feedstock
Facility GENERATES Feedstock
Feedstock CONTAINS Material
Contact WORKS_FOR Company
Contact INFLUENCES Opportunity
Broker INTRODUCED Opportunity
Investor INTERESTED_IN Project
Company DISPOSING_OF Asset
Asset LOCATED_AT Facility
Signal INDICATES Opportunity
Conversation REFERENCES Opportunity
LOI SECURES Feedstock
Shipment MOVES Feedstock
Capital Source FUNDS Acquisition
Grant Program SUPPORTS R&D
Processing Partner RECOVERS Material
```

### Example Relationship Chain

```text
University
  -> owns
Data Center Facility
  -> replacing
Retired Server Equipment
  -> contains
PCB-rich Feedstock
  -> creates
Feedstock Acquisition Opportunity
```

---

## Layer 2: Knowledge Graph Layer

### Core Question

```text
What do these connections mean?
```

The knowledge graph adds business meaning to the raw relationships.

A retired server is not just equipment. It is potential feedstock.

A telecom upgrade is not just an IT project. It may indicate future board, server, cabling, and network hardware disposal.

A municipal surplus auction is not just an auction. It may be a recurring source of decommissioned electronics.

### Entity Meaning Examples

```text
Server Rack
= Potential Feedstock

PCB Material
= Precious Metals Bearing Material

Hospital
= Potential Enterprise Feedstock Source

University
= Potential Enterprise Feedstock Source

Telecom Company
= Potential Telecom Electronics Source

Municipality
= Potential Surplus / Procurement Source

Broker
= Relationship Access Node

Investor
= Feedstock Acquisition Capital Source
```

### Material Intelligence

Feedstock should be tagged by expected recoverable material category where information is available:

```text
Gold
Silver
Copper
Palladium
Aluminum
Steel
Mixed plastics
Battery-related materials
```

### Source Type Classification

Organizations should be classified into source types:

```text
Data Center
Hospital / Healthcare Network
University / College
Municipality
Telecom Company
Bank / Financial Institution
Enterprise Office Network
Government Agency
IT Asset Disposition Firm
Electronics Recycler
Manufacturer
Industrial Facility
Auction Platform
Broker / Aggregator
```

---

## Layer 3: Context Graph Layer

### Core Question

```text
What matters right now?
```

The context graph filters the knowledge graph based on the current mission, constraints, timing, relationships, and business priority.

Example mission:

```text
Secure high-grade PCB and retired server material within the next 90 days to support the $5M feedstock acquisition raise.
```

The context graph should prioritize:

```text
Data center closures
Enterprise server refreshes
Hospital IT upgrades
University equipment refreshes
Telecom hardware replacements
Municipal surplus auctions
Bank branch consolidations
Government technology decommissions
Known warm introductions
Prior conversations with feedstock holders
Opportunities that can produce LOIs
Opportunities that can support investor diligence
```

The context graph should deprioritize:

```text
Low-grade consumer electronics
Small household e-waste drives
Unverified brokers
Material without chain-of-custody clarity
Signals with no current disposal event
Targets with low relationship access
Targets outside practical logistics range
```

---

## Layer 4: Action / Execution Layer

### Core Question

```text
What should be done next?
```

The execution layer turns context into workflow.

Potential next-best actions:

```text
Research account
Find decision maker
Find warm introduction
Send supplier education email
Send Vidyard explainer
Record personalized Loom follow-up
Book supplier discovery call
Request inventory list
Request photos
Request weight estimate
Request chain-of-custody details
Draft LOI
Escalate to Gilbert for material qualification
Escalate to Andrew for strategic relationship
Escalate to Dennis for investor/capital linkage
Add to data room evidence package
```

---

## Signal Intelligence Layer

Signals are external or internal events that may indicate feedstock availability.

### Public Signals

```text
Company closure
Facility closure
Office consolidation
Data center shutdown
Merger or acquisition
Bankruptcy or restructuring
Equipment liquidation
Corporate sustainability report
E-waste disposal initiative
```

### Procurement Signals

```text
New IT infrastructure contract
Server replacement tender
Data center migration tender
Telecom network refresh
Government IT modernization project
Hospital technology upgrade
University infrastructure modernization
```

### Job Signals

```text
Data Center Migration Manager
IT Decommissioning Lead
Infrastructure Upgrade Manager
Asset Recovery Specialist
Surplus Asset Manager
Procurement Manager
Facilities Manager
Sustainability Manager
```

### Real Estate / Facility Signals

```text
Office move
Warehouse closure
Campus consolidation
Facility sale
Data center relocation
Industrial tenant move-out
```

### Relationship Signals

```text
Known contact works at target company
Broker has access to feedstock source
Supplier previously handled similar material
Investor has funded circular economy assets
Strategic partner has facility access
Existing conversation mentions disposal need
```

---

## Opportunity Scoring Model

Each feedstock opportunity should receive a score based on fit, urgency, relationship access, material quality, and strategic value.

### Suggested Scoring Dimensions

```text
Material Fit Score
Source Quality Score
Volume Potential Score
Timing / Urgency Score
Relationship Access Score
Logistics Feasibility Score
Chain-of-Custody Confidence Score
Investor Diligence Value Score
LOI Probability Score
Strategic Partner Value Score
```

### Example Signal Scores

```text
Data center closure = 95
Hospital server refresh = 90
University infrastructure upgrade = 85
Municipal surplus auction = 80
Bank branch consolidation = 75
Enterprise office move = 70
Generic office equipment sale = 45
Consumer e-waste drive = 20
```

---

## Data Model Draft

### organizations

```text
id
name
organization_type
industry
website
location
region
source_type
status
notes
created_at
updated_at
```

### facilities

```text
id
organization_id
name
facility_type
address
city
state_or_province
country
logistics_notes
status
created_at
updated_at
```

### contacts

```text
id
organization_id
first_name
last_name
title
email
phone
linkedin_url
role_type
relationship_strength
notes
created_at
updated_at
```

### feedstock_assets

```text
id
organization_id
facility_id
asset_type
material_category
estimated_weight
estimated_units
expected_recoverable_materials
grade_estimate
condition
chain_of_custody_status
photo_links
notes
created_at
updated_at
```

### signals

```text
id
organization_id
facility_id
signal_type
signal_source
signal_url
signal_date
summary
relevance_score
confidence_score
created_at
updated_at
```

### opportunities

```text
id
organization_id
facility_id
primary_contact_id
opportunity_type
feedstock_asset_id
stage
material_fit_score
source_quality_score
volume_potential_score
timing_score
relationship_access_score
logistics_score
chain_of_custody_score
investor_diligence_score
loi_probability_score
total_opportunity_score
next_best_action
owner
created_at
updated_at
```

### relationships

```text
id
source_entity_type
source_entity_id
relationship_type
target_entity_type
target_entity_id
strength
confidence
source
notes
created_at
updated_at
```

### conversations

```text
id
organization_id
contact_id
opportunity_id
conversation_type
summary
key_commitments
next_steps
follow_up_date
created_by
created_at
updated_at
```

### lois

```text
id
opportunity_id
organization_id
feedstock_asset_id
status
estimated_volume
estimated_value
terms_summary
review_required
counsel_review_status
signed_date
created_at
updated_at
```

### shipments

```text
id
loi_id
opportunity_id
origin_facility_id
destination_facility_id
estimated_weight
actual_weight
shipment_status
chain_of_custody_documentation
created_at
updated_at
```

---

## Agent Workforce Design

### Worker 1: Feedstock Signal Hunter

Finds potential feedstock signals from public, procurement, auction, closure, and facility-change sources.

Outputs:

```text
Signal records
Target organizations
Opportunity candidates
Source URLs
Initial relevance score
```

### Worker 2: Organization Research Worker

Researches target accounts.

Outputs:

```text
Organization profile
Facilities
Decision makers
Procurement contacts
Sustainability contacts
IT / facilities contacts
Known vendors
Recent initiatives
```

### Worker 3: Relationship Intelligence Worker

Builds relationship paths.

Outputs:

```text
Warm introduction paths
Known contact overlaps
Broker / advisor connections
Investor / supplier relationship links
Relationship strength scores
```

### Worker 4: Feedstock Value Worker

Estimates potential value and operational relevance.

Outputs:

```text
Estimated asset category
Estimated volume
Estimated weight
Material category
Likely recoverable metals
Preliminary value assumptions
Qualification questions for Gilbert
```

### Worker 5: Capital Formation Worker

Links qualified feedstock opportunities to capital strategy.

Outputs:

```text
Investor diligence evidence
LOI package requirements
Capital requirement estimate
Working capital need
Grant / R&D relevance
Data room evidence updates
```

---

## Planned System Flow

```text
Signal Detected
  ↓
Organization Created / Updated
  ↓
Facility Identified
  ↓
Contact / Decision Maker Mapped
  ↓
Feedstock Asset Hypothesis Created
  ↓
Relationship Path Checked
  ↓
Opportunity Score Calculated
  ↓
Next Best Action Assigned
  ↓
Supplier Outreach / Warm Introduction
  ↓
Discovery Call
  ↓
Material Qualification
  ↓
LOI / Feedstock Commitment
  ↓
Investor Diligence Evidence
  ↓
Capital Formation Support
```

---

## Implementation Notes

### MVP Storage Recommendation

Do not begin with a dedicated graph database unless relationship volume and query complexity require it.

Start with:

```text
Supabase
Postgres relationship tables
MotherDuck / DuckDB analytical layer
ICM markdown workspaces
Structured JSON records
Hermes context orchestration
```

### Future Graph Upgrade Path

Neo4j or another graph database can be evaluated later when the system requires:

```text
high-volume relationship traversal
multi-hop relationship queries
enterprise-scale entity resolution
real-time graph analytics
large-scale context retrieval for agents
```

### Principle

The system should be graph-aware before it becomes graph-database-dependent.

---

## Initial MVP Priorities

1. Define source type taxonomy.
2. Build target account master list.
3. Create basic organization, contact, signal, opportunity, and relationship tables.
4. Add feedstock asset records.
5. Add opportunity scoring.
6. Add next-best-action field.
7. Connect outreach and video engagement signals.
8. Track supplier discovery calls.
9. Convert qualified supplier conversations into LOIs.
10. Use LOIs and qualified feedstock evidence to support the $5M raise.

---

## Success Metrics

### Feedstock Metrics

```text
Qualified supplier accounts researched
Feedstock signals detected
Feedstock opportunities created
Supplier conversations completed
Estimated tonnes identified
Estimated tonnes qualified
LOIs drafted
LOIs signed
Shipment opportunities identified
```

### Intelligence Metrics

```text
Relationship paths discovered
Warm introductions identified
Signals converted into opportunities
Opportunities with complete decision-maker mapping
Opportunities with material qualification notes
Average opportunity score
Next-best-action completion rate
```

### Capital Formation Metrics

```text
Feedstock evidence packages created
LOIs added to data room
Investor diligence questions answered using feedstock data
Capital linked to specific acquisition opportunities
Investor engagement improved through feedstock proof
```

---

## Governance Notes

- Gilbert Jones should review material qualification assumptions.
- Andrew Ferguson should review strategic partner and executive-level opportunities.
- Dennis Eng should own GTM engineering, relationship intelligence, investor linkage, data room coordination, and digital collateral workflow.
- Any investor-facing claims, valuation assumptions, offering documents, or securities-related communications must be reviewed by qualified securities counsel before use.

---

## Working Doctrine

```text
Graph = Who and what is connected.
Knowledge Graph = What those connections mean.
Context Graph = What matters for the mission right now.
RIOS = What action should be taken next.
```

For the Urban Mining Feedstock use case, the mission is clear:

```text
Find, qualify, and secure high-value electronic feedstock that strengthens the $5M raise and validates the Urban Mining platform.
```
