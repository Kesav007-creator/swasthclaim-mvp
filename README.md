# SwasthClaim 🏥
**Front-Desk Admission & Intimation Engine for Indian Hospitals**

SwasthClaim is a B2B SaaS prototype designed to solve the two biggest operational bottlenecks at the admission desks of Tier-2 and Tier-3 Indian hospitals: **manual paperwork delays** and **revenue leakage due to room-rent capping**.

This product is currently being built alongside active customer discovery with billing heads in the healthcare industry.

## ⚠️ The Problem
1. **The Time Sink:** Despite using digital portals (like IHX), Indian TPAs (Third Party Administrators) still legally require physical, signed "Pre-Authorization" PDFs. Hospital clerks spend 15-20 minutes per patient manually writing or typing redundant data into different PDF layouts for insurers like Star Health, Mediassist, and Vidal.
2. **The Revenue Leakage:** If a patient is admitted to a room that exceeds their policy limit (e.g., Deluxe vs. Twin-sharing), the insurer will proportionately deduct doctor and surgery fees from the final cashless claim, costing the hospital thousands of rupees.

## 🚀 The Solution (MVP Features)
SwasthClaim acts as a lightweight middleware for the hospital reception desk:

* **Feature 1: The Auto-Pre-Auth Generator (Template Engine)**
  The receptionist enters the patient's details once. The Python backend maps this data to exact X/Y coordinates and auto-stamps it onto the specific official PDF layout required by the TPA. Result: A perfectly filled PDF ready for signature in 2 seconds.
* **Feature 2: The Admission Guardrail (Eligibility Checker)**
  A lightning-fast lookup engine. The receptionist types the patient's Corporate/Retail Policy ID, and the system instantly returns the exact Room Rent Limit and Remaining Sum Insured, ensuring the patient is assigned the correct ward on Day 1.

## 🛠️ Tech Stack
* **Backend:** Python, FastAPI
* **PDF Manipulation:** `PyMuPDF` (`fitz`) / `pdfrw`
* **Frontend:** HTML, CSS, Vanilla JavaScript (Iterating to React)
* **Database:** JSON Mocks (Transitioning to PostgreSQL)


## 🗺️ Roadmap
- [x] Customer Discovery & Problem Validation
- [ ] Build basic UI form for data entry
- [ ] Map X/Y coordinates for Star Health Pre-Auth PDF
- [ ] Build Python script to stamp text onto PDF
- [ ] Create mock database for Room Rent lookup
- [ ] Future: Integrate with ABDM Sandbox / NHCX API for live policy data
