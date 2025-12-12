# User Stories – Team To-Do Web App

This document captures the **functional requirements** of the Team To-Do Web App in the form of **user stories** with acceptance criteria.

It is structured around three main **Epics**:

- **EP-01** – Core Task Management  
- **EP-02** – Visibility & Filtering  
- **EP-03** – Team Experience & Adoption  



## 0. Legend & Conventions

- **Format:**  
  - *As a `<role>`, I want `<capability>` so that `<business/value outcome>`.*
- **Priority:**  
  - **M** – Must-have (MVP)  
  - **S** – Should-have (important, but can follow MVP)  
  - **C** – Could-have (nice to have)  
- **Status:** For a real project, this would track _Planned / In Progress / Done_.  
  Here, values are left as **Planned** to reflect the learning/project nature.
- **Estimates:** T-shirt sizing (S / M / L) as a rough complexity indicator.



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

1. A user can open a “Create Task” form from the main interface.
2. The form includes at least the following fields:
   - Title (mandatory)  
   - Description (optional)  
   - Assignee (mandatory)  
   - Due Date (mandatory)  
   - Status (defaulted to “To Do”)  
3. If a mandatory field is missing and the user attempts to save, a clear validation message is shown.
4. When the task is successfully created:
   - It appears in the task list/board immediately.
   - All entered values are correctly displayed.
5. The system confirms successful creation (e.g., via a toast message or clear visual feedback).

---

### US-02 – View Task List

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **see a list of all tasks** with key attributes so that **I understand what needs to be done and by whom**.

**Acceptance Criteria**

1. A default **“All Tasks” view** is available upon entering the app.
2. Each task in the list shows at least:
   - Title  
   - Assignee  
   - Status  
   - Due Date  
3. Tasks are displayed in a consistent order (e.g., by due date or creation date; defined for MVP).
4. If there are **no tasks**, an empty state message is shown (e.g., “No tasks yet. Create your first task.”).
5. The view updates automatically when tasks are created, edited or deleted.



### US-04 – Edit Task

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **edit an existing task** so that **I can keep information accurate when things change**.

**Acceptance Criteria**

1. A user can open an existing task in **edit mode** from the task list/board.
2. The user can modify:
   - Title  
   - Description  
   - Assignee  
   - Due Date  
   - Status  
3. Mandatory fields remain mandatory and are validated on save.
4. When changes are saved:
   - The updated task is immediately reflected in the task list/board.
   - No duplicate tasks are created.
5. If the user cancels editing, no changes are saved.



### US-06 – Update Task Status

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **change the status of a task** (To Do, In Progress, Done) so that **the board reflects the real progress of work**.

**Acceptance Criteria**

1. For each task, the user can update the **Status** field.
2. Available statuses for MVP:
   - To Do  
   - In Progress  
   - Done  
3. When status is updated:
   - The change is immediately reflected in the UI.
   - If a board view is used, the task moves to the appropriate column.
4. The status change is persisted (remains after refresh/reload).
5. No invalid status values can be selected.



### US-07 – Basic Validation & Data Quality

**Epic:** EP-01 – Core Task Management  
**Priority:** M  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **team member**, I want the system to **validate key fields** and show clear messages so that **I avoid saving incomplete or invalid tasks**.

**Acceptance Criteria**

1. The system validates at least:
   - Title is not empty  
   - Assignee is selected  
   - Due date is a valid date (not an invalid format)  
2. If validation fails:
   - The user sees a clear, human-readable message.
   - The error is shown near the problematic field or in a visible error area.
3. The system **prevents saving** a task until mandatory fields are corrected.
4. Validation happens both on **new task creation** and **task editing**.



### US-11 – Data Consistency Across Views

**Epic:** EP-01 – Core Task Management  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want **task updates to be consistently reflected across all views** so that **I can trust the data when reviewing work**.

**Acceptance Criteria**

1. If a user updates a task (title, status, assignee, due date), the change is visible:
   - In the main list view  
   - In any board/grouped view (if implemented)  
2. There is no situation where two different views show **conflicting information** for the same task.
3. After refresh/reload, all views show the same, up-to-date information.
4. If technical limitations exist (e.g., caching), they are documented and addressed in future iterations.



## 2. Epic EP-02 – Visibility & Filtering

> Improve visibility and prioritisation so the team can understand workload and focus.



### US-03 – Filter Tasks by Assignee

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **filter tasks by assignee** so that **I can quickly see who is working on what and identify overload**.

**Acceptance Criteria**

1. A filter control is available (e.g., dropdown) to select one or more assignees.
2. When one assignee is selected, the list/board shows only tasks assigned to that person.
3. When the filter is cleared, the view returns to showing all tasks.
4. Filter state is clearly visible (e.g., showing the active assignee).
5. Filtering and status updates work together (e.g., a filtered view still reflects real-time status changes).

