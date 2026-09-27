# SAHAKAR-SETU (सहकार-सेतु)
### AI & LMS - Enabled Cooperative Capacity Building, ERP & Employment Ecosystem

**Smart India Hackathon (SIH) 2026** | **Problem Statement ID:** 26087  
**Ministry:** Ministry of Cooperation, Government of India  
**Department / Apex Organization:** National Council for Cooperative Training (NCCT)  
**Theme:** Smart Education | **Category:** Hardware | **Proposed Mode:** Software + Hardware  

---

## 📌 Executive Summary

India is currently investing **₹2,925.39 Crores** to computerize and modernize **79,630 Primary Agricultural Credit Societies (PACS)** onto a unified national ERP. However, the human capital engine driving this transformation remains constrained by paper-based registrations, proxy attendance, low-bandwidth rural connectivity barriers, and unverified paper certifications.

**SAHAKAR-SETU** is a unified, production-grade digital and hardware ecosystem bridging NCCT's 20 apex training institutions (VAMNICOM Pune, 5 RICMs, 14 ICMs) with 79,630 computerized PACS and rural learners.

```
┌──────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                    SAHAKAR-SETU ECOSYSTEM                                        │
├───────────────────┬───────────────────┬──────────────────────┬───────────────────────────────────┤
│ 1. TRAINING ERP   │ 2. EDGE HARDWARE  │ 3. VERNACULAR LMS    │ 4. EMPLOYMENT EXCHANGE            │
│ 20 NCCT Institutes│ 8" Android Kiosk  │ Audio-First (<2MB)   │ Direct 79,630 PACS Recruiter Desk │
│ Batch & Hostel Grid│ Local Face Match  │ 22 PACS ERP Sandbox  │ W3C Ed25519 Cryptographic QR      │
│ Verified TA/DA    │ <80ms / Anti-Spoof│ 22 Indic Languages   │ Automated DigiLocker / NAD Push   │
└───────────────────┴───────────────────┴──────────────────────┴───────────────────────────────────┘
```

---

## 🏛️ Master Technical System Architecture

![Master Architecture Diagram](master_architecture_cream.png)

### 5-Layer Architectural Topology
1. **Layer 1 (Client & Edge Interfaces):** Offline-first Next.js 14 Trainee PWA (<1.2MB payload), Web Audio MediaRecorder Voice Assistant, React Admin Portals with FullCalendar, and an autonomous 8-inch Android edge attendance kiosk.
2. **Layer 2 (Gateway & Security Layer):** Nginx / Cloudflare reverse proxy enforcing TLS 1.3 strict ciphers, WAF rate limiting, and JWT Role-Based Access Control (RBAC) isolating 20 institutes.
3. **Layer 3 (Core Modular Monolith Backend):** High-performance asynchronous FastAPI core hosting Camunda BPMN approval workflows, automated TA/DA stipend calculator with anomaly fraud gates, audio micro-lesson bundlers, 22-module PACS ERP sandbox engine, asymmetric Ed25519 certificate signers, and an explainable deterministic job ranker.
4. **Layer 4 (Persistence & Data Storage):** Multi-tenant PostgreSQL 16 with Row-Level Security (RLS) and `pg_trgm` fuzzy matching, Redis 7 in-memory task broker & Celery worker queues, and Cloudflare R2 / AWS S3 encrypted object storage.
5. **Layer 5 (National DPI & External Integrations):** AI4Bharat / Bhashini (IndicWhisper ASR, IndicTrans2, Meta MMS-TTS in 22 Scheduled languages), DigiLocker / National Academic Depository (NAD), National Career Service (NCS), National Cooperative Database (NCD), and NIC Gov SMS / WhatsApp DLT gateway.

---

## 🔄 End-to-End User Flow & Operational Journey

![User Flow with Roles](userflow_with_users.jpg)

### Operational Lifecycle Stages:
1. **Stage 1 (Discovery & Nomination):** Rural youth discover courses via voice queries in 22 regional languages; PACS Secretaries submit bulk candidate rosters.
2. **Stage 2 (Institute ERP & Campus Logistics):** Automated approval routing via Camunda BPMN; conflict-free timetable scheduling; real-time hostel room and bed allocation grid.
3. **Stage 3 (Smart Attendance Kiosk):** Trainee scans face at classroom doorway; INT8 MobileFaceNet ONNX executes biometric match in `<80ms` with MiniFASNet anti-spoofing; local SQLite buffers 50,000 check-ins offline; TA/DA stipend calculated automatically.
4. **Stage 4 (Multilingual Micro-LMS):** Trainees listen to audio lessons (`<2MB/module`) cached in browser `IndexedDB` and practice real daybook entries inside an in-browser 22-module PACS ERP simulator.
5. **Stage 5 (Verifiable Certification):** Instant certificate generation with asymmetric Ed25519 signatures encoded in 2D QR codes; verified offline in `<15ms` ($0 gas fees); pushed directly to citizen DigiLocker vaults.
6. **Stage 6 (Cooperative Employment Exchange):** 79,630 PACS post vacancies; candidates apply in 1-click attaching cryptographically verified transcripts; ranked via an auditable, deterministic formula.
7. **Stage 7 (National Governance):** Live executive dashboard for Ministry of Cooperation and NCCT HQ tracking training KPIs, state diversity, placement ROI, and fraud fund savings.

