# Mobile Device Forensic Examination: Advanced Logical vs File System Extraction Comparison

**Case:** DFIR-MF-2026 (AMF-001) | **Device:** Samsung SM-A032F | **Tools:** Cellebrite UFED, Physical Analyzer

## Summary

This case examines a Samsung SM-A032F using two acquisition methods, Advanced Logical and File System, to compare data yield on a device with a current security patch level. File System extraction returned significantly less data due to privilege escalation restrictions, while Advanced Logical, using vendor built routines that bypass that requirement, recovered a broader dataset.

## Key Result

| Category | Advanced Logical | File System |
|---|---|---|
| Structured Data (calls, SMS, contacts, calendar) | Identical | Identical |
| Images | 190 | 178 |
| Text Files | 85 | 1 |
| Archives | 13 | 1 |

---

## 6. Conclusion

Both Advanced Logical and File System extractions were performed on the device to preserve and analyze accessible data and to evaluate the consistency of results across acquisition methods. Communications records, user data, media artifacts, location artifacts, and potentially recoverable deleted data were examined within the scope of these acquisitions.

Device Data (calls, SMS, contacts, calendar, device info) was consistent across both methods. Device Data Files diverged, with Advanced Logical recovering a broader dataset than File System due to the device's security patch level restricting the privilege escalation required for a full File System pull (see Sections 4.4 and 5.6).

The examination was conducted using Cellebrite UFED version 7.71.0.1858 and Cellebrite Physical Analyzer version 8.1.0.12. The findings and limitations documented in this report are specific to the data accessible from the device at the time of examination and to the capabilities and limitations of that software version and the acquisition methods used. No conclusions have been drawn beyond the evidence available in the extracted datasets.

---
## Skills Demonstrated

Cellebrite UFED and Physical Analyzer, hash verification, chain of custody documentation, comparative extraction methodology.
