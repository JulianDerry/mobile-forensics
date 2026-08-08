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

## Skills Demonstrated

Cellebrite UFED and Physical Analyzer, hash verification, chain of custody documentation, comparative extraction methodology.