---

## 📊 Modules Grouped by Deployment Platform

![Modules Grouped by Technology](modules_grouped_by_tech.jpg)

| Deployment Platform | Key Modules & Components | Primary Users & Roles | Technology Stack |
| :--- | :--- | :--- | :--- |
| **📱 Mobile PWA & App** | • Trainee Portal<br>• Audio Micro-LMS<br>• PACS ERP Simulator<br>• Voice AI Assistant<br>• Dynamic QR Token | Rural Youth, Women SHGs, Farmers, Trainees | Next.js 14 PWA, IndexedDB, Tailwind CSS |
| **💻 Responsive Web Portals** | • Institution ERP<br>• Timetable Scheduler<br>• Hostel Bed Grid<br>• Recruiter Job Exchange<br>• Public Credential Verifier<br>• National Executive Cockpit | Institute Coordinators, Wardens, Faculty, PACS Recruiters, Ministry | React / Next.js, TanStack Table, FullCalendar, Camunda BPMN |
| **📟 Physical Hardware & Edge** | • Wall-Mounted Rugged Kiosk<br>• Edge Face Recognition<br>• Anti-Spoof Liveness<br>• Offline Event Spooler | Trainees (Face Scan at Door), Campus Gatekeepers | Android Tablet / RK3566, ONNX Runtime Mobile, OpenCV, SQLite |
| **⚙️ Cloud Backend & Database** | • Core API Gateway<br>• Multi-Tenant Database<br>• Cryptographic Credential Signer<br>• Verified Stipend Rule Engine | System Services, Database Administrators, Audit Officers | Python FastAPI, PostgreSQL 16 (RLS), Redis, Ed25519 (PyNaCl) |
| **🌐 AI & DPI Integrations** | • Multilingual Voice Gateway<br>• DigiLocker & NAD Sync<br>• National Cooperative Database<br>• National Career Service Exchange | Pan-India Citizens, Ministry Leadership, Verifiers | AI4Bharat, Bhashini API, DigiLocker API, NCS API |

---

## 🗂️ Complete 45-Component Census

| Subsystem Group | Component Count | Summary of Key Deliverables |
| :--- | :--- | :--- |
| **1. Institution ERP Platform** | 10 Components | Self-registration, bulk nominations, Camunda approval workflow, trainee/institute/faculty profiles, timetable scheduler, hostel bed matrix, mess tracking, verified TA/DA stipend calculator. |
| **2. Smart Digital Attendance** | 5 Components | Kiosk client app, INT8 MobileFaceNet edge recognition (<80ms), MiniFASNet anti-spoofing, dynamic TOTP QR fallback, 50k offline SQLite buffer. |
| **3. Interactive Multilingual LMS** | 4 Components | Micro-learning delivery (22 languages), multimedia learning hub, in-browser 22-module PACS ERP simulator, assessment and quiz engine. |
| **4. Skill Certification & Verification** | 4 Components | Auto certificate generator, asymmetric Ed25519 2D QR signer, zero-login public verification portal, centralized transcript repository. |
| **5. Cooperative Employment Exchange** | 5 Components | Recruiter portal, vacancy posting interface, talent directory search, 1-click verified application workflow, explainable deterministic ranker. |
| **6. AI Career Counseling Chatbot** | 3 Components | Vernacular voice/text interface (22 languages), cooperative rules guidance engine, automated course recommendation algorithm. |
| **7. Mobile-Friendly Trainee Client** | 2 Components | Next.js 14 Progressive Web App (<1.2MB payload), Serwist/Workbox offline content caching manager. |
| **8. Centralized Database & Analytics** | 3 Components | Multi-tenant PostgreSQL 16 with Row-Level Security, Ministry & NCCT HQ macro analytics cockpit, automated SMS/WhatsApp outreach engine. |
| **9. Physical Hardware Specifications** | 4 Components | 8-inch rugged tablet/SBC, wide-angle HD optical camera sensor, tamper-resistant wall mount with keylock, internal 5000mAh battery backup. |
| **10. National DPI & Ecosystem Gateways** | 5 Gateways | API Gateway/WAF, DigiLocker/NAD API, National Career Service (NCS) API, National Cooperative Database (NCD) API, NIC SMS/WhatsApp Gateway. |
| **TOTAL ARCHITECTURAL ELEMENTS** | **45 Elements** | **100% Comprehensive Coverage of PS ID 26087** |