---

### US-05 – Highlight Overdue & Upcoming Tasks

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **quickly identify overdue and near-due tasks** so that **I can follow up before deadlines are missed**.

**Acceptance Criteria**

1. The system identifies **overdue tasks** (due date in the past and status not “Done”).
2. The system identifies **upcoming tasks** (e.g., due in the next X days – a configurable or clearly stated timeframe).
3. Overdue tasks are visually distinguished (e.g., red date or icon).
4. Upcoming tasks are visually indicated (e.g., a subtle highlight or label like “Due soon”).
5. A simple way to filter or sort by due date is available (even basic sorting is acceptable for MVP).



### US-08 – Group Tasks by Status (Board View)

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team member**, I want to **see tasks grouped by status** (To Do, In Progress, Done) so that **I can quickly understand overall progress at a glance**.

**Acceptance Criteria**

1. A **board-style view** (or similar representation) is available where tasks are grouped by status.
2. Each column (or section) represents one of:
   - To Do  
   - In Progress  
   - Done  
3. Tasks appear in the correct column based on their current status.
4. When the status of a task is changed, the task moves to the corresponding column.
5. If there are no tasks in a column, an empty state message is shown.



### US-09 – Empty States & No-Results Behaviour

**Epic:** EP-02 – Visibility & Filtering  
**Priority:** C  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **user**, I want **clear empty states** when there are no tasks or when filters return no results so that **I am not confused by a blank screen**.

**Acceptance Criteria**

1. When there are **no tasks at all**, a meaningful message is displayed (e.g., “No tasks yet. Create your first task to get started.”).
2. When a filter is applied and **no tasks match**, a different message appears (e.g., “No tasks match the current filter.”).
3. The empty state provides a clear next step (e.g., a “Create Task” button).
4. Empty states appear consistently across list and board views.



## 3. Epic EP-03 – Team Experience & Adoption

> Support smooth onboarding, error handling and adoption to help teams use the tool consistently.



### US-10 – Clear Error Handling & Feedback

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** S  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **user**, I want **clear and human-friendly error messages** when something goes wrong so that **I understand what happened and what I should do next**.

**Acceptance Criteria**

1. If a task cannot be saved due to a technical issue, an error message is shown that avoids technical jargon.
2. Error messages:
   - Explain what went wrong at a high level.
   - Suggest a next action (e.g., “Please try again” or “Contact support”).
3. The app does not silently fail (no invisible errors).
4. Error states do not leave the UI in a broken or confusing state (e.g., partially created duplicates).



### US-12 – Simple Onboarding & Help (Optional)

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** C  
**Estimate:** S  
**Status:** Planned  

**User Story**  
As a **new user**, I want **a brief explanation of how to use the app** so that **I can start managing tasks without needing training**.

**Acceptance Criteria**

1. A short introductory text or help section is available (e.g., “How it works”).
2. The help content briefly explains:
   - How to create tasks  
   - How to update status  
   - How to filter and interpret the board/list  
3. The help can be accessed in one click from the main interface.



### US-13 – Basic Activity Transparency (Optional)

**Epic:** EP-03 – Team Experience & Adoption  
**Priority:** C  
**Estimate:** M  
**Status:** Planned  

**User Story**  
As a **team lead**, I want to **see when key changes were made to tasks** (e.g., status changes) so that **I can better understand recent activity**.

**Acceptance Criteria**

1. For MVP, this may be as simple as:
   - “Last updated” timestamp on each task.
2. The timestamp updates when key fields change (status, assignee, due date).
3. If a full activity log is not implemented, this limitation is clearly documented.



## 4. Non-Functional Notes (Cross-Cutting)

These are not user stories but important constraints to consider in implementation:

- **Performance:**  
  The app should respond quickly for typical team sizes (e.g., up to a few hundred tasks).

- **Usability:**  
  UI should be simple, with clear labels and minimal steps to create/update tasks.

- **Reliability:**  
  Basic safeguards should prevent data loss during typical usage.

- **Future Considerations:**  
  If the app were extended, stories around authentication, multi-team support, integrations and audit logging could be added.



## 5. Summary

This user story set is intentionally structured to reflect **real-world IT / digital delivery**:

- A clear mapping of **Epics → Stories → Acceptance Criteria**
- Balanced focus on **core functionality**, **visibility/management**, and **user experience/adoption**
- Enough detail that an engineering team could start estimation and implementation, with the Project Manager facilitating refinements and prioritisation.

In a real environment, these stories would be tracked in a tool such as **Jira**, linked to sprints, releases, and technical tasks. For this portfolio, they are captured here to illustrate my approach to **requirements engineering as an IT Project Manager**.
