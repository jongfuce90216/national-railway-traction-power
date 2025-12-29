# Root Cause Analysis for Recurring Fault BTV-07

**Date:** 2025-12-28  
**Analyst:** Engineering Team  
**Status:** Closed

## Summary
Multiple undervoltage faults (BTV‑07) have been reported across booster transformer units on Line 3. Investigation reveals a strong correlation with peak traffic hours and a specific voltage regulator model.

## Affected Units
- Booster transformer units #12, #18, #24, #31 (Line 3)
- All units equipped with voltage regulator **VR‑4500** (serial range 4500‑xxxx)

## Incident Timeline
| Date       | Time       | Unit | Notes |
|------------|------------|------|-------|
| 2025‑11‑10 | 08:15      | #12  | First recorded BTV‑07 |
| 2025‑11‑12 | 17:45      | #18  | During evening peak |
| 2025‑11‑15 | 08:30      | #24  | Concurrent with high train density |
| 2025‑11‑20 | 17:20      | #31  | Similar pattern |

## Root Cause
1. **Peak Traffic Load**  
   Faults occur exclusively during morning (07:00–09:00) and evening (17:00–19:00) peaks, when train current demand exceeds the regulator’s ability to maintain output voltage within tolerance.

2. **Regulator Model Limitation**  
   The VR‑4500 regulator uses a **fixed‑gain droop compensation** that cannot respond quickly enough to sudden load changes. Under high‑rate current transients, the output sags beyond the undervoltage threshold (‑12 % of nominal).

3. **Thermal Derating**  
   Prolonged operation at high ambient temperature (common in tunnel sections) reduces the regulator’s effective current capability, exacerbating the voltage drop.

## Supporting Evidence
- Log analysis shows undervoltage events coincide with train schedules.
- Laboratory tests on a VR‑4500 sample confirm sluggish response to step loads > 150 A.
- Field measurements indicate voltage dips of 10–15 % during peak hours, while adjacent lines with newer VR‑4800 regulators show no dips.

## Recommendations
1. **Immediate Action**  
   - Replace VR‑4500 regulators in high‑traffic corridors with VR‑4800 (or equivalent) during the next planned outage.
   - Adjust regulator setpoints temporarily to provide a wider voltage window (‑10 % to +10 %) until hardware upgrade.

2. **Long‑Term Measures**  
   - Upgrade all VR‑4500 units across the network within 12 months.
   - Install additional voltage monitoring points for predictive analytics.
   - Revise maintenance schedule to include regulator firmware updates.

## Linked Issues
- #1 (Undervoltage fault BTV-07 on booster transformer unit #12)
- #2 (Undervoltage fault BTV-07 on booster transformer unit #18)
- #3 (Undervoltage fault BTV-07 on booster transformer unit #24)
- #4 (Undervoltage fault BTV-07 on booster transformer unit #31)

---

*This document is maintained in the project repository under `docs/analysis/root-cause-btv-07.md`.*