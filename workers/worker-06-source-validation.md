# Worker 06: Feedstock Source Validation Worker

## Purpose

The Feedstock Source Validation Worker classifies potential feedstock sources by evidence level before they enter the MineTeck / Breakthrough acquisition pipeline.

This worker prevents the system from treating potential sources such as OEMs, government agencies, recycling depots, telecom firms, or data centres as confirmed suppliers before validation.

## Operating Principle

A source is not confirmed until there is direct evidence of access to material.

The worker must distinguish between:

- A likely feedstock generator
- A verified disposer of relevant material
- A qualified opportunity with a contact path
- A confirmed supplier or available lot
- A recurring feedstock source

## Source Confidence Ladder

```text
Speculative
↓
Potential
↓
Qualified
↓
Verified
↓
Confirmed
↓
Recurring Source
```

## Status Definitions

### Speculative

The source may generate feedstock, but evidence is weak.

Example:

A large electronics company may generate obsolete inventory, but no disposal pathway has been identified.

### Potential

The source is likely to generate feedstock based on industry, operations, or public information.

Example:

A data centre operator likely refreshes servers, but no contact or disposal process is known.

### Qualified

A relevant decision maker, department, or access path has been identified.

Example:

A procurement manager, sustainability contact, IT asset manager, or surplus disposal office is identified.

### Verified

There is evidence that the source disposes of relevant material.

Example:

A public surplus listing, recycling contract, disposal program, or direct conversation confirms relevant electronic material is disposed.

### Confirmed

Material has been offered, acquired, contracted, or directly confirmed as available.

Example:

A seller confirms 10 tonnes of server equipment are available for evaluation.

### Recurring Source

The source has an ongoing or repeatable feedstock relationship.

Example:

A recycling depot or ITAD firm agrees to monthly or quarterly material flow.

## Inputs

The worker receives:

```text
source_name
source_category
location
feedstock_hypothesis
signal_source
known_contact
relationship_owner
supporting_evidence
notes
```

## Outputs

The worker returns:

```text
source_name
source_category
confidence_status
feedstock_types_likely
validation_evidence
relationship_owner
recommended_next_action
risk_flags
investor_safe_language
```

## Source Categories

### Recycling and Collection Networks

Includes:

- Municipal recycling depots
- E-waste collection centres
- Scrap yards
- ITAD companies
- Reverse logistics firms
- Electronics recyclers

Default status:

Potential, unless access or material flow is verified.

### OEM and Manufacturer Sources

Includes:

- Samsung
- Dell
- HP
- Lenovo
- Cisco
- Other electronics manufacturers

Default status:

Potential or speculative, unless there is proof of accessible returns, warranty rejects, obsolete inventory, or contractor pathway.

### Government and Defence Sources

Includes:

- U.S. Department of Defense
- Canadian government surplus
- Provincial surplus programs
- Municipal surplus programs
- Defence contractors

Default status:

Potential or verified depending on whether a disposal pathway is public and accessible.

Special caution:

Do not imply access to defence material without evidence, approvals, and compliance review.

### Telecom Sources

Includes:

- Telecom carriers
- Network operators
- ISP infrastructure firms
- Telecom refurbishers

Default status:

Potential until decision maker, refresh cycle, or disposal pathway is identified.

### Data Centre and ITAD Sources

Includes:

- Data centres
- Colocation facilities
- Managed service providers
- IT asset disposition firms
- Cloud migration contractors

Default status:

Potential until equipment refresh, decommissioning, or disposal process is verified.

## Required Validation Questions

For every source, answer:

1. What feedstock might this source generate?
2. What evidence supports that assumption?
3. Who controls the material?
4. Is the material already under contract?
5. Is there a relationship owner?
6. What compliance issues may apply?
7. What is the next action required to move this source up the confidence ladder?

## Investor Safe Language

The worker should produce safe wording for investor materials.

### Unsafe

> Samsung and the U.S. Department of Defense are feedstock suppliers.

### Safer

> The system is designed to evaluate potential feedstock channels including OEM return streams, recycling depots, ITAD firms, telecom infrastructure, data centres, and government surplus pathways. Each source is classified by validation status before being included in the acquisition pipeline.

### Stronger if Verified

> MineTeck has identified verified disposal pathways in recycling and ITAD channels and is working to qualify additional sources across enterprise, telecom, and government surplus categories.

## Human Review Rules

Human review is required before:

- Marking a source as confirmed
- Naming a source in investor materials as a supplier
- Sending outreach to sensitive government or defence sources
- Representing expected volume from an unverified source
- Creating financial projections from speculative sources

Reviewers:

- Dennis Eng
- Gilbert Jones
- Authorized MineTeck / Breakthrough operator

## Recommended First 90-Day Target

The worker should prioritize moving sources from Potential to Qualified and Verified.

Initial goal:

```text
50 potential sources
20 qualified sources
10 verified sources
3 confirmed acquisition conversations
1 recurring feedstock relationship
```
