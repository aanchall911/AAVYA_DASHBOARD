# AAVYA — Victim Support & Case Coordination Platform
### Smart India Hackathon (SIH) | Problem Statement: PS 26094
> **Official Police, Coordination & Clinical Monitoring Dashboard with Integrated Victim & Family Android App Ecosystem**

---

## 📌 Executive Summary

Under **Smart India Hackathon (SIH) Problem Statement 26094**, **AAVYA** is an end-to-end, victim-centric digital ecosystem designed to bridge the critical gap between law enforcement agencies, judicial proceedings, mental health professionals, and vulnerable victims along with their families.

Traditional case tracking often leaves victims isolated, uninformed of case developments, and vulnerable to retaliation or acute psychological trauma. **AAVYA** provides a unified, secure, multi-stakeholder platform comprising:
1. **AAVYA Official & Clinical Web Dashboard** *(This Repository)*: High-throughput operational command portal for Police Officers, Case Coordinators, and Clinical Psychologists.
2. **AAVYA Victim & Family Companion Android App** *(Mobile Client)*: Secure, trauma-informed native mobile application providing real-time SOS alerts, anonymous case status tracking, emotional well-being check-ins, and direct support request pipelines.

```
┌────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                   AAVYA ECOSYSTEM OVERVIEW                                     │
└────────────────────────────────────────────────────────────────────────────────────────────────┘

         ┌─────────────────────────────────┐               ┌──────────────────────────────────┐
         │     VICTIM & FAMILY MOBILE      │               │     AAVYA WEB DASHBOARD (PORTAL) │
         │       (Android Application)     │               │    (Police & Trauma Specialists) │
         └────────────────┬────────────────┘               └─────────────────┬────────────────┘
                          │                                                  │
       SOS / Distress     │  • Real-time Panic Trigger                       │  • Live Incident Map & Triage
       Safety Alerts      ├─────────────────────────────────────────────────►│  • Dispatch & Unit Action Logs
                          │                                                  │
       Psychological      │  • Periodic Self-Assessment                      │  • Role-Gated Clinical Trends
       Well-being         ├─────────────────────────────────────────────────►│  • Longitudinal Distress Chart
                          │                                                  │
       Case Stages &      │  • FIR & Investigation Milestones                │  • Official Stage Progression
       Hearings           │◄─────────────────────────────────────────────────┤  • Summons & Court Calendar
                          │                                                  │
       Support & Relief   │  • Shelter, Legal Aid, Medical                   │  • Inter-Agency Allocation
       Requests           │◄─────────────────────────────────────────────────┤  • Case Resolution Tracking
                          │                                                  │
                          └───────────────────────┬──────────────────────────┘
                                                  │
                                      ┌───────────▼───────────┐
                                      │ AAVYA API & SYNC CORE │
                                      │  (Encrypted Gateway)  │
                                      └───────────────────────┘
```

---

## 🎯 Key Objectives for SIH PS 26094

- **Victim Safety & Swift Incident Response**: Real-time triage of high-risk cases, instant escalation of threats, and systematic deployment of witness/victim protection measures.
- **Inter-Agency Coordination**: Seamlessly connect investigating officers, legal coordinators, social workers, and clinical psychologists under strict role-based access controls (RBAC).
- **Victim Empowerment & Transparency**: Keep victims and authorized family members updated on case milestones, court hearing dates, and protection statuses without compromising confidential police investigations.
- **Mental Health & Trauma Monitoring**: Continuous psychological safety monitoring to identify distress spikes, post-traumatic reactions, and clinical intervention needs early.
- **Auditable Chain of Custody**: Complete tamper-evident action logging for every official intervention, inquiry, and assistance dispatch.

---

## 📱 Integration: Connecting the Victim & Family Android App

The **AAVYA Android App** is designed for victims and their verified family members. It connects directly with this dashboard to provide a secure two-way lifeline:

