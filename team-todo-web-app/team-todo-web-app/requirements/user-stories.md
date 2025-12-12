# User Stories – Team To-Do Web App

This document describes the **functional requirements** of the Team To-Do Web App in the form of **user stories** with acceptance criteria.

I created these stories as part of a self-initiated project to practise **requirements writing for IT projects** and to show how I think as an IT Project Manager / Delivery Lead.

User stories are grouped into three main **Epics**:

- **EP-01** – Core Task Management  
- **EP-02** – Visibility & Filtering  
- **EP-03** – Team Experience & Adoption  



## 0. Legend & Conventions

- **Story format:**  
  _As a `<role>`, I want `<capability>` so that `<value/outcome>`._
- **Priority:**
  - **M** – Must-have (MVP)  
  - **S** – Should-have (important, but can follow MVP)  
  - **C** – Could-have (nice to have)  
- **Status:** For this portfolio project, stories are marked as **Planned**, but are written as if they were going into a real backlog.
- **Estimate:** T-shirt sizing (S / M / L) as a rough complexity indicator.



## 1. Epic EP-01 – Core Task Management

> Enable team members to create, view, edit and complete tasks in a shared workspace.



### US-01 – Create Task

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **create a task** with a title, description, due date and assignee so that **responsibilities and expectations are clear**.

**Acceptance Criteria**

1. The user can open a “Create Task” form from the main interface.
2. The form includes at least:
   - Title (mandatory)  
   - Description (optional)  
   - Assignee (mandatory)  
   - Due Date (mandatory)  
   - Status (defaults to “To Do”)  
3. If a mandatory field is missing and the user tries to save, a clear validation message is shown.
4. When the task is successfully created:
   - It appears in the task list/board immediately.  
   - All entered values are displayed correctly.  
5. The user receives clear feedback that the task has been created (e.g., a short message or visual confirmation).



### US-02 – View Task List

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **see a list of all tasks** with key details so that **I know what needs to be done and by whom**.

**Acceptance Criteria**

1. A default **“All Tasks” view** is available when the user opens the app.
2. Each task in the list shows at least:
   - Title  
   - Assignee  
   - Status  
   - Due Date  
3. Tasks are displayed in a consistent order (e.g., by due date or creation date; this rule is defined for MVP).
4. If there are no tasks, an empty state message is shown (e.g., “No tasks yet. Create your first task.”).
5. When tasks are created, updated or deleted, the list view reflects the changes without the user needing to reload the page (if technically feasible).



### US-04 – Edit Task

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **edit an existing task** so that **I can keep information accurate when things change**.

**Acceptance Criteria**

1. The user can open any existing task in an **edit mode**.
2. The user can modify:
   - Title  
   - Description  
   - Assignee  
   - Due Date  
   - Status  
3. Mandatory fields remain mandatory and are re-validated on save.
4. When changes are saved:
   - The updated task is shown in the list/board with the new values.  
   - No duplicate task is created.  
5. If the user cancels editing, the original values remain unchanged.



### US-06 – Update Task Status

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **change the status of a task** (To Do, In Progress, Done) so that **the board reflects the real progress of work**.

**Acceptance Criteria**

1. Each task allows the user to update its **Status**.
2. For the MVP, allowed statuses are:
   - To Do  
   - In Progress  
   - Done  
3. When the status is changed:
   - The new status is shown immediately.  
   - In any board view, the task appears under the correct column.  
4. The status change is saved and persists after refresh/reload.
5. The user cannot select invalid or undefined statuses.



### US-07 – Basic Validation & Data Quality

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want the system to **validate key fields** and show clear messages so that **I avoid saving incomplete or broken tasks**.

**Acceptance Criteria**

1. The app validates at least:
   - Title is not empty  
   - Assignee is selected  
   - Due date is a valid date (no invalid format)  
2. If validation fails:
   - A clear error message is shown close to the field or in a visible area.  
3. The task is **not saved** until validation issues are fixed.
4. Validation is applied both when:
   - Creating a new task  
   - Editing an existing task  



### US-11 – Data Consistency Across Views

**Epic:** EP-01 – Core Task Management  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want **task updates to be shown consistently across all views** so that **I can trust the data when reviewing work**.

**Acceptance Criteria**

1. If a task is updated (title, status, assignee, due date), the change appears:
   - In the list view  
   - In any board or filtered view  
2. There is no situation where two views show different values for the same task.
3. After refresh/reload, all views show the same updated information.
4. If there are any technical limitations (e.g., refresh delays), these are documented and planned for improvement.



## 2. Epic EP-02 – Visibility & Filtering

