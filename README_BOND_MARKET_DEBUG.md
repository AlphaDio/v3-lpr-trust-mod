# Bond Market LPR - Debug Features

## Debug Journal Entry

The mod includes a debug journal entry called "The Bond Market" that provides real-time information about your country's bond market status.

### How to Access

1. **For Players:** The journal entry is automatically available in the Economy section of the Journal (added at game start)
2. **For Developers:** Available in debug mode or for player countries

### Information Displayed

The journal entry shows:
- **Trust:** Current bond trust value (0-100)
- **Tier:** Trust tier (Very Low, Low, Medium, High, Very High)
- **Debt:** Current scaled debt as a percentage
- **Income:** Net fixed income (positive = surplus, negative = deficit)

### Example Display
```
Trust: 65 | Tier: High | Debt: 45% | Income: +2500
```

## Debug Decisions

In debug mode, you can access additional decisions in the Politics -> Decisions menu:

- **"Bond Market: Show Trust"** - Displays a popup with detailed trust information
- **"Bond Market: Add Bond Market Journal Entry"** - Adds the journal entry for ongoing monitoring
- **"Bond Market: Set Trust to 10/60/95"** - Manually sets trust to specific values for testing

## Trust System Mechanics

### Monthly Updates
Every month, trust changes based on:
- **Default:** -20 trust penalty
- **High Debt (≥90%):** -5 trust penalty
- **Medium Debt (≥70%):** -3 trust penalty
- **Low Debt (≥50%):** -1 trust penalty
- **Low Debt + Surplus (≤20% debt + non-deficit):** +2 trust bonus
- **Drift toward 60:** ±1 trust toward neutral level

### Trust Tiers & Effects
- **0-19 (Very Low):** +5% interest rate, -30% building cash reserves
- **20-39 (Low):** +3% interest rate, -15% building cash reserves
- **40-59 (Medium):** +1% interest rate, neutral cash reserves
- **60-79 (High):** -1% interest rate, +10% building cash reserves
- **80-100 (Very High):** -3% interest rate, +20% building cash reserves

### Define Changes
- Doubled base credit limit (200,000 vs 100,000 default)
- Doubled GDP-based credit multiplier (1.0 vs 0.5 default)

This makes the bond market system more prominent and dynamic in gameplay.
