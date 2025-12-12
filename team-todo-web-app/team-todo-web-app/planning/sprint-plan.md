# Sprint Plan – Team To-Do Web App

This document outlines the **planned sprint structure** for the Team To-Do Web App learning project.  
It is written as if it were a real-world delivery, using a lightweight Scrum-style approach.



## 1. Delivery Approach

- **Methodology:** Scrum-inspired, iterative delivery
- **Cadence:** 2-week sprints (timebox can be adjusted in a real context)
- **Team Size (assumed):** 1–2 developers, 1 QA (part-time), 1 Product Owner, 1 Project Manager
- **Release Strategy:** Deliver a usable **MVP** early, then iterate with incremental improvements



## 2. Sprint Overview

| Sprint  | Focus Area                    | High-Level Outcome                                        |
|--------|--------------------------------|-----------------------------------------------------------|
| 0      | Discovery & Shaping            | Problem framed, backlog drafted, basic architecture outlined |
| 1      | Core Task Management (MVP)     | Users can create, view, update and complete tasks         |
| 2      | Visibility & Filtering         | Users can filter tasks and have improved UX               |
| 3      | Hardening & UAT Preparation    | Stabilised app, edge cases addressed, UAT-ready build     |



## 3. Sprint 0 – Discovery & Shaping

**Goal:**  
Establish a clear understanding of the problem, users, and scope; draft an initial product backlog and delivery approach.

### 3.1 Key Activities

- Clarify **problem statement** and **business goals**
- Identify key **personas** (e.g. Team Lead, Team Member)
- Map **core workflows**:
  - Creating a task
  - Updating status
  - Reviewing workload
- Draft initial **epics and user stories**
- Define **MVP scope** vs. future enhancements
- Outline **non-functional expectations** at a high level (usability, performance, reliability)

### 3.2 Example Deliverables

- Problem & goals section in `README.md`
- Initial backlog in `requirements/user-stories.md`
- High-level scope and constraints (in README or requirements)
- Initial **RAD log** (Risks, Assumptions, Dependencies) in `planning/risk-log.md`
- High-level solution sketch (can be a simple diagram stored in `/diagrams` or embedded in docs)

### 3.3 Out-of-Scope for Sprint 0

- Any implementation work
- Detailed UI design (can be rough sketches only)
- Non-MVP features (tracked but not elaborated fully)



## 4. Sprint 1 – Core Task Management (MVP)

**Sprint Goal:**  
Deliver a first working version where a single team can **create and manage tasks** with owner, due date, and status.

### 4.1 Scope (User Stories)

Suggested user stories for Sprint 1:

- **US-01 – Create Task**  
  As a team member, I want to create a task with a title, description, due date and assignee so that responsibilities are clear.

- **US-02 – View Task List**  
  As a team member, I want to see a list of all tasks with key details so that I understand what needs to be done.

- **US-04 – Edit Task**  
  As a team member, I want to edit a task when requirements change so that the information stays accurate.

- **US-06 – Update Task Status**  
  As a team member, I want to change the status of a task (To Do, In Progress, Done) so that the board reflects reality.

- **US-07 – Basic Validation**  
  As a team member, I want to be prevented from saving tasks with missing mandatory fields so that data quality is maintained.

*(Story IDs should match those maintained in `user-stories.md`.)*

### 4.2 Non-Functional Focus

- Basic responsiveness (works comfortably on a laptop browser)
- Reasonable performance for a small set of tasks (no noticeable lag)
- Clear error messages when required fields are missing

### 4.3 Example Tasks (per Story)

For each story, typical tasks could include:

- Clarify acceptance criteria
- Design minimal UI for task form and list
- Implement backend logic (if applicable)
- Wire UI to data (task creation and storage)
- Basic unit / functional testing
- Update documentation (screenshots, notes)

### 4.4 Expected Deliverables

- Functional UI to:
  - Create a task
  - View a list of tasks
  - Edit basic task fields
  - Change task status
- Updated requirements in `user-stories.md` with acceptance criteria
- Initial test cases listed in `uat/testing-checklist.md` (for stories in scope)
- Sprint 1 summary in a separate log (e.g. `planning/sprint-1-notes.md` – optional)



## 5. Sprint 2 – Visibility & Filtering

**Sprint Goal:**  
Improve **visibility and usability** by allowing users to filter tasks and better understand workload.