> Help the team understand workload, priorities and deadlines more easily.



### US-03 – Filter Tasks by Assignee

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **filter tasks by assignee** so that **I can quickly see each person’s workload and avoid overload**.

**Acceptance Criteria**

1. A filter control is available to select one assignee (MVP).
2. When an assignee is selected, only tasks assigned to that person are shown.
3. When the filter is cleared, the view returns to showing all tasks.
4. The active filter is clearly indicated (e.g., the selected assignee is visible).
5. Status updates still appear correctly when a filter is active.



### US-05 – Highlight Overdue & Upcoming Tasks

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **quickly see which tasks are overdue or due soon** so that **I can follow up before things slip**.

**Acceptance Criteria**

1. Tasks with a due date in the past and status not “Done” are marked as **overdue**.
2. “Due soon” is defined for the MVP (e.g., tasks due in the next 3 days).
3. Overdue tasks are clearly highlighted (e.g., red date or a small icon).
4. “Due soon” tasks are also visibly marked, but less aggressively than overdue.
5. Sorting or filtering by due date is available (even basic sorting is sufficient for MVP).



### US-08 – Group Tasks by Status (Board View)

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **see tasks grouped by status** so that **I can understand overall progress at a glance**.

**Acceptance Criteria**

1. A board-style view (or similar) is available where tasks appear in columns by status:
   - To Do  
   - In Progress  
   - Done  
2. Tasks appear in the correct column based on their current status.
3. When a status is changed, the task moves to the appropriate column.
4. If a column has no tasks, an empty state message is displayed.
5. The board view and the list view are consistent (same tasks and statuses).



### US-09 – Empty States & No-Results Behaviour

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** C  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **user**, I want **clear empty states** when there are no tasks or no results for a filter so that **I understand what is happening and what to do next**.

**Acceptance Criteria**

1. When there are **no tasks at all**, a friendly message is shown (e.g., “No tasks yet. Create your first task.”).
2. When a filter returns **no matching tasks**, a different message is shown (e.g., “No tasks match the current filter.”).
3. The empty states suggest a next action (e.g., “Create Task” button).
4. Empty states behave consistently between list and board views.



## 3. Epic EP-03 – Team Experience & Adoption

> Make the app easier and safer to use so people actually adopt it.



### US-10 – Clear Error Handling & Feedback

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **user**, I want **clear and simple error messages** when something goes wrong so that **I know what happened and what I should do next**.

**Acceptance Criteria**

1. If saving or updating a task fails due to a technical issue, an error message is shown without technical jargon.
2. Error messages:
   - Explain the problem at a high level (e.g. “Something went wrong while saving this task”).  
   - Suggest a next step (e.g. “Please try again” or “Contact support if this continues”).  
3. The app does not silently fail; the user always gets feedback.
4. The UI stays in a usable state (no “half-saved” tasks visible).



### US-12 – Simple Onboarding & Help (Optional)

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** C  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **new user**, I want **a short explanation of how to use the app** so that **I can start using it without training**.

**Acceptance Criteria**

1. A “Help” or “How it works” section is available from the main interface.
2. It briefly explains:
   - How to create tasks  
   - How to change status  
   - How to filter tasks  
3. The content is short, direct and easy to understand.

---

### US-13 – Basic Activity Transparency (Optional)

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** C  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **see when a task was last updated** so that **I have a basic sense of recent activity**.

**Acceptance Criteria**

1. Each task shows a simple “Last updated” timestamp.
2. The timestamp is updated whenever key fields change (e.g. status, assignee, due date).
3. The format is readable (e.g. “Updated: 10 Dec 2025, 14:30”).
4. If a full activity log is not implemented, this simple timestamp acts as a minimum.

---

## 4. Non-Functional Notes (Cross-Cutting)

These are not full user stories, but important overall expectations:

- **Performance:**  
  The app should respond quickly for a typical small team (up to a few hundred tasks).

- **Usability:**  
  The interface should be simple and clean, with intuitive labels and actions.

- **Reliability:**  
  Normal usage should not lead to data loss.

- **Future Ideas:**  
  For a real roadmap, we could add stories around:
  - Authentication & multi-team support  
  - Integrations (Slack, email, calendar)  
  - Reporting and dashboards  



## 5. Summary

This set of user stories is designed to look and feel like a **real backlog** for a small internal product:

- Clear mapping of **Epics → Stories → Acceptance Criteria**  
- Balanced focus on core functionality, visibility and user experience  
- Enough detail that an engineering team could start estimation and refinement  

For this portfolio, the goal is to show how I would think and write as an **IT Project Manager** preparing a team for delivery.
