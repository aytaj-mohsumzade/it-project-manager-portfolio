# Sprint Plan – Team To-Do Web App

This document outlines the **planned sprint structure** for the Team To-Do Web App learning project.

I created this as part of my transition from general project management into **IT / digital project management**, to practise how I would plan and explain sprints in a real software project.



## 1. Delivery Approach

- **Approach:** Simple Scrum-style, iterative delivery  
- **Cadence:** 2-week sprints (this can be adjusted in a real project)  
- **Assumed Team Setup (for realism):**
  - 1–2 developers  
  - 1 QA (part-time)  
  - 1 Product Owner  
  - 1 Project Manager (my role)  
- **Release Strategy:**  
  - Deliver a small but usable **MVP** first  
  - Then add improvements in later sprints



## 2. Sprint Overview

| Sprint  | Focus Area                   | High-Level Outcome                                         |
|--------|-------------------------------|------------------------------------------------------------|
| 0      | Discovery & Shaping           | Problem and scope defined, backlog drafted, approach clear |
| 1      | Core Task Management (MVP)    | Users can create, view, edit and complete tasks            |
| 2      | Visibility & Filtering        | Users can filter tasks and understand progress more easily |
| 3      | Finishing & UAT Preparation   | App stabilised and ready for UAT with clear scenarios      |

This plan is intentionally small but realistic for a **simple internal tool**.



## 3. Sprint 0 – Discovery & Shaping

**Sprint Goal:**  
Make sure we really understand the problem, the users, and what the first version should do.

### 3.1 Key Activities

- Clarify **problem statement** and **business goals**
- Identify key **personas** (e.g. Team Lead, Team Member)
- Map core **workflows**:
  - Creating a task  
  - Updating task status  
  - Reviewing workload as a lead
- Draft initial **epics and user stories**
- Define what is **MVP** vs. “nice to have later”
- Note high-level **non-functional needs** (basic usability, performance)

### 3.2 Example Deliverables

- Problem and goals captured in `README.md`
- Initial backlog in `requirements/user-stories.md`
- High-level scope and constraints (in README or requirements)
- Initial **risk and assumptions log** in `planning/risk-log.md`
- Simple solution sketch (diagram or text)

### 3.3 Out of Scope for Sprint 0

- Implementation and coding  
- Pixel-perfect UI design  
- Deep details for future features (beyond MVP)



## 4. Sprint 1 – Core Task Management (MVP)

**Sprint Goal:**  
Deliver the first working version where a team can **create and manage basic tasks** in one place.

### 4.1 Planned User Stories

From `requirements/user-stories.md`:

- **US-01 – Create Task**  
- **US-02 – View Task List**  
- **US-04 – Edit Task**  
- **US-06 – Update Task Status**  
- **US-07 – Basic Validation & Data Quality**

These stories together form the **minimum usable app**.

### 4.2 Non-Functional Focus

- Basic responsiveness (comfortable on a laptop browser)  
- Reasonable performance for a small number of tasks  
- Clear error/validation messages when required fields are missing

### 4.3 Example Tasks (for each story)

Typical tasks under these stories could include:

- Confirm acceptance criteria  
- Design simple UI for:
  - Task form  
  - Task list
- Implement storage and retrieval of tasks (in a real project)  
- Implement validation rules  
- Do basic checks (happy path + obvious edge cases)  
- Update documentation (screenshots, test notes, etc.)

### 4.4 Expected Deliverables

- Working UI to:
  - Create tasks  
  - See a list of tasks  
  - Edit tasks  
  - Change status  
- Updated `user-stories.md` (with any refined acceptance criteria)  
- Initial test cases in `uat/testing-checklist.md` for these MVP stories  
- Short sprint summary (optional, e.g. `planning/sprint-1-notes.md`)



## 5. Sprint 2 – Visibility & Filtering

**Sprint Goal:**  
Make it easier for the team to **understand workload and priorities** at a glance.

### 5.1 Planned User Stories

From `requirements/user-stories.md`:

- **US-03 – Filter Tasks by Assignee**  
- **US-05 – Highlight Overdue & Upcoming Tasks**  
- **US-08 – Group Tasks by Status (Board View)**  
- **US-09 – Empty States & No-Results Behaviour** (if capacity allows)

### 5.2 Non-Functional Focus

- Clear, simple **UX**: the user should understand the screen without training  
- Visual hints for status and urgency  
- Consistent behaviour between list and board views

### 5.3 Example Tasks

- Add filter controls (e.g. assignee, status)  
- Implement logic for overdue / due-soon highlighting  
- Create or refine board view (columns by status)  
- Design and implement meaningful empty states  
- Update testing checklist for filtering and visibility scenarios  
- Add new screenshots to README (optional but helpful)

### 5.4 Expected Deliverables

- Enhanced view(s) where:
  - Tasks can be filtered  
  - Overdue / near-due tasks are visible  
  - Tasks can be seen grouped by status  
- Updated UAT / test checklist including these behaviours  
- Sprint 2 notes / retrospective (key learnings and ideas)



## 6. Sprint 3 – Finishing & UAT Preparation

**Sprint Goal:**  
Stabilise the MVP, tidy up edge cases, and prepare a **version that is ready for UAT**.

### 6.1 Planned Work Items

From `requirements/user-stories.md` and additional tasks:

- **US-10 – Clear Error Handling & Feedback**  
- **US-11 – Data Consistency Across Views**  
- Technical clean-up tasks (bug fixes, usability tweaks)  
- UAT-related tasks:
  - Finalise test scenarios  
  - Define UAT entry/exit criteria  
  - Document known limitations

### 6.2 UAT Preparation Activities

- Finalise **testing checklist** in `uat/testing-checklist.md`  
- Optionally add a short **UAT script** or scenarios (e.g. typical team workflows)  
- Define simple UAT criteria, for example:
  - Entry: MVP stories implemented, no critical known defects  
  - Exit: Key workflows successfully tested by UAT users, no critical open issues

### 6.3 Expected Deliverables

- Stabilised MVP ready for UAT (conceptually)  
- Updated documentation of:
  - Known issues and limitations  
  - UAT scope and outcomes (if executed)  
- Draft release notes in `releases/release-notes-v1.0.md`:
  - What is included in v1.0  
  - Known limitations  
  - Next-step ideas



## 7. Definitions of Ready & Done (DoR / DoD)

These definitions help keep the work clear and realistic.

### 7.1 Definition of Ready (Story Level)

A story is **Ready** when:

- The user, goal and benefit are clear  
- Acceptance criteria are written and testable  
- Dependencies are identified or consciously ignored for MVP  
- The story is small enough to fit into one sprint

### 7.2 Definition of Done (Story Level)

A story is **Done** when:

- The behaviour is implemented  
- Acceptance criteria pass  
- Basic tests have been executed  
- UI is checked for obvious issues  
- Relevant documentation is updated (if needed)

### 7.3 Definition of Done (Sprint / Increment)

A sprint is **Done** when:

- All committed stories are either:
  - Done (by story DoD), or  
  - Explicitly moved out with a reason
- A short **sprint summary** and **lessons learned** are captured  
- The increment could reasonably be shown to stakeholders or UAT users



## 8. Notes

This sprint plan is part of a **practice project** and is meant to show how I would:

- Break down delivery into realistic sprints  
- Balance MVP scope vs. “nice to have” features  
- Prepare UAT and release activities  

In a real company, I would adapt this plan to the **team’s capacity, tech stack and existing processes**, but the core structure would be similar.