---

## 💡 Key Architectural Innovations

1. **Edge Biometrics vs. Broken Fingerprints:** Up to 28% of agricultural workers experience failure-to-enroll on optical thumb scanners due to worn friction ridges. Our 8-inch tablet kiosk runs INT8 MobileFaceNet locally in `<80ms` with MiniFASNet liveness detection. Complies 100% with India's **DPDP Act 2023** (raw camera frames are purged from RAM; only 128-d vectors are stored).
2. **Stipend Leakage Prevention:** Travel & Daily Allowances (TA/DA) are cryptographically bound to biometric door-scan timestamps, supported by automated duplicate claim & anomaly detection saving an estimated **₹1.2–₹2.5 Cr annually**.
3. **Audio-First LMS over Video:** Replaces 500MB video streams with `<2MB` audio micro-lessons in 22 Scheduled Indian languages, paired with an offline in-browser sandbox replicating 22 live PACS ERP software modules.
4. **W3C Cryptographic Credentials over Blockchain:** Employs asymmetric Ed25519 private-key signatures embedded in 2D QR codes verified in `<15ms offline` with **$0 gas fees**, pushed directly to citizen DigiLocker accounts.
5. **Auditable Deterministic Job Ranker:** Replaces unexplainable black-box AI with a transparent public-sector hiring formula:
   $$\text{Rank Score} = w_1(\text{Exam Grade}) + w_2(\text{Proximity}) + w_3(\text{Recency})$$
6. **Voice AI with Strict Refusal Gate:** Voice-in/voice-out assistant (AI4Bharat IndicWhisper) with a strict RAG retrieval boundary that refuses out-of-scope questions, preventing misinformation.

---

## 📁 Repository Structure & Documentation Index

```
├── .agents/skills/                   # AI Coding & Architecture Skills
│   ├── arkitect/                     # Architecture diagramming skill (Draw.io / Excalidraw)
│   ├── sih-presentation-strategist/  # Smart India Hackathon slide deck guidelines
│   ├── technical-content-writer/     # Engineering documentation standards
│   ├── senior-ml-agent/              # Edge ML & model deployment specs
│   └── ponytail/                     # Minimalist architecture & YAGNI optimization
│
├── ARCHITECTURE.md                   # Complete 25-section CTO Master Architecture Document
├── RESEARCH.md                       # Government policy research, DPI links & citations
├── PROPOSED_SOLUTION.md              # Requirement-by-requirement technical solution mapping
├── TECHNICAL_SYSTEM_ARCHITECTURE.md  # 45-component technical census & explicit data flow specs
├── PPT_CONTENT.md                    # Slide-by-slide copy-paste ready presentation deck
├── SIH_EVALUATION_DECK_6_SLIDES.md   # Official 6-Slide presentation deck template
├── discussion.md                     # Living architectural decision ledger & discussions
│
├── generate_diagram.py               # Python generator script for vector architecture diagrams
├── master_architecture_cream.svg     # Scalable vector architecture diagram (Cream palette)
├── master_architecture_cream.png     # High-resolution raster diagram
├── master_architecture_cream.pdf     # Vector printable architecture document
├── master_architecture_viewer.html   # Interactive web viewer for system architecture
│
├── system_user_flow.jpg              # Horizontal 16:9 end-to-end userflow visual
├── vertical_user_flow.jpg            # Vertical 9:16 operational flowchart
├── userflow_with_users.jpg           # Two-column operational flow with primary user badges
├── modules_grouped_by_tech.jpg       # Technology deployment platform matrix
└── technical_system_architecture.jpg # 5-Layer technical blueprint image
```

---

## 🚀 Running the Architecture Generator Locally

### Prerequisites
```bash
python --version   # Python 3.10+
pip install reportlab svglib pypdfium2 pillow
```

### Generate Vector Diagrams
```bash
python generate_diagram.py
```
This outputs `master_architecture_cream.svg`, which can be viewed directly in any browser or converted into high-resolution PNG/PDF assets.

---

## 📜 License & Acknowledgements
Developed for the **Ministry of Cooperation, Government of India** and the **National Council for Cooperative Training (NCCT)** under the **Smart India Hackathon (SIH) 2026**.  
Licensed under the **MIT License**.
