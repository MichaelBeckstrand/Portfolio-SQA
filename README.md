# Michael Beckstrand — QA Portfolio

- [About Me](#about-me)
- [Resume](#resume)
- [Skills](#skills)
- [Tools](#tools)
- [Certifications & Education](#certifications--education)
- [Examples of My Work](#examples-of-my-work)
  - [Test Plan — theCaseWork Capstone](#test-plan--thecasework-capstone)
  - [Bug Reports](#bug-reports)
  - [Feature Requests](#feature-requests)
  - [Automation](#automation)

---

## About Me

I'm a detail-oriented QA specialist based in Lehi, UT with a background that spans software quality assurance, electronics testing, and production QC. I graduated from Mountainland Technical College's Software Quality Assurance Program and hold a Google Cybersecurity Professional Certificate, with CompTIA A+ in progress.

My approach to QA combines structured test design with practical hands-on experience: I write clear, reproducible test cases, document defects thoroughly, and think carefully about what should and shouldn't be automated. I'm comfortable working across manual and automated testing, bug tracking tools, and API testing environments.

I'm actively looking to apply these skills in a professional QA role where I can contribute to product quality from day one.

---

## Resume

📄 [Download Resume (PDF)](./Michael_Beckstrand_Resume.pdf) 

Or view highlights below:

**Recent Experience**
- **Epic Dental Studios** — 3D Printer Technician (Jan 2025 – Present)
- **Jellyfish Lighting** — Production Assembler / QC (Jun 2023 – Jan 2025)
- **iRecertify** — Electronics Technician (Nov 2022 – Jul 2023)
- **Boostability** — Website QA Specialist (Jun 2021 – Jul 2021)

---

## Skills

**Manual Testing**
- Perform functional, negative, boundary, and UI/interaction testing on web applications
- Design test cases from feature requirements; choose manual vs. automated based on test type and risk
- Experienced with exploratory testing and edge case identification

**Test Documentation**
- Write structured test cases with clear preconditions, steps, expected results, and reasoning
- Author detailed bug tickets including severity ratings, reproduction steps, and expected vs. actual results
- Produce test plans covering scope, success criteria, timelines, and resource allocation

**Automation**
- Write and maintain automated test scripts using WebdriverIO (JavaScript)
- Evaluate which tests benefit from automation vs. manual verification (e.g., visual/timer tests stay manual; predictable logic tests are scripted)
- Experience with a full capstone automation suite covering CRUD, negative, security, and data persistence tests

**API Testing**
- Familiar with REST API concepts and manual API validation using Postman

**Security Testing**
- Verified unauthenticated access prevention (redirect-to-login on protected routes)
- Familiar with SIEM tools and security hardening concepts from Google Cybersecurity Certificate

**Defect Detection & QC**
- Electronics grading and defect documentation (iRecertify, Jellyfish Lighting)
- Production QC inspection and non-conformance reporting (X2 Development Group)

---

## Tools

| Category | Tools |
|---|---|
| **Test Management** | Jira, Azure DevOps (dev.azure.com) |
| **Automation** | WebdriverIO, JavaScript |
| **API Testing** | Postman |
| **Bug Tracking** | Jira, Azure DevOps |
| **Languages** | JavaScript, SQL |
| **OS / CLI** | Linux / Command Line |
| **Browsers** | Google Chrome (DevTools) |
| **Other** | VS Code, Google Suite, Microsoft Word |

---

## Certifications & Education

- **Software Quality Assurance Certification** — Mountainland Technical College, Lehi UT
- **theCaseWork Externship Certificate**
- **Google Cybersecurity Professional Certificate**
- **CompTIA A+** *(In Progress)*
- **Culinary Arts Certificate** — MTEC

---

## Examples of My Work

### Test Plan — theCaseWork Capstone

**Project:** [theCaseWork](https://app.thecasework.com) — a case management platform for legal/professional services firms

**Timeline:** April 20 – May 8, 2026

**Scope:** 4 feature areas — Engagements, Dashboard My Tasks, Case Tasks, and Security

**Success Criteria:**

| Category | Criterion |
|---|---|
| Automation | >80% of Engagement & Task tests automated |
| Security | 100% pass rate on unauthorized access test |
| Reliability | Successful CRUD validation across all task modules |
| Performance | No UI glitches under standard load |

**Test Cases Written: 34 total** across 4 modules (mix of automated and manual)

#### Engagement Tests (7 cases)

| ID | Description | Type | Method |
|---|---|---|---|
| MTQA-5301 | Updating engagement title | Functional (Positive/CRUD) | Automated |
| MTQA-5305 | Adding signatures | Functional (Positive) | Automated |
| MTQA-5366 | Adding templates | Functional (Positive) | Automated |
| MTQA-5422 | Updating signatures | Functional (Positive/CRUD) | Manual |
| MTQA-5530 | Excessive characters in text box | Boundary | Manual |
| MTQA-5564 | Adding signature without selecting user | Functional (Negative) | Automated |
| MTQA-5565 | Adding signature without selecting contact | Functional (Negative) | Automated |

#### Dashboard "My Tasks" Tests (13 cases)

| ID | Description | Type | Method |
|---|---|---|---|
| MTQA-5367 | Adding task | Functional (Positive) | Automated |
| MTQA-5368 | Editing task | Functional (Positive/CRUD) | Automated |
| MTQA-5372 | Timer functionality | Functional (Positive) | Manual |
| MTQA-5373 | Completing a task | Functional (Positive) | Automated |
| MTQA-5374 | Closing a task | Functional (Positive) | Automated |
| MTQA-5399 | Adding notes | Functional (Positive/Boundary) | Automated |
| MTQA-5409 | My Tasks filter functionality | UI / Interaction | Manual |
| MTQA-5470 | Adding task with past due date | Functional (Negative) | Automated |
| MTQA-5531 | Adding invalid entries to timer | Functional (Negative) | Automated |
| MTQA-5535 | Double clicking tasks | UI / Interaction | Manual |
| MTQA-5669 | Adding task without required fields | Functional (Negative) | Automated |
| MTQA-5704 | Adding task and not saving | Functional (Negative) | Automated |
| MTQA-5705 | Adding task with additional entries | Functional (Positive) | Automated |
| MTQA-5706 | Editing task and not saving | Functional (Negative) | Automated |

#### Case Tasks Tests (13 cases)

Mirrors the Dashboard suite within the case-specific view — same test types applied to the in-case task module to validate consistent behavior across both contexts.

[View case task IDs: MTQA-5379, 5382, 5384, 5386, 5387, 5405, 5473, 5533, 5534, 5536, 5701, 5702, 5703]

#### Security Test (1 case)

| ID | Description | Type | Method |
|---|---|---|---|
| MTQA-5392 | Unauthenticated access to protected case URL | Security | Automated |

🔗 [Capstone Automation Repository](https://github.com/MichaelBeckstrand/Capstone)

---

### Bug Reports

**12 bug reports** filed during the theCaseWork capstone externship. All were assigned to the dev team and resolved as **Completed**.

A selection of notable bugs:

---

**BUG 637 — [Case/Dashboard] Timer input accepts non-numeric text, causing page crash**
> **Severity:** Medium | **Status:** Fixed

Entering non-numeric characters into the timer's hours field was accepted by the system. When the timer was subsequently started, the page crashed. After refreshing, the timer remained unresponsive.

- **Expected:** Input restricted to valid numeric values; timer functions correctly
- **Actual:** Non-numeric text accepted; timer initiation crashes the page
- **Reproduction:** Click the + icon on a task → enter text in hours box → Submit → click Play

---

**BUG 638 — [Case/Engagements] Excessive text input causes page to become unresponsive**
> **Severity:** Medium | **Status:** Fixed

Engagement text boxes had no character limit. Entering thousands of words caused the text to become unreadable, and at extreme lengths the entire page became unresponsive.

- **Expected:** Character limit enforced or UI gracefully handles large input
- **Actual:** Page becomes unresponsive at high character counts

---

**BUG 602 — [Case/Engagements/Signatures] Same contact signature can be added infinitely; deleting one removes all**
> **Severity:** Medium | **Status:** Fixed

The system allowed the same client contact signature to be added multiple times. Because the system treated duplicates as the same entity, deleting one instance removed all of them simultaneously.

- **Expected:** Contact signature unavailable for re-selection once added; deletions are independent
- **Actual:** Infinite duplicate additions allowed; deleting one clears all identical entries

---

**BUG 663 — [Case/Add Task] Automation bypasses milestone requirement**
> **Severity:** Medium | **Status:** Fixed

Manual task creation correctly enforced milestone selection. However, the automated test could "brute force" past this validation, allowing tasks to be saved without a milestone. Caught during automation development — demonstrates proactive thinking about automation reliability.

---

**BUG 627 — [Case/Task/Notes] Notes overlap when word count limit is reached**
> **Severity:** Not Specified | **Status:** Fixed

Adding a maximum-length note followed immediately by a shorter one caused the two notes to visually overlap, rendering both unreadable.

---

**Additional bugs filed (all resolved):**
- BUG 660 — Milestones field interactable but rejects text input
- BUG 640 — Double-clicking timer icons opens unrelated edit dialog
- BUG 603 — "Select Contacts" button always active regardless of selection state
- BUG 549 — Misspelling in storage limit error message ("assiatance")
- BUG 592 — Address placeholder text typo ("addres 1")
- BUG 540 — Settings page not scrollable when browser is minimized
- BUG 554 — Client text fields overflow UI when over-filled

---

### Feature Requests

**6 feature requests** submitted during the externship.

| ID | Title | Status |
|---|---|---|
| FEATURE 639 | Require mandatory fields in Engagements (title + signatures) | Proposed |
| FEATURE 636 | Make Tasks & Engagements tabs scrollable at high zoom (accessibility) | Under Consideration |
| FEATURE 555 | Integrate "Add Case Type" option directly into dropdown | Planned |
| FEATURE 550 | Streamline invoice creation UI with consistent Add button placement | Under Consideration |
| FEATURE 552 | Input validation for address, phone, and contact fields | Closed |
| FEATURE 545 | Visible storage usage indicator before 1GB limit is reached | Closed (Accepted) |

---

### Automation

All automation was written in **JavaScript using WebdriverIO** as part of the capstone project.

**What was automated:**
- Full CRUD flows for tasks (add, edit, complete, close) across Dashboard and Case views
- Negative tests: missing required fields, invalid timer input, unsaved changes persistence
- Security test: unauthenticated redirect to login
- Engagement tests: title updates, signature validation, template application

**What was kept manual** (and why):
- Timer UI — visual verification of graphics and animations
- Filter interactions — confirming filtered data "looks" correct
- Double-click behavior — unpredictable rapid human interactions
- Signature overwrite — checking for UI ghosting artifacts

🔗 [View Capstone Repository on GitHub](https://github.com/MichaelBeckstrand/Capstone)

---

*Last updated: May 2026*
