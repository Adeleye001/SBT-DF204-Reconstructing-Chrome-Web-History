# SBT-DF204: Reconstructing Chrome Web History

## Overview
This repository contains the forensic evidence, extraction scripts, query reports, and documentation for SBT-DF204 (Module 2: Reconstructing Chrome Web History). The lab focuses on deep artifact recovery, SQLite database parsing, WebKit epoch timestamp conversion, and digital evidence chain-of-custody documentation.

---

## Repository Structure
SBT-DF204-Reconstructing-Chrome-Web-History/
├── evidence/              # Securely ingested Chrome History SQLite database
├── reports/               # Raw query outputs and executive summaries
│   ├── evidence_hash.txt  # SHA-256 cryptographic verification hash
│   ├── timeline_extract.txt # Chronological browsing activity export
│   ├── search_terms_extract.txt # Omnibox keyword search terms
│   ├── downloads_extract.txt    # Downloaded file artifacts log
│   └── executive_report.md      # Formal DFIR investigation report
├── screenshots/           # Terminal execution and verification captures
└── README.md              # Project documentation and summary

---

## Key Forensic Findings Summary
* Evidence Ingestion: Chrome History database verified via SHA-256 hash (b991b0fa69662c44caf599e468c8088576ebd9cebbf46d02c89cf51bcde3fd19).
* Timeline Analysis: Reconstructed user activity on April 19, 2022, tracking a sequence from Gmail authentication to blockchain transactions and cryptocurrency exchange access.
* Artifact Correlation: Discovered the download of C:\Users\FSCS_User\Desktop\proof_of_payment.png (33,844 bytes) at 10:56:58, directly tied to an external transaction identifier (txid: 517b2156...) and an Rx supplement order thread.
