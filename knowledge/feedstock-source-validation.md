# Feedstock Source Validation Framework

This file defines how Breakthrough Urban Mining / MineTeck should classify potential feedstock sources before treating them as acquisition targets.

## Core Principle

Do not treat a company, depot, government agency, recycler, or manufacturer as a confirmed feedstock source unless there is evidence that MineTeck, Gilbert Jones, Breakthrough, or an authorized partner has verified access to material.

A source can be strategically attractive and still remain unconfirmed.

## Source Confidence Levels

| Status | Meaning | Evidence Required |
|---|---|---|
| Confirmed | Material has been acquired, directly offered, or verified as available to MineTeck or a trusted partner. | Prior transaction, direct confirmation, written offer, contract, or validated relationship. |
| Verified | The source disposes of relevant material, but MineTeck has not yet secured access. | Public disposal program, vendor listing, procurement pathway, direct conversation, or confirmed disposal stream. |
| Qualified | Relevant decision maker identified and source appears to generate target feedstock. | Named contact, known disposal role, likely material stream, and outreach path. |
| Potential | Likely feedstock generator based on industry, assets, or operations. | Industry logic, public information, or signal intelligence. |
| Speculative | The source may generate feedstock, but there is insufficient evidence. | Hypothesis only. Requires research before outreach. |

## Feedstock Source Categories

### 1. Existing Recycling Depots and Recycling Centres

Examples:

- Municipal recycling depots
- Regional recycling centres
- E-waste collection sites
- Electronics recycling programs
- Scrap yards
- IT asset disposition companies
- Reverse logistics operators

Current status:

- Category: Generally confirmed as feedstock aggregators
- Supplier status for MineTeck: Not confirmed until relationship and access are verified

Advantages:

- Existing material aggregation
- Recurring volume potential
- Easier to identify than hidden enterprise sources
- Possible partnership or offtake arrangements

Risks:

- Existing contracts
- Thin margins
- Material already priced efficiently
- Mixed low-grade material
- Contamination or sorting costs

Validation questions:

- Who owns the collected material?
- Is there an existing processor or offtake buyer?
- What feedstock types are collected?
- What volumes are available monthly?
- Are servers, PCBs, telecom boards, or enterprise electronics separated?
- Is material sold by weight, lot, auction, or contract?

### 2. Enterprise Manufacturers and OEMs

Examples:

- Samsung
- Dell
- HP
- Lenovo
- Cisco
- Other electronics manufacturers

Current status:

- Potential source category
- Not confirmed as MineTeck-accessible without validation

Possible feedstock streams:

- Warranty returns
- Refurbishment rejects
- Obsolete inventory
- Manufacturing scrap
- Returned enterprise hardware
- Defective boards

Risks:

- Existing global recycling contracts
- Internal recovery programs
- Strict compliance requirements
- Vendor onboarding requirements
- Low probability of direct access without strategic partnership

Validation questions:

- Does the company manage returns internally or through third-party processors?
- Who handles end-of-life inventory?
- Are there regional contractors?
- Is there a procurement or sustainability contact?
- Does the source require certified data destruction or environmental certification?

### 3. Government and Defence Sources

Examples:

- U.S. Department of Defense
- Canadian government surplus channels
- Provincial government surplus
- Municipal government surplus
- Defence contractors
- Aerospace contractors

Current status:

- Potential or verified category depending on disposal pathway
- Not confirmed as MineTeck source until access path is proven

Possible feedstock streams:

- Servers
- Communications equipment
- Networking hardware
- Specialized electronics
- Telecom boards
- Industrial or defence electronics

Risks:

- Security restrictions
- Data destruction requirements
- Export controls
- Procurement qualification
- Contractor approval requirements
- Chain-of-custody requirements
- Sensitive equipment handling

Validation questions:

- What surplus disposal channel is used?
- Are private buyers allowed?
- Is material sold through auction, approved vendors, or destruction contracts?
- Are certifications required?
- Can material be exported or processed cross-border?
- Is the material demilitarized or restricted?

### 4. Telecom and Network Infrastructure Sources

Examples:

- Telecom carriers
- Network operators
- ISP infrastructure operators
- Tower/network service providers
- Telecom equipment refurbishers

Current status:

- High-priority potential category
- Requires source-by-source validation

Possible feedstock streams:

- Telecom boards
- Switching equipment
- Routing equipment
- Power units
- Network cabinets
- Copper cabling
- Carrier-grade electronics

Advantages:

- Historically attractive board grades in some telecom equipment
- Network refresh cycles can create significant volume
- 4G/5G and core infrastructure upgrades may trigger disposal

Risks:

- Existing recovery contracts
- Security/data concerns
- Site logistics
- Equipment reuse/resale competition

### 5. Data Centres, MSPs, and ITAD Channels

Examples:

- Data centres
- Colocation providers
- Managed service providers
- IT asset disposition firms
- Cloud migration contractors

Current status:

- High-priority potential category
- Some may be verified after outreach or public disposal evidence

Possible feedstock streams:

- Rack servers
- Blade servers
- Storage arrays
- Networking equipment
- Server boards
- Copper cabling
- Power supplies

Risks:

- Resale value may exceed material recovery value
- Existing ITAD relationships
- Data destruction requirements
- Competitive bidding

## Source Validation Workflow

1. Identify source category.
2. Capture signal or reason for interest.
3. Assign initial status: Speculative or Potential.
4. Search for evidence of disposal pathway.
5. Identify decision maker or relationship owner.
6. Ask Gilbert Jones if the source is known, trusted, or historically relevant.
7. Upgrade to Qualified only when a contact path exists.
8. Upgrade to Verified only when the source confirms relevant material disposal.
9. Upgrade to Confirmed only after direct availability, transaction, or written confirmation.

## Minimum Required Fields

For each source, store:

```text
source_name
source_category
confidence_status
feedstock_types
estimated_volume
geography
relationship_owner
known_contact
validation_evidence
last_verified_date
access_path
risk_notes
next_action
```

## Investor Narrative Guidance

When communicating with investors, avoid overstating unconfirmed sources.

Use:

- Potential source category
- Verified disposal pathway
- Qualified source
- Confirmed source
- Recurring source

Avoid:

- Claiming Samsung, the U.S. Department of Defense, or any government/enterprise entity is a supplier unless verified.

Better phrasing:

> The system is designed to identify and validate feedstock opportunities across recycling depots, OEM return channels, telecom infrastructure, data centres, ITAD firms, and government surplus pathways. Sources are classified by confidence level before being included in the acquisition pipeline.

## Gilbert Jones Validation Questions

Ask Gilbert:

1. Which of these source categories have historically produced profitable feedstock?
2. Which specific sources has he worked with before?
3. Which source types produce high-margin feedstock versus reliable-volume feedstock?
4. Which sources should be avoided?
5. Which sources require certifications, permits, or special handling?
6. Which relationships already exist?
7. Which sources are likely to be easiest to access in the first 90 days?
8. Which sources are strategically valuable for the capital raise narrative?