### 1. Instant SOS & Threat Escalation
* **Mobile Action**: The victim or family member taps the one-touch Emergency SOS button or voice trigger on the Android app.
* **Dashboard Synchronization**: A high-priority **RED ALERT** pops up immediately in the **Safety Alerts Screen** of the police dashboard with geo-coordinates, timestamp, and victim reference code (`VIC-XXXX`). Officers can immediately dispatch patrol units and log interventions.

### 2. Anonymous Case Timeline & Court Notifications
* **Dashboard Action**: When an officer updates the case stage (*Complaint Registered* → *Investigation* → *Legal Proceedings* → *Trial* → *Rehabilitation*) or schedules a court date in the **Proceedings Screen**, the update is committed.
* **Mobile Synchronization**: The Android app receives a push notification and displays user-friendly progress indicators, date/time of hearing, required documents, and protective guidelines, eliminating procedural anxiety.

### 3. Trauma-Informed Distress & Psychological Check-ins
* **Mobile Action**: The victim completes brief, accessible weekly check-ins (evaluating sleep difficulty, emotional distress, fear/anxiety, and well-being).
* **Dashboard Synchronization**: Data is tokenized and transmitted strictly to the **Psychologist Portal**. The system computes a longitudinal distress score and flags upward trends (*Rising*, *Rapid Rise*), allowing licensed psychologists to intervene or schedule counselling.

### 4. Support & Rehabilitation Requests
* **Mobile Action**: Victims can request legal aid, emergency shelter, medical evaluations, or victim compensation relief directly from their phone.
* **Dashboard Synchronization**: The request enters the **Support Requests Screen** where coordinators assign dedicated agencies, set follow-up dates, and track completion status.

---

## 🛡️ Role-Based Access Control (RBAC) Architecture

AAVYA enforces strict confidentiality boundaries between law enforcement personnel and clinical healthcare workers:

| Feature / Data Domain | Police Officer / Case Coordinator | Trauma Psychologist / Clinical Specialist |
| :--- | :---: | :---: |
| **Safety Alerts & Triage** | Full Access (Acknowledge, Dispatch, Resolve) | Read-only / Reference |
| **Case Investigation & FIR Details** | Full Access (Edit Stages, Officers, FIR) | Metadata Only (Anonymous Reference) |
| **Protection Orders & Security Measures** | Full Control (Patrol Routes, Safehouses) | Read-only (Safety Context) |
| **Legal Proceedings & Court Dates** | Full Control (Add hearings, summons) | View Schedule (Prep victim for court) |
| **Psychological Trend Analysis & Scores** | ⛔ **Hidden** (Confidentiality Protected) | Full Access (Longitudinal Charts & Flags) |
| **Clinical Session Notes & Assessments** | ⛔ **Hidden** (Doctor-Patient Privilege) | Full Access (Add, Edit, Sign Assessments) |
| **Inter-Agency Support Coordination** | Full Management | Request Counselling / Support |
| **Official Action Audit Trail** | Full Access (Record & Review Logs) | View Clinical Coordination Actions |

---

## 🖥️ Dashboard Screens & Functional Modules

### 1. Police & Case Coordinator Portal
- **Dashboard Overview (`/dashboard`)**: Metric cards for Open Cases, Immediate Concerns, Active Protection Orders, and Pending Court Proceedings.
- **Safety Alerts (`/alerts`)**: Multi-tier alert queue (Red: Immediate Danger, Orange: Protection Review, Yellow: Support Assistance) with real-time acknowledgment and response dispatching.
- **Case Directory & Detail (`/cases`, `/case-detail`)**: Comprehensive view of all registered cases featuring anonymous references, timeline steppers, FIR data, assigned officers, and instant case action logging.
- **Protection Orders (`/protection`)**: Active threat level assessments (*Low*, *Moderate*, *Critical*), protection measure checklists (patrols, phone taps, safe transit, CCTV), and mandatory review scheduling.
- **Legal Proceedings (`/proceedings`)**: Court appearance schedules, summons verification, venue tracking, and attendee requirements with victim notification dispatching.
- **Support Requests (`/support`)**: Central hub for inter-agency rehabilitation requests (Free Legal Aid, Shelter Assistance, Medical Exams, Criminal Injury Compensation).
- **Official Action Log (`/action-log`)**: Immutable chronological audit trail of all officer assignments, visits, victim calls, and court filings.

