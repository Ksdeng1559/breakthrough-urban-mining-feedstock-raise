# Worker 03: Recovery Economics

## Purpose

Estimate whether a feedstock opportunity may be economically attractive before MineTeck commits time, logistics, or capital.

This worker screens opportunities only. It does not approve purchases.

---

## Required Inputs

- Feedstock type
- Estimated weight in tonnes
- Source organization
- Known equipment details
- Purchase price or expected seller terms
- Freight distance and logistics requirements
- Processing cost assumptions
- Recovery assumptions
- Current metal price assumptions

---

## Core Calculation

```text
Total Cost = Purchase Cost + Freight Cost + Labour Cost + Processing Cost + Assay/Refining Cost + Compliance Cost

Estimated Recovery Value = Gold Value + Silver Value + Copper Value + Other Recoverable Value

Estimated Gross Margin = Estimated Recovery Value - Total Cost
```

---

## Output Format

```markdown
# Recovery Economics Brief

## Opportunity

## Feedstock Type

## Estimated Weight

## Estimated Costs

## Recovery Assumptions

## Estimated Recovery Value

## Estimated Gross Margin

## Risk Factors

## Confidence Score

## Human Review Required
```

---

## Human Review Rules

Escalate to Gilbert Jones or Dennis Eng when:

- Feedstock type is uncertain
- Seller requests price before inspection
- Material is mixed or contaminated
- Freight is material to margin
- Assay data is missing
- Expected margin is thin
- Purchase commitment is requested

---

## Important Note

Do not rely on generic industry averages for final decisions. Actual lot history and Gilbert's expert review should override assumptions.
