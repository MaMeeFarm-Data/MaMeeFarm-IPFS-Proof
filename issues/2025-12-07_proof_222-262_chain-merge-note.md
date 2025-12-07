# DGCP™ Issue Log — Google Sheet Timestamp Error  
### Date: 2025-12-07  
### Related Proof Range: 222–262  
### Status: Chain preserved (no missing OTS)

---

## 1. Overview  
During daily DGCP™ operations on **2025-12-07**, the Google Sheet used for timestamp parsing encountered repeated formula and filter errors.  
The issue was caused by Google Sheets blocking the filter range (“partially intersects a table”) and preventing the formula from resolving timestamps for the Proof range 260–262.

Even though the sheet malfunctioned, all proofs were already safely **OpenTimestamped**, so **the chain remains unbroken**.

---

## 2. Issue Details

### **2.1 Formula Breakdown**
The formula:
=IF(A262="", "", DATEVALUE(LEFT(A262, FIND(" ", A262)-1)) + TIMEVALUE(MID(A262, FIND(" ", A262)+1, 8)))

returned:
#VALUE! Error: Function FIND parameter 2 value should be non-empty.

**Cause:**  
Some timestamp cells became invisible or empty after Google Sheet automatically collapsed rows when filter view was applied.

---

### **2.2 Filter System Error**
Repeated pop-up message:
There was a problem. You can’t apply a filter to a range that partially intersects a table.

**Cause:**  
Google Sheets detected the table created by Form Responses and prevented a second filter layer.

This caused temporary “file disappearing” behaviour when scrolling.

---

## 3. Recovery Actions (Completed)

- ❌ Removed the damaged rows (260–262)  
- ✔ Re-entered all timestamps manually  
- ✔ Re-applied the global formula  
- ✔ Verified each timestamp line  
- ✔ Confirmed all data matches Proof 222–262  
- ✔ Prepared combined OpenTimestamp PDF for 6–7 December

---

## 4. Chain Integrity Status

| Item | Status |
|------|--------|
| Proof 222–240 (Dec 6) | ✔ Already timestamped |
| Proof 241–262 (Dec 7) | ✔ Successfully timestamped |
| Chain Gap | ❌ None |
| Data Loss | ❌ None |
| Manual Correction Required | ✔ Completed |

The DGCP™ chain for **Dec 6–7, 2025** is fully intact.

---

## 5. Files Generated (for archival)

### **MMFARM_DGCP_DAILY_2025-12-06_Proof222-240.pdf**
- Daily Proof PDF  
- Timestamped: ✔  
- Receipt: ✔  

### **MMFARM_DGCP_DAILY_2025-12-07_Proof241-262.pdf**
- Daily Proof PDF  
- Timestamped: ✔  
- Receipt: ✔  

### Combined Summary  
Both days now form a continuous DGCP™ block with no timestamp gaps.

---

## 6. Notes for Future Prevention

- Avoid using extra filter views in Form Responses tab.  
- If formula cells break again → duplicate sheet before repairing.  
- DGCP chain cannot break as long as OTS files are completed daily.

---

### **MMFARM-POL-2025 License Applies**  
This document is part of the DGCP™ governance record.
