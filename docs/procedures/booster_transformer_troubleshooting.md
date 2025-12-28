# Booster Transformer Troubleshooting Guide

This document provides procedures for diagnosing and resolving faults in booster transformer units.

## Common Fault Codes

### Fault Code BTV-01
Description: Overcurrent protection triggered.

### Fault Code BTV-02
Description: Temperature sensor failure.

### Handling Fault Code BTV-07
**Description:** Undervoltage fault detected on booster transformer secondary side.

**Root Cause Analysis:**
- Fault consistently occurs during peak traffic hours (07:00–09:00 and 17:00–19:00).
- Affected units utilize voltage regulator model **VR-4500** (serial range 4500-xxxx).
- High load demand leads to insufficient regulator response, causing voltage sag beyond tolerance.

**Diagnostic Checklist:**

1. **Check Time of Occurrence**
   - Confirm fault timestamp matches peak traffic window.
   - Review historical logs for similar patterns.

2. **Identify Voltage Regulator Model**
   - Locate unit identification plate.
   - Verify regulator model is VR-4500 (or compatible series).

3. **Measure Input/Output Voltages**
   - Use calibrated multimeter on primary (input) terminals.
   - Measure secondary (output) terminals under load.
   - Record voltage values before, during, and after fault.

4. **Assess Load Conditions**
   - Determine train traffic density at time of fault.
   - Check adjacent booster units for similar undervoltage events.

5. **Inspect Regulator Settings**
   - Access regulator configuration menu (refer to VR-4500 manual).
   - Verify setpoint and droop settings are within specification.
   - Adjust if necessary (consult engineering).

6. **Perform Thermal Inspection**
   - Use infrared camera to detect overheating in regulator components.
   - Ensure cooling fins are clean and ventilation unobstructed.

7. **Review Maintenance History**
   - Check previous service entries for regulator firmware updates.
   - Look for past replacements or adjustments.

8. **Temporary Mitigation**
   - If fault recurs, consider reducing load on affected section during peak hours.
   - Schedule regulator replacement with upgraded model VR-4800.

**Preventive Measures:**
- Replace VR-4500 regulators in high‑traffic corridors during next maintenance cycle.
- Install additional voltage monitoring points for early detection.
- Update firmware to latest version (VR‑4500‑v2.1 or later).

## General Diagnostic Steps

1. Check input voltage.
2. Verify output voltage.
3. Inspect wiring connections.
4. Review maintenance logs.

---