
# Mobile Device Forensic Examination Report

## Table of Contents

1. [Administrative & Case Details](#1-administrative--case-details)
   - 1.1 Case Information
   - 1.2 Examiner Information
   - 1.3 Scope of Examination
   - 1.4 Examination Objectives
2. [Evidence & Chain of Custody](#2-evidence--chain-of-custody)
   - 2.1 Evidence Description
   - 2.2 Device Identifiers
   - 2.3 SIM Card Details
   - 2.4 Chain of Custody Log
3. [Intake State & Preservation](#3-intake-state--preservation)
   - 3.1 Device Condition on Receipt
   - 3.2 Isolation and Preservation Measures
   - 3.3 Photographic Documentation
4. [Extraction & Acquisition Methodology](#4-extraction--acquisition-methodology)
   - 4.1 Acquisition Type
   - 4.2 Hardware and Software Tools
   - 4.3 Integrity Verification
   - 4.4 Extraction Notes and Anomalies
5. [Technical Findings & Analysis](#5-technical-findings--analysis)
   - 5.1 Communications
   - 5.2 User Data
   - 5.3 Media and Metadata
   - 5.4 Location Artifacts
   - 5.5 Data Recovery
   - 5.6 Cross-Method Comparison
6. [Conclusion](#6-conclusion)
7. [Appendices](#7-appendices)

---

## 1. Administrative & Case Details

### 1.1 Case Information

| Item | Value |
|---|---|
| Case Identifier | DFIR-MF-2026 |
| Requesting Agency / Client | Personal Laboratory Examination |
| Report Date | August 06, 2026 |
| Examination Date(s) | August 05 to 06, 2026 |
| Case Reference | AMF-001 |

### 1.2 Examiner Information

| Item | Value |
|---|---|
| Examiner Name | Julian Derry |
| Title / Position | Digital Forensics Analyst |
| Organization | Independent / Personal Laboratory |
| Signature / Authorization | JD |
| Date Signed | August 06, 2026 |

### 1.3 Scope of Examination

This examination involved the forensic acquisition and analysis of a Samsung SM-A032F mobile device submitted for laboratory examination. Two acquisition methods, Advanced Logical and File System, were deliberately performed on the same device to evaluate and compare their respective data yields under the device's current security patch level. The examination was conducted using accepted digital forensic procedures intended to preserve data integrity and maintain evidential continuity within the limits of a personal laboratory environment.

### 1.4 Examination Objectives

- Evaluate and compare the data yield of Advanced Logical and File System extraction methods on a device with an updated security patch level. This evaluation was conducted on a device running Android 13 (Security Patch Level: 1 December 2025, Base Version: A032FXXS9CZA1) to assess how extraction method choice affects artifact recovery under current security conditions.
- Identify and preserve data stored on the device.
- Acquire forensic copies of accessible data.
- This evaluation focused on extraction method comparison at the data yield and artifact-count level, detailed analysis of individual artifact categories (communications, user activity, media, location, deleted data) was outside the scope of this exercise.
- Produce a documented forensic report suitable for technical review and evidential reference.

---

## 2. Evidence & Chain of Custody

### 2.1 Evidence Description

| Item | Value |
|---|---|
| Evidence Item No. | AMF-001 |
| Device Type | Mobile Phone |
| Manufacturer | Samsung |
| Model | SM-A032F A03 Core |
| Android Version | 13 |
| Security Patch Level | 1 December 2025 |
| Based Version | A032FXXS9CZA1 |
| Color | Black |
| Physical Condition | Several cracks on phone screen |

### 2.2 Device Identifiers

| Item | Value |
|---|---|
| IMEI | 35138xxxxxx5619 |
| IMEI 2 | 35322xxxxxx5618 |
| MEID | 3513xxxxxx7561 |
| ESN | Not present |
| Serial Number | R7xxxxxxR6A |

**Examiner Note:** On this device, the IMEI and MEID appear together because the handset uses a hybrid identifier format in which the MEID is represented by the first 14 digits and the IMEI is represented by the full 15-digit value. ESN (Electronic Serial Number) is an older identifier format that has largely been replaced by MEID on modern devices.

### 2.3 SIM Card Details

| Item | Value |
|---|---|
| SIM Slot | SIM 1 & SIM 2 |
| ICCID (SIM 1)| Not obtained |
| ICCID (SIM 2)| 8923 3020 5072 04XXXX |
| IMSI | 6200xxxxxx58050 \| 6200xxxxxx48328 |
| Carrier | MTN \| TELECEL |

### 2.4 Chain of Custody Log

| Date & Time | Action | From | To | Location | Signature |
|---|---|---|---|---|---|
| August 05, 2026 6:20 PM | Device photographed and documented | Julian Derry | Julian Derry, Digital Forensics Analyst | Accra, Ghana | JD |
| August 05, 2026 6:24 PM | Forensic extraction initiated | Julian Derry | Julian Derry, Digital Forensics Analyst | Accra, Ghana | JD |
| August 05, 2026 6:27 PM | Forensic extraction completed | Julian Derry | Julian Derry, Digital Forensics Analyst | Accra, Ghana | JD |
| August 05, 2026 6:30 PM | Device retained by examiner following examination | Julian Derry | Julian Derry, Digital Forensics Analyst | Accra, Ghana | JD |

**Examiner Note:** This examination was conducted on a personally owned device within a controlled home laboratory environment. As a result, some chain of custody events commonly recorded in formal law enforcement or corporate evidence handling procedures, such as seizure by an external party, evidence bag sealing, transport to evidence storage, and transfer to an investigating officer, did not occur and are therefore not recorded in this log.

---

## 3. Intake State & Preservation

### 3.1 Device Condition on Receipt

| Item | Value |
|---|---|
| Power State | On |
| Screen State | Unlocked |
| Battery Level | 62% |
| SIM Present | Yes |
| External Damage | Multiple cracks on screen; scratches on body; small chip below power button |

### 3.2 Isolation and Preservation Measures

- Device isolated from cellular networks.
- Wi-Fi and Bluetooth communications prevented.
- Airplane mode enabled.
- Device handled using forensic best practices to avoid data alteration.

### 3.3 Photographic Documentation

- Front view
- Rear view
- Left and right sides
- Top and bottom edges
- Screen display upon receipt
- Any visible damage

**Figures**
- Figure 1: Front View
- Figure 2: Rear View
- Figure 3: Screen State on Receipt
- Figure 4: External Damage

---

## 4. Extraction & Acquisition Methodology

### 4.1 Acquisition Type

| Acquisition Method | Performed |
|---|---|
| Logical Extraction | Yes (Advanced Logical) |
| File System Extraction | Yes |
| Physical Extraction | No |

### 4.2 Hardware and Software Tools

| Tool | Version | Purpose |
|---|---|---|
| Cellebrite UFED | 7.71.0.1858 | Data extraction |
| Cellebrite Physical Analyzer | 8.1.0.12 | Analysis of the UFED extraction file (.ufdx) |

**Examiner Note:** The extraction package generated by Cellebrite UFED in .ufdx format was subsequently analyzed using Cellebrite Physical Analyzer, which supports examination of UFED extraction containers and associated artifact datasets.

### 4.3 Integrity Verification

| Extraction File | Algorithm | Hash Value |
|---|---|---|
| Samsung GSM_SM-A032F A03 Core_AdvancedLogical | SHA-256 | 40105FD6E7F857379339B0C97D2E5355DB3A60BFEBC566CCD3C9EF17DB9E399F |
| Samsung GSM_SM-A032F A03 Core_FileSystem | SHA-256 | E4F6DBBC38629865E969A9EB568DB0C3F4C9056E9469F2DAD05620E1353D4B60 |

Hash values were calculated immediately after acquisition and verified prior to analysis.

### 4.4 Extraction Notes and Anomalies

| Observation | Details |
|---|---|
| Connection Errors | None |
| Extraction Warnings | A backup option popup appeared during acquisition |
| Unsupported Artifacts | Instant messaging application data not acquired |
| Encryption Status | Encrypted |
| Acquisition Limitations | Device's security patch level limited privilege escalation during File System acquisition, resulting in a reduced dataset relative to Advanced Logical |

**Examiner Note (Advanced Logical review):** The Advanced Logical case was initially reviewed using the .ufdx file alone, which returned no media or file artifacts. A subsequent review incorporating the associated extraction archive (.zip) revealed the complete Device Data Files. 

**Examiner Note (File System limitation):** File system extraction was performed but limited by the device's security patch level, which restricted privilege escalation, resulting in a reduced dataset compared to the Advanced Logical extraction. File system extraction generally needs elevated privileges to reach protected storage, whereas Advanced Logical uses vendor built routines that pull from structured app containers and database paths without needing that escalation, so it was not blocked in the same way.

The observations and limitations documented in this section apply specifically to the version of Cellebrite UFED used during this examination and should not be generalized to all versions of the software.

---

## 5. Technical Findings & Analysis

### 5.1 Communications

**Call Logs**

A total of 111 call records were acquired. The table below contains a representative sample of four records for reporting purposes.

| Date/Time | Direction | Number / Contact | Duration |
|---|---|---|---|
| 8/5/2026 1:12:00 PM (UTC+0) | Outgoing | 116 | 00:05:36 |
| 8/2/2026 12:54:21 PM (UTC+0) | Outgoing | 027xxxxxxx | |
| 7/23/2026 11:31:12 AM (UTC+0) | Answered | 020xxxxxxx | 00:00:41 |
| 7/8/2026 9:48:46 AM (UTC+0) | Missed | 059xxxxxxx | |

**SMS / MMS**

A total of 374 SMS/MMS records were acquired. The table below contains a representative sample of three records for reporting purposes.

| Date/Time | Sender | Recipient | Summary |
|---|---|---|---|
| 8/5/2026 5:11:42 PM (UTC+0) | Telecel | 05068xxxxx | Did you know, you can save more on every call... |
| 8/5/2026 2:28:55 PM (UTC+0) | MTNFBB | 05068xxxxx | Your request for broadband bundle purchase through MTN Mobile Money failed. |
| 8/5/2026 9:32:03 AM (UTC+0) | 505 | 05068xxxxx | Super news! More options for you! |

**Examiner Note, Dual-SIM Correlation:** The device was provisioned with two active SIM profiles (IMSI 6200xxxxxx58050 on MTN and IMSI 6200xxxxxx48328 on TELECEL). Both carriers are represented in the acquired SMS dataset, MTN-originated messages (sender "MTNFBB") and TELECEL-originated messages (sender "Telecel") both appear among the extracted records, indicating that both SIM slots were actively in use rather than one being idle or a backup line. This is consistent with normal dual-SIM personal use rather than a single primary line with a secondary/unused SIM.

### 5.2 User Data

**Contacts**

A total of 1 contact record was acquired.

| Name | Number | Email |
|---|---|---|
| Jude | 02461xxxxx | |

**Examiner Note:** The extraction contained only one contact record. During examination, it was confirmed that only one contact was intentionally stored in the device's internal contact storage. The extraction may have been permitted to access device contact data while SIM card contact storage was not accessible, or SIM-resident contacts were not included in the extracted dataset.

**Calendar Entries**

A total of 1 calendar event was acquired.

| Date | Event | Notes |
|---|---|---|
| 1/1/1970 | Jude's birthday | |

**Examiner Confirmation:** The examiner confirmed that only one calendar event had been manually added to the device prior to acquisition.

Additional user artifacts such as notes, reminders, and emails were reviewed where accessible.

### 5.3 Media and Metadata

**Media Summary**

| Media Type | Advanced Logical | File System |
|---|---|---|
| Images | 190 | 178 |
| Audio Files | 2 | 2 |
| Videos | 3 | 0 |
| Documents | 1 | 0 |
| Archives | 13 | 1 |
| Text Files | 85 | 1 |
| Uncategorized | 5 | 13 |

**Findings**

Media artifacts were recovered from both extractions, with the Advanced Logical extraction yielding a broader file set across nearly every category. A sample verification was performed: one video file from the Advanced Logical extraction and one audio file from the File System extraction were opened and confirmed to play successfully, indicating the recovered media is intact and not corrupted. A full content review of all recovered files, along with EXIF, geolocation, or timestamp metadata analysis, was not performed and was outside the scope of this examination.

**Interpretation**

Both extractions recovered media artifacts from the device, with Advanced Logical yielding a substantially broader file set than File System across nearly every category. The methodological reasons for this divergence, tied to the device's security patch level restricting privilege escalation during File System acquisition, are discussed in Section 5.6.

### 5.4 Location Artifacts

| Artifact Type | Details |
|---|---|
| GPS Records | 0 |
| Wi-Fi Networks | 0 |
| Cell Tower Associations | 0 |
| Significant Locations | 0 |

**Examiner Note:** No location artifacts were recovered from either the Advanced Logical or File System extraction. Location artifacts are typically stored in system and app-level databases that neither acquisition method reliably captured on this device, consistent with the privilege-escalation limitation discussed in Section 4.4.

### 5.5 Data Recovery

Deleted records were examined using forensic recovery techniques, including database review and artifact analysis where applicable.

| Artifact Type | Records Recovered | Recovery Method |
|---|---|---|
| SMS | 374 | Present in extraction, not identified as deleted |
| Contacts | 1 | Active device record |
| Photos | 190 (Advanced Logical) / 178 (File System) | Active device records, not identified as deleted |
| Chat Messages | 0 | No recoverable deleted artifacts identified |

**Examiner Note:** Both extractions recovered active photo files (190 via Advanced Logical, 178 via File System), but neither dataset flagged any of these, or any other artifact type, with a deletion status indicator. The photo counts represent active, currently-stored files, not recovered deleted media. As with SMS, no artifacts were conclusively identified as deleted records by the forensic tool during this examination.

The absence of recovered deleted artifacts in this examination should not be interpreted as confirmation that no deleted data exists on the device. Neither Advanced Logical nor the limited File System extraction parses unallocated space, where deleted records typically reside after removal from active databases. Recovering deleted SMS, media, or database records generally requires a full File System or Physical extraction with unrestricted privilege escalation, which this device's security patch level did not permit (see Section 4.4). Accordingly, the findings in this section reflect the limitations of the acquisition methods, not a confirmed absence of deleted data.

### 5.6 Cross-Method Comparison

Both Advanced Logical and File System extractions were performed on this device to evaluate whether the two methods produced consistent results, and to document the effect of the device's security patch level on extraction outcomes.

Device Data (Calendar, Call Log, Contacts, Device Info, Instant Messages) was identical across both extractions: 111 call records, 374 SMS/MMS records, 1 contact, 1 calendar entry, and 16 device info fields in each. This consistency indicates both methods reliably captured OS-level structured data regardless of acquisition type.

Device Data Files diverged significantly, as shown in Section 5.3. Advanced Logical recovered a substantially larger and more categorized file set (190 images, 85 text files, 13 archives, 3 videos, 1 document) compared to File System (178 images, 1 text file, 1 archive, 0 videos, 0 documents), with a higher Uncategorized count of 13 versus 5.

This divergence is attributed to the device's security patch level restricting the privilege escalation that File System extraction requires to reach protected app-specific storage. Advanced Logical extraction avoided this limitation by using vendor built routines that query structured application containers and database paths directly, without needing elevated OS privileges. The higher Uncategorized count in the File System result is also consistent with a privilege-limited pull: files were present but not fully parsed or categorized by the tool.

This result demonstrates that extraction method selection, and awareness of device patch level, has a direct and measurable effect on data yield, and that relying on a single extraction method may understate the data actually present on a device.

---

## 6. Conclusion

Both Advanced Logical and File System extractions were performed on the device to preserve and analyze accessible data and to evaluate the consistency of results across acquisition methods. Communications records, user data, media artifacts, location artifacts, and potentially recoverable deleted data were examined within the scope of these acquisitions.

Device Data (calls, SMS, contacts, calendar, device info) was consistent across both methods. Device Data Files diverged, with Advanced Logical recovering a broader dataset than File System due to the device's security patch level restricting the privilege escalation required for a full File System pull (see Sections 4.4 and 5.6).

The examination was conducted using Cellebrite UFED version 7.71.0.1858 and Cellebrite Physical Analyzer version 8.1.0.12. The findings and limitations documented in this report are specific to the data accessible from the device at the time of examination and to the capabilities and limitations of that software version and the acquisition methods used. No conclusions have been drawn beyond the evidence available in the extracted datasets.

---

## 7. Appendices

| Appendix | Description |
|---|---|
| Appendix A | Automated Extraction Report |
| Appendix B | Hash Verification Output |
| Appendix C | Photographic Log |
| Appendix D | File System Inventory |
| Appendix E | Call Log Export |
| Appendix F | Message Database Export |
| Appendix G | Media File Index |
| Appendix H | Location Artifact Export |
| Appendix I | Screenshot Repository, organized in two folders by extraction method (Advanced Logical / File System), corresponding to Sections 4 and 5. |
| Appendix J | Photo of the SIM tray showing both Telecel and MTN SIM cards as physically installed in the device at time of extraction. ICCID and identifying numbers redacted for privacy. Included to document physical verification of SIM presence referenced in Findings. |

---

*End of Report*
