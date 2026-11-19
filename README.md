Project : My Vidyon Intelligent Onboarding Platformgit
# Project Name
A brief 1–2 sentence description of what your project does.

## Folder Structure
- `docs/` – System architecture diagrams and documentation
- `frontend/` – User interface components, pages, and styles
- `backend/` – Server logic, API routes, and database models
- `tests/` – Application test files

## Core Modules
1. **Frontend Module:** Handles user interface, forms, and navigation.
2. **Authentication Module:** Manages user registration, login, and security.
3. **Backend API Module:** Processes requests and business logic.
4. **Database Module:** Stores and retrieves user and application data.

Requirements

Functional: The platform lets applicants register and log in under role-based access (Applicant, Reviewer, Admin). They complete a multi-step onboarding form that auto-saves progress, and upload documents against a checklist with file validation and secure storage. OCR and AI then extract key details from the documents and flag mismatches with the form data. An embedded AI assistant answers applicant questions. Reviewers can approve, reject or request changes on each application, and the system sends email alerts, shows status tracking and keeps an audit trail of key actions.

Non-functional: The platform should be:

Secure: HTTPS, hashed passwords, private storage and role-based authorization.
Fast: pages load within about 3 seconds, and OCR/AI results come back within about 15 seconds.
Scalable and reliable: it handles many concurrent applicants without losing saved drafts.
Usable and responsive: a simple guided UI that works on mobile and desktop.
Maintainable and auditable: modular TypeScript code with tests, and time-stamped logs for critical actions.

User expectations:

Applicants want a guided process, the option to save and resume, quick feedback on wrong uploads and instant answers from the AI assistant.
Reviewers want one dashboard with form data, documents and AI flags side by side.
Admins want control over users, roles and the document checklist.
Modules
Module	Responsibility
M1. Authentication & Access Control	Sign-up, login, verification, role-based protection
M2. Onboarding Wizard	Multi-step form, draft saving, progress and submission
M3. Document Management	Checklist, upload validation, secure storage
M4. OCR & AI Processing	Text extraction, field extraction, mismatch flags
M5. AI Assistant	Chat helper for applicant questions
M6. Reviewer & Admin Dashboard	Review workflow, user and checklist management
M7. Notification Service	Email alerts on status changes
M8. Audit & Logging	Action logs and admin log viewer
M9. Database & Storage Layer	PostgreSQL schema, Supabase storage, access policies
M10. Testing, Deployment & Docs	Tests, cloud deployment, README

Build order: M9, then M1, M2, M3, M6, M7, M8, M4, M5 and finally M10.

Priorities:

Must Have: login, onboarding form, document upload, reviewer dashboard and status tracking.
Should Have: OCR, AI validation, email alerts, audit trail and admin management.
Could Have: AI Q&A assistant, analytics, multi-language support and bulk review.