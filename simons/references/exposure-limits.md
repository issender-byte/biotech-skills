# Exposure Limits Reference

Framework for managing portfolio exposure and preventing excessive concentration.

---

## Overview

Exposure limits define the boundaries for portfolio construction. They ensure diversification and prevent excessive concentration.

---

## Gross and Net Exposure

### Definitions

| Metric | Calculation | Typical Range |
|--------|-------------|---------------|
| **Gross Exposure** | \|Longs\| + \|Shorts\| | 150-250% |
| **Net Exposure** | Longs - Shorts | 20-80% net long |
| **Beta-Adjusted Net** | Σ(Position × Beta) | Varies |

### Why They Matter

**Gross exposure:**
- Measures total risk capital deployed
- Higher gross = more volatility
- Limits leverage effects

**Net exposure:**
- Measures directional market exposure
- Positive = bullish on sector
- Negative = bearish on sector

---

## Position Limits

### Single Position Limits

| Position Type | Max Size | Rationale |
|---------------|----------|-----------|
| High conviction | 200-300 bps | Concentrated bet, high edge |
| Standard | 100-150 bps | Normal position |
| Starter/Speculative | 25-75 bps | Building position or high risk |
| Binary catalyst | 100-150 bps | Event-driven, manage loss |

### Concentration Triggers

| Trigger | Action |
|---------|--------|
| Single position >3% NAV | Review and document |
| Single position >5% NAV | Reduce or committee approval |
| Top 5 positions >50% gross | Diversify |
| Top 10 positions >70% gross | Add positions or reduce |

---

## Therapeutic Area Limits

### TA Concentration

| Limit | Threshold | Rationale |
|-------|-----------|-----------|
| Single TA | <30% of gross | TA-specific news risk |
| Top 2 TAs | <50% of gross | Diversification |

### TA Categories

Common TA groupings:
- **Oncology** (solid tumor, heme malignancies)
- **Immunology/Inflammation** (I&I, autoimmune)
- **CNS** (neurology, psychiatry)
- **Cardiovascular/Metabolic** (CV, diabetes)
- **Rare disease** (genetic, ultra-orphan)
- **Infectious disease** (virology, antibiotics)
- **Ophthalmology**

---

## Phase/Stage Limits

### Development Phase

| Phase | Risk Profile | Suggested Max |
|-------|--------------|---------------|
| Preclinical | Very high (binary, no human data) | 10-15% of gross |
| Phase 1 | High (early human data) | 15-20% |
| Phase 2 | High (efficacy signal needed) | 25-30% |
| Phase 3 | Medium (pivotal, but binary) | 30-40% |
| Commercial | Lower (execution risk) | 40-50% |

### Binary Event Limits

| Limit | Threshold | Rationale |
|-------|-----------|-----------|
| Binary events per week | 3-5 max | Manage portfolio volatility |
| Single binary event | <150 bps | Cap event-driven loss |
| Correlated binaries | Count as 1 event | Same outcome risk |

---

## Top Position Limits

| Limit | Typical Threshold | Rationale |
|-------|-------------------|-----------|
| Top 5 positions | <50% of gross | Diversification |
| Top 10 positions | <70% of gross | Concentration check |

---

## Dynamic Exposure Management

### When to Reduce Gross

| Condition | Action |
|-----------|--------|
| Market volatility spike | Reduce 10-20% |
| Multiple binary catalysts | Reduce ahead |
| Liquidity deteriorating | Reduce illiquid first |
| Correlation spike | Reduce gross, maintain net |

### When to Increase Gross

| Condition | Action |
|-----------|--------|
| High conviction opportunities | Add within limits |
| Volatility normalizing | Rebuild positions |
| Liquidity improving | Extend into smaller caps |

---

## Limit Breach Protocol

### Soft Breach (Within 5% of Limit)

- Monitor daily
- No new positions that increase breach
- Plan to reduce within 1 week

### Hard Breach (Exceeds Limit)

- Immediate notification
- Plan to reduce within 48 hours
- Document reason and resolution

---

## Exposure Checklist

**Daily review:**
- [ ] Gross exposure within limit
- [ ] Net exposure within range
- [ ] No single position > max
- [ ] No single TA > 30% gross
- [ ] Top 5 positions < 50% gross
- [ ] Binary catalyst count < 5

**Weekly review:**
- [ ] Phase concentration appropriate
- [ ] Correlation clustering acceptable
- [ ] Liquidity profile adequate
