# Library Management Platform
# Unit 1: Product Engineering & Design Thinking

## 1. Business Problem Statement & Business Justification

### Business Domain
Academic Library Services.

### Core Problem Statement
Library members experience severe operational delays in locating, reserving, borrowing, and returning literary resources due to inefficient manual tracking. Concurrently, administrative staff lack centralized real-time visibility, leading to unrecorded losses, reporting errors, and poor user satisfaction.

### Core Library Operations
1. Book Acquisition & Cataloging
2. Membership Management
3. Search & Circulation Workflow
4. Financial Penalties
5. Administrative Analytics

### Manual Challenges and Automated Solutions

| Manual Bottleneck | Automated Platform Solution | Business Outcome |
|---|---|---|
| Physical searching across card catalogs | Indexed database with multi-field search engine | Search time reduced from 25 min to <5 seconds |
| Manual paper ledger entries for checkout | Automated barcode/QR scanner integration | Queue processing speed improved by 80% |
| Manual tracking of overdue items | Cron-driven notification system and dynamic fine calculation | Overdue return rates decreased by 40% |
| Human error, lost records and missing inventory | Relational database with strict integrity constraints | Record accuracy brought to 99.9% |

---

## 2. Product Vision & MVP Feature Matrix

### Product Vision Statement

"To deliver a modern, automated, and cloud-native Library Management Platform that eliminates manual administrative overhead, streamlines circulation workflows, and delivers an intuitive digital catalog experience for academic communities."

### MVP Release Scope

| MVP Feature | Description |
|---|---|
| User Login & Profile RBAC | Role-based access for users |
| Book Search & Availability Status | Search books and view availability |
| Basic Issue & Return Transaction Management | Manage circulation transactions |
| Automated Fine Calculation Logic | Calculate overdue penalties |
| Basic Administrative Reporting | Provide basic administrative reports |

### Deferred Capabilities
AI book recommendations and third-party payment gateways are deferred from the MVP.

---

## 3. Stakeholder Responsibility Matrix & User Personas

### User Personas

#### Aarav — Student
**Objective:** Find academic references fast and avoid late fines.  
**Frustrations:** Long physical queues and unexpected fine accumulation.  
**Target Features:** Mobile search portal and push/email due-date alerts.

#### Mrs. Sunita — Librarian
**Objective:** Process checkouts quickly and maintain accurate catalog inventory.  
**Frustrations:** Manual record entries, stock discrepancies and lost books.  
**Target Features:** Barcode issue/return interface and automated fine tracker.

#### Dr. Verma — Library Administrator
**Objective:** Monitor library utilization and generate departmental compliance reports.  
**Frustrations:** Lack of real-time usage data and manual report generation taking days.  
**Target Features:** Executive analytics dashboard with 1-click PDF export.

### Stakeholder Matrix

| Stakeholder Group | Key Roles | Responsibilities & Expectations |
|---|---|---|
| Business Stakeholders | College Management, Library Admin, Students, Faculty | Define business vision, validate functional usability, ensure domain compliance |
| Engineering Stakeholders | Software Developers, UI/UX Designers, QA Engineers | Architect codebase, build responsive frontends, write unit tests, ensure high quality |
| Operations Stakeholders | DevOps Engineers, Database Administrators, Security Team | Provision cloud infrastructure, maintain database integrity, automate CI/CD pipelines |

---

## 4. Functional & Non-Functional Requirements

### Functional Requirements

**FR-01 Authentication:** Secure Role-Based Access Control (RBAC) for Admin, Librarian, Student, and Faculty.

**FR-02 Book Catalog Management:** Full CRUD operations for books, authors, categories, and physical shelf coordinates.

**FR-03 Circulation Engine:** Automated check-out and check-in processing with inventory increment/decrement.

**FR-04 Fine Engine:** Automated background processing calculating overdue penalties based on user tier.

**FR-05 Notification System:** Triggered email alerts for upcoming due dates and overdue fines.

### Non-Functional Requirements

**NFR-01 Security:** Password hashing (Bcrypt/Argon2), JWT token session management, and HTTPS encryption.

**NFR-02 Performance:** Sub-500ms API response time for search queries under concurrent user load.

**NFR-03 Availability & Scalability:** Containerized deployment targeting 99.9% uptime with horizontal pod autoscaling.

**NFR-04 Maintainability:** Infrastructure as Code (IaC) modularity and clear codebase separation.

---

## 5. Design Thinking Report

### Stage 1 — Empathize
The key user categories are:
- Students
- Faculty Members
- Librarians
- System Administrators

The objective is to understand users in their natural library workflow.

### Stage 2 — Define

**Core Problem Statement:**

"Library members experience severe operational delays in locating, reserving, borrowing, and returning literary resources due to inefficient manual tracking. Concurrently, administrative staff lack centralized real-time visibility, leading to unrecorded losses, reporting errors, and poor user satisfaction."

### Stage 3 — Ideate

High-value capabilities identified:
- Automated email/SMS reminders
- Dynamic QR code membership cards
- Mobile self-checkout
- Live inventory dashboards
- Automated penalty generation

### Stage 4 — Prototype

Low-fidelity wireframing of:
- Login Page
- User Search Portal
- Librarian Checkout Dashboard
- Admin Analytics Panel

### Stage 5 — Test

Paper prototypes are demonstrated to students and library staff to evaluate navigation flows, layout clarity, and task completion speed before frontend engineering.

---

## 6. IBM Design Thinking & IBM Loop

### IBM Design Thinking

#### Focus on User Outcomes
Shift technical goals to measurable human outcomes.

**Feature Goal:** Build a catalog database search query.

**Outcome Focus:** Enable students to locate and reserve any book in under 3 clicks.

#### Restless Reinvention
Treat continuous deployment as an ongoing refinement cycle, continuously analyzing production usage to improve UI layout and backend response speed.

#### Diverse Empowered Teams
Cross-functional collaboration among:
- Product Managers
- UX Designers
- Software Engineers
- QA
- Database Administrators
- DevOps Engineers

### IBM Loop Engine

```text
        ┌───────────────────────────┐
        │         OBSERVE           │
        │ Study interactions, logs  │
        │ and operational friction  │
        └─────────────┬─────────────┘
                      │
                      ▼
        ┌───────────────────────────┐
        │         REFLECT           │
        │ Analyze metrics, align    │
        │ priorities, re-evaluate   │
        └─────────────┬─────────────┘
                      │
                      ▼
        ┌───────────────────────────┐
        │           MAKE            │
        │ Design UI, write code,    │
        │ automate CI/CD deployment │
        └─────────────┬─────────────┘
                      │
                      └──────► OBSERVE
