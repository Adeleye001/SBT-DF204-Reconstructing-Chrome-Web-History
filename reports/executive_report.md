# Digital Forensics Investigation Report: Chrome Web History Analysis

**Case / Lab Code:** SBT-DF204  
**Module:** Reconstructing Chrome Web History  
**Examiner:** Adeleye Ademiluyi  
**Date:** October 12, 2026  

---

## 1. Executive Summary
An independent forensic examination was conducted on an ingested Google Chrome History SQLite database file (evidence/History). The primary objective was to reconstruct user browsing habits, isolate keyword search queries, identify downloaded files, and establish a precise chronological timeline of events leading up to financial transactions on April 19, 2022.

---

## 2. Evidence Integrity & Chain of Custody
To maintain legal and forensic admissibility, cryptographic hashing was performed immediately upon ingestion:
* **Evidence File:** evidence/History
* **File Size:** 192 KB
* **SHA-256 Hash:** b991b0fa69662c44caf599e468c8088576ebd9cebbf46d02c89cf51bcde3fd19

---

## 3. Chronological Reconstruction & Findings
By querying the urls, visits, keyword_search_terms, and downloads tables—and converting WebKit microsecond timestamps (offset -11644473600) into local time—the following behavioral sequence was established:

1. **Authentication (09:58 – 09:59 UTC+1):**  
   The subject authenticated into Gmail under account unsub.fscs@gmail.com via standard Google service login challenges.
2. **Communication & Orders (10:04 – 10:05):**  
   The user interacted with email correspondence regarding an order titled "cheaper than Rx supplements - order" referencing transaction identifier 517b2156914944339a96137ad8978408ea52b2fc144c98d3b0b16b21888afdc5.
3. **Evidence Acquisition (10:56):**  
   The user downloaded a receipt file named proof_of_payment.png (33,844 bytes) to the local desktop environment.
4. **Blockchain & Financial Verification (10:58 – 11:02):**  
   The user performed searches for "blockchain explorer" and "kraken", verified transaction hashes and wallet addresses across blockchain.com and mempool.space, completed a device approval on Kraken, and reviewed financial ledgers showing an active balance exceeding 41,500 USD.

---

## 4. Conclusion & Recommendations
The artifact recovery successfully established a direct link between email communications, proof-of-payment image downloads, blockchain transaction verifications, and exchange account activities. It is recommended that these findings be archived alongside full disk image extractions if broader scope analysis is required.