### 5.1 Scope (User Stories)

Suggested user stories for Sprint 2:

- **US-03 – Filter by Assignee**  
  As a team lead, I want to filter tasks by assignee so that I can quickly see each person’s workload.

- **US-05 – Highlight Overdue / Upcoming Tasks**  
  As a team lead, I want to see tasks that are overdue or due soon so that I can follow up proactively.

- **US-08 – Status-Based View**  
  As a team member, I want to see tasks grouped by status (To Do, In Progress, Done) so that progress is visually clear.

- **US-09 – Empty States & Basic UX Improvements**  
  As a user, I want the app to clearly show when there are no tasks or no results so that I am not confused.

### 5.2 Non-Functional Focus

- UX clarity: intuitive filters and clear labels
- Visual hierarchy: statuses and due dates easily noticeable
- Basic accessibility considerations (legible fonts, clear contrasts)

### 5.3 Example Tasks

- Implement filtering logic (by assignee, by status)
- Add visual cues for overdue / upcoming tasks
- Design and implement empty state messages
- Update test scenarios to cover filtering and visibility behaviour
- Update README with new screenshots (optional but recommended)

### 5.4 Expected Deliverables

- Enhanced task list / board view:
  - Filter by assignee and status
  - Highlight overdue / near-due tasks
- Updated test checklist including visibility and filtering
- Sprint 2 notes / retrospective (lessons learned, improvement ideas)

---

## 6. Sprint 3 – Hardening & UAT Preparation

**Sprint Goal:**  
Stabilise the product, address edge cases, and prepare a **UAT-ready build** with clear test scenarios.

### 6.1 Scope (User Stories / Work Items)

In addition to any remaining stories, Sprint 3 focuses on:

- **US-10 – Error Handling & Edge Cases**  
  As a user, I want clear messages if something goes wrong so that I know what to do next.

- **US-11 – Basic Data Consistency**  
  As a team lead, I want to be sure task updates are correctly reflected across views so that I can rely on the board.

- Technical tasks:
  - Review and fix known bugs
  - Tidy up any obvious UX issues

- UAT-related tasks:
  - Prepare UAT checklist and instructions
  - Identify UAT scenarios based on real workflows
  - Define simple acceptance criteria for UAT sign-off

### 6.2 UAT Preparation Activities

- Finalise **testing checklist** in `uat/testing-checklist.md`
- Create a simple **UAT scenario document** (can be part of the checklist or separate file)
- Define **UAT entry and exit criteria**, e.g.:
  - Entry: All critical and high defects resolved; core stories implemented  
  - Exit: No open critical defects; key workflows validated by UAT participants

### 6.3 Expected Deliverables

- Stabilised MVP build (conceptually)
- Updated documentation of:
  - Known issues (if any)
  - UAT scope and scenarios
- Draft `releases/release-notes-v1.0.md` describing:
  - Features delivered
  - Known limitations
  - Recommended next steps



## 7. Definitions of Ready & Done (DoR / DoD)

Even in a small project, having clear criteria improves predictability and quality.

### 7.1 Definition of Ready (Story Level)

A story is “Ready” when:

- The **user role**, **goal** and **benefit** are clear
- Acceptance criteria are written in simple, testable form
- Dependencies are identified (or explicitly deferred)
- Story size is reasonable for a single sprint (if not, it is split)

### 7.2 Definition of Done (Story Level)

A story is “Done” when:

- Implementation is complete and builds successfully
- Acceptance criteria are met
- Basic tests for the story have been executed
- UI is reviewed for obvious usability issues
- Relevant documentation (if any) is updated

### 7.3 Definition of Done (Sprint / Increment)

A sprint is “Done” when:

- All committed stories are either:
  - Done (by story DoD), or  
  - Explicitly moved back to the backlog / next sprint with clear rationale
- A short **sprint summary** and **lessons learned** are captured
- The increment is in a state that could be shown to stakeholders / UAT users



## 8. Notes

This sprint plan is intentionally detailed to reflect how I would plan and structure work as an **IT Project Manager / Delivery Lead**.  
In a real environment, the precise scope per sprint would be adjusted based on:

- Team capacity and skills  
- Technical constraints discovered during implementation  
- Feedback from early users and stakeholders  

For the purposes of this portfolio, the goal is to demonstrate **structured thinking, realistic scoping, and clear communication** of the delivery plan.
