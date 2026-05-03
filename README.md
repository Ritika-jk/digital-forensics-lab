## Digital Forensics Laboratory: Investigation & Analysis Portfolio
A professional compendium documenting advanced forensic investigations, evidence preservation techniques, artifact extraction, and digital incident reconstruction.

## Overview
This portfolio serves as the definitive technical record for the Digital Forensics (DFT) Laboratory. It provides a structured methodology for the acquisition, preservation, analysis, and reporting of digital evidence. Every experiment adheres to industry-standard forensic principles to ensure that all findings are legally defensible and technically sound.

## Comprehensive Experiment Index

*1. Forensic Disk Imaging & Integrity Verification*

- Objective: Execute a bit-for-bit physical acquisition of a storage medium using FTK Imager or Guymager and validate the result via SHA-256 cryptographic hashing.
- Focus: Establishing a forensically sound "Gold Master" image. This module emphasizes the "Original Evidence Preservation" principle, ensuring that the source remains untouched while the working copy is verified for 100% accuracy through digital signatures.

*2. Deleted File Recovery & Metadata Analysis*
- Objective: Utilize Autopsy and The Sleuth Kit (TSK) to retrieve deleted data clusters and examine unallocated space within a disk image.
- Focus: Investigating file system structures to recover "ghost" data and analyzing critical metadata—such as MAC (Modified, Accessed, Created) times and ownership permissions—to reconstruct user activity.

*3. Memory Forensics (Volatile RAM Analysis)*
- Objective: Perform live memory capture using DumpIt and conduct deep-dive analysis using the Volatility Framework.
- Focus: Identifying "smash-and-grab" evidence that disappears upon reboot, including active process trees, injected code, hidden network connections, and decrypted credentials residing in volatile memory.

*4. Timeline Analysis & File System Chronology* 
- Objective: Generate a unified system-wide timeline using Plaso (log2timeline) or the Autopsy Timeline engine.
- Focus: Correlating disparate system events into a single chronological narrative. This helps investigators identify the exact moment of compromise and detect anomalous patterns that deviate from standard operating behavior.

*5. Advanced Metadata Extraction: Media & Documents*
-  Objective: Leverage ExifTool and PDFinfo to parse embedded metadata from multimedia files and office documents.
- Focus: Uncovering "hidden" data layers, such as original author identities, GPS coordinates (geotags) from images, software versions used for creation, and revision histories that are not visible to the casual user.


*6. Email Header Investigation & PGP Authentication*
- Objective: Trace email origins through header analysis in Thunderbird and verify the integrity of encrypted communications using Gpg4win (Kleopatra).
- Focus: Mapping the "hop-by-hop" path of an email to identify the originating IP address and utilizing Pretty Good Privacy (PGP) tools to confirm sender authenticity and message non-repudiation.

*7. Browser Artifact & Web Activity Inspection*
- Objective: Systematically examine browsing history, cache files, and persistent cookies using Browser History Examiner and Nirsoft utilities.
- Focus: Reconstructing a user’s online persona and activity. This includes identifying visited URLs, search queries, downloaded files, and potential drive-by-download infection vectors.

*8. Android Mobile Device Forensics*
- Objective: Conduct a logical or physical extraction of an Android device image for analysis in Andriller or Autopsy.
- Focus: Retrieving mobile-specific artifacts such as call logs, SMS/MMS messaging threads, third-party app data (WhatsApp, Telegram), and saved location history.

*9. Hash-Based Integrity & Tamper Detection*

- Objective: Implement rigorous file integrity checks using sha256sum and md5deep for mass-file comparison.
- Focus: Detecting unauthorized modifications or "bit rot" in evidence. This ensures that the chain of custody remains intact by proving that no data alteration has occurred between the collection and trial phases.

*10. Multi-Source Incident Reconstruction*

- Objective: Aggregate system logs, network traffic, and host artifacts into Timesketch for collaborative analysis.
- Focus: High-level incident response. By correlating multiple evidence sources, investigators can build a comprehensive visual narrative of a security breach and prepare formal, professional-grade forensic reports.

## Technical Stack & Toolset

Disk & File Forensics	FTK Imager, Autopsy, Sleuth Kit	Imaging, Recovery, & File System Analysis
Memory Forensics	Volatility 3, DumpIt	Volatile RAM Capture & Artifact Extraction
Metadata Analysis	ExifTool, PDFinfo	Document & Media Intelligence
Network & Email	Thunderbird, Gpg4win, Wireshark	Header Tracing & Cryptographic Verification
Mobile & Web	Andriller, NirSoft Suite, BHE	Mobile Artifacts & Browsing History
Incident Timeline	Plaso, Timesketch	Log Aggregation & Event Correlation
## Core Methodologies
*Evidence Preservation*: Utilizing write-blockers and bit-stream imaging to protect original data.

*Cryptographic Validation*: Mandatory use of SHA-256/MD5 hashing at every stage of the lifecycle.
Author: Ritika Sharma

*Timeline Reconstruction*: Building chronological maps to visualize the "Who, What, When, Where, and How."

*Chain of Custody*: Rigorous documentation of evidence handling to ensure legal admissibility.
