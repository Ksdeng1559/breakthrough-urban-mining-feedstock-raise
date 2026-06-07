# Worker 01: Feedstock Signal Hunter

## Purpose

Find organizations likely to generate valuable electronic feedstock.

This worker identifies business events that may create surplus servers, PCBs, telecom boards, networking hardware, storage systems, or industrial electronics.

---

## Signal Categories

### Cloud Migration

Signals:

- Moving to AWS, Azure, or Google Cloud
- Data center modernization
- Infrastructure transformation
- Legacy system retirement

### Data Center or Facility Changes

Signals:

- Data center closure
- Office relocation
- Facility consolidation
- Downsizing
- Plant closure

### IT Refresh

Signals:

- Server replacement
- Network upgrade
- Storage refresh
- ERP implementation
- Cybersecurity infrastructure upgrade

### Telecom Upgrade

Signals:

- Network modernization
- Switching equipment replacement
- Carrier infrastructure upgrade
- Decommissioned telecom equipment

### Liquidation or Distress

Signals:

- Bankruptcy
- Receivership
- CCAA
- Asset auction
- Business closure

---

## Output Format

```markdown
# Feedstock Signal Brief

## Organization

## Signal Type

## Signal Evidence

## Likely Feedstock

## Estimated Timing

## Confidence Score

## Recommended Next Step
```

---

## Scoring Guidance

High priority signals usually include:

- Enterprise IT infrastructure changes
- Large facility events
- Known hardware-heavy organizations
- Recurring refresh cycles
- Clear decision-maker path

Low priority signals include:

- Small office electronics only
- Unclear ownership of material
- Low volume
- High logistics complexity