### 2. Psychologist & Clinical Monitoring Portal
- **Psychological Overview (`/psy-dashboard`)**: High-level clinical triaging displaying victims with *Rising* or *Rapid Rise* distress, pending review decisions, and active cases.
- **Psychological Case Detail (`/psy-case-detail`)**:
  - Interactive 4-week distress progression chart (0–100 score).
  - Multi-indicator breakdown (Emotional Distress, Fear/Anxiety, Sleep Disturbance, Social Withdrawal, Overall Well-being).
  - Risk factor badges and flagged behavioral reasons.
  - Review Decision Module (*Confirmed*, *Downgraded*, *Escalated*).
- **Clinical Assessments & Notes (`/psy-analytics`)**: Secure clinical repository for session notes, psychiatric assessments, and referral recommendations.
- **Referrals Management (`/psy-referrals`)**: Tracking status for specialized psychiatric interventions, NGO counseling partners, and trauma recovery therapies.

---

## 🛠️ Technology Stack

- **Frontend Framework**: [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- **Build Tool & Dev Server**: [Vite 8](https://vitejs.dev/) with optimized HMR and allowed host routing
- **Styling**: [Tailwind CSS v4](https://tailwindcss.com/) with custom slate/police blue theme and accessible UI components
- **Motion & Interactions**: [Motion](https://motion.dev/) for smooth transitions and accessible alert modals
- **Icons**: [Lucide React](https://lucide.dev/)
- **State Management**: React Context (`AppContext.tsx`) with dynamic role toggling between Police Official and Psychologist
- **Security & Reliability**: Strict TypeScript typing, no sensitive logs exposed in client UI, sanitized inputs, and responsive desktop/tablet/mobile viewport support

---

## 📂 Project Directory Structure

```
├── index.html                     # HTML5 entry point with AAVYA SEO & meta tags
├── metadata.json                  # AI Studio & SIH application metadata
├── package.json                   # Dependencies, dev dependencies & scripts
├── tsconfig.json                  # Strict TypeScript configuration
├── vite.config.ts                 # Vite bundler, host configuration & plugins
├── src/
│   ├── App.tsx                    # Root layout, role routing & navigation container
│   ├── main.tsx                   # React 19 root bootstrap
│   ├── index.css                  # Global Tailwind CSS imports
│   ├── types/
│   │   └── index.ts               # Shared types for Cases, Alerts, RBAC, & Psychology
│   ├── context/
│   │   └── AppContext.tsx         # Central application state, user sessions & mutations
│   ├── data/
│   │   └── mockData.ts            # Realistic mock data aligned with SIH PS 26094
│   ├── components/
│   │   ├── Header.tsx             # Role indicator, notifications & user profile
│   │   ├── Sidebar.tsx            # Adaptive navigation for Official & Psychologist
│   │   ├── AssignOfficerModal.tsx # Dynamic officer dispatch modal
│   │   ├── RecordActionModal.tsx  # Quick action logging modal
│   │   ├── FooterDisclaimer.tsx   # Official portal compliance & helpline banner
│   │   ├── StatusBadge.tsx        # Normalized status tags (Safety, Urgency, Stage)
│   │   ├── Toast.tsx              # Dynamic feedback notifications
│   │   └── psychologist/
│   │       ├── DistressChart.tsx  # SVG/Canvas distress progression curve
│   │       └── AddNoteModal.tsx   # Confidential psychological session entry
│   └── screens/
│       ├── LoginScreen.tsx        # Multi-role portal login (Official / Psychologist)
│       ├── DashboardScreen.tsx    # Police operational command center
│       ├── SafetyAlertsScreen.tsx # High-risk SOS & protection alert queue
│       ├── CasesScreen.tsx        # Filterable case list with search & district filters
│       ├── CaseDetailScreen.tsx   # Comprehensive case inspection & timeline
│       ├── ProtectionScreen.tsx   # Protection order management & threat assessments
│       ├── ProceedingsScreen.tsx  # Court hearings & judicial diary
│       ├── SupportRequestsScreen.tsx # Multi-departmental victim aid coordination
│       ├── ActionLogScreen.tsx    # Complete audit log with filters
│       ├── SettingsScreen.tsx     # System configuration & notification preferences
│       └── psychologist/
│           ├── PsychologistDashboardScreen.tsx # Clinical triage & flagged victims
│           ├── PsychologistCaseDetailScreen.tsx# In-depth psychological evaluation
│           ├── PsychologistAnalyticsScreen.tsx # Population mental health metrics
│           ├── PsychologistReferralsScreen.tsx # External referral tracking
│           └── PsychologistSettingsScreen.tsx  # Clinical credentials & protocols
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (version 20.x or higher recommended)
- npm or bun

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-org/aavya-dashboard.git
   cd aavya-dashboard
   ```

2. **Install project dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```
   The dashboard will be accessible at: `http://localhost:3000`

4. **Verify TypeScript & Production Build:**
   ```bash
   npm run lint
   npm run build
   ```

---

## 🔒 Victim Anonymity & Data Protection Standards

In accordance with legal guidelines for victim safety:
1. **Masked Identifiers**: Victims are identified across all official screens using irreversible tokenized codes (`VIC-XXXX`). Direct personal identifiers are never rendered in public or open views.
2. **End-to-End Encryption for Mobile Check-ins**: Distress questionnaire results from the Android app are encrypted on device and only decrypted inside the Psychologist session.
3. **Audit Trails**: Every view, status change, and officer assignment is recorded with the active officer’s badge number, designation, and timestamp for complete accountability.
4. **Emergency Helplines**: Persistent access to National Emergency (`112`), Women Helpline (`1091`), and National Tele-Mental Health (`14416`) across both web and mobile clients.

---

## 🔗 Android App Connectivity Specifications (API Blueprint)

To interface the **AAVYA Victim & Family Android App** with this portal, the backend API exposes the following primary endpoints:

| Endpoint | Method | Role | Description |
| :--- | :---: | :---: | :--- |
| `/api/v1/mobile/sos` | `POST` | Victim | Triggers immediate RED alert on Police Dashboard with live GPS coordinates. |
| `/api/v1/mobile/case/status` | `GET` | Victim/Family | Returns non-confidential case stage (`timelineStep`), assigned officer contact, and next hearing date. |
| `/api/v1/mobile/distress-checkin` | `POST` | Victim | Ingests weekly 5-question psychological check-in scores directly to the clinical dataset. |
| `/api/v1/mobile/support-request` | `POST` | Victim | Submits requests for Legal Assistance, Shelter, Medical Review, or Financial Aid. |
| `/api/v1/mobile/hearings` | `GET` | Victim/Family | Retrieves court appearance schedules, venue details, and protective instructions. |

---

## 🏆 Smart India Hackathon (SIH) Evaluation Highlights

- **Direct Impact on PS 26094**: Solves the real-world operational bottlenecks in victim safety triage and inter-agency coordination.
- **Dual-Perspective Innovation**: Eliminates the barrier between enforcement (police) and healing (psychological trauma support) while strictly preserving medical privacy.
- **Mobile + Web Harmony**: True bidirectional communication where victim SOS and emotional updates immediately inform police action and clinical care.
- **Production-Ready UX**: Fast, accessible, responsive interface designed for high-stress police control rooms and clinical consulting rooms.

---

*Developed for Smart India Hackathon (SIH) — Problem Statement PS 26094.*  
*AAVYA — Shielding Safety, Rebuilding Lives.*
