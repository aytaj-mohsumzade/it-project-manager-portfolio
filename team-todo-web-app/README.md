# Team To-Do Web App – End-to-End Delivery Case Study (Self-Initiated)

## 0. Executive Summary

This repository documents an end-to-end **product delivery case study** for a lightweight **Team To-Do Web Application**.

The objective of this project was to simulate a realistic delivery scenario and demonstrate my capabilities as an **IT Project Manager / Delivery Lead** across the full lifecycle:

- Product discovery and business case
- Requirements engineering (functional & non-functional)
- Agile delivery planning (roadmap, sprints, releases)
- Risk, dependency and stakeholder management
- Quality, UAT and release management
- Metrics, outcomes and continuous improvement

This is a **self-initiated learning project**, not a commercial engagement, designed to mirror how I would structure and lead a real-world digital product delivery.

---

## 1. Business Context & Problem Statement

Small teams often manage tasks across fragmented tools (chat, email, personal notes), creating:

- Low visibility into who owns what and by when  
- No single source of truth for work in progress  
- Difficulty prioritising and following up  

**Business Goal:**  
Design and deliver a simple web application that provides a **shared, transparent task board** for small teams, with minimal onboarding and operational overhead.

**Primary Outcome Sought:**  
Enable teams to track tasks in a single place, with clear ownership and status, improving **predictability** and **accountability**.

---

## 2. Objectives & Success Metrics

### 2.1 Objectives

1. Provide a **centralised view** of all team tasks, including ownership and due dates.
2. Enable team members to **create, update and complete tasks** with minimal friction.
3. Establish a **lightweight delivery model** (backlog → sprints → releases) aligned with agile best practices.
4. Demonstrate **end-to-end IT project management** including planning, risk management, and release governance.

### 2.2 Example Success Metrics (for a real implementation)

*(For this simulated project, these are target metrics I would use if the app were deployed to a real team.)*

- ✅ Adoption: 80% of team members actively using the app weekly after 4 weeks.
- ✅ Visibility: 100% of active tasks have an owner and due date.
- ✅ Flow: 20–30% reduction in “hidden work” (tasks discussed in chat but not tracked).
- ✅ Delivery: 90% of stories committed to a sprint are completed within the sprint after two iterations of stabilisation.

---

## 3. Scope, Constraints & Assumptions

### 3.1 In Scope

- Core web UI for:
  - Creating tasks (title, description, assignee, due date, status)
  - Viewing tasks in a list or basic board style (e.g., To Do / In Progress / Done)
  - Editing and completing tasks
- Basic filtering (e.g., by status, assignee)
- Minimal authentication approach (e.g., single team, simplified access assumptions)
- Documentation of:
  - Requirements & user stories
  - Backlog and sprint plan
  - Testing / UAT approach
  - Release notes and retrospective

### 3.2 Out of Scope (Initial Release)

- Native mobile application
- Complex role-based permissions
- Advanced reporting or analytics
- Integrations (Slack, email, calendar)
- SSO / enterprise identity integration

### 3.3 Key Constraints (Simulation)

- No dedicated development team: the focus is on **project management process and artefacts**, not on writing production-grade code.
- Tools used are limited to easily accessible options (GitHub, spreadsheets, diagrams, etc.).

---

## 4. Stakeholders, Roles & Governance

### 4.1 Example Stakeholder Map (for a real deployment)

| Role                      | Example Stakeholder        | Interest / Responsibility                                 |
|---------------------------|----------------------------|----------------------------------------------------------|
| Sponsor                   | Head of Operations         | Improve team visibility and on-time task delivery        |
| Product Owner             | Team Lead                  | Owns backlog, prioritisation and acceptance of features  |
| Delivery / IT PM          | Myself                     | Planning, coordination, risk/issue management            |
| Engineering Lead          | Senior Developer (hypothetical) | Technical direction, estimates, implementation      |
| QA / UAT Representatives  | 2–3 Key Team Members       | Validate functionality against real workflows            |
| Support / Operations      | Team Coordinator           | Feedback on usability and day-to-day adoption            |

### 4.2 Governance & Cadence

For this project, I defined a **lightweight governance model**, which in a real setting would include:

- Weekly **Planning / Refinement** (backlog review, prioritisation, estimates)
- Bi-weekly **Sprint Review & Demo**
- Bi-weekly **Retrospective** focusing on flow, bottlenecks, and communication
- Ad hoc **Risk / Issue reviews** when needed

In this simulated project, these ceremonies are documented as structured notes and checklists.

---

## 5. Solution Overview

### 5.1 Functional Overview

The Team To-Do Web App supports:

- **Task Management**
  - Create, update and delete tasks
  - Assign tasks to team members
  - Set and update due dates
  - Track status (To Do / In Progress / Done)

- **Task Visibility**
  - See all tasks in a consolidated view
  - Filter by status and assignee
  - Optionally group by due date

### 5.2 Non-Functional Considerations (Conceptual)

For a production implementation, I would consider:

- **Usability:** Minimal clicks to create/edit tasks, clear visual status indicators.
- **Performance:** Fast page load and task updates for typical team size.
- **Reliability:** Basic error handling; tasks are not lost on refresh.
- **Security:** Appropriate data access controls if used across multiple teams.
- **Scalability:** Ability to scale from a single team to multiple teams in future iterations.

---

## 6. Delivery Approach

### 6.1 Methodology

I used a **Scrum-inspired iterative approach**, tailored for a small, focused product:

- Product backlog maintained as user stories with acceptance criteria.
- Timeboxed iterations (**sprints**) with clear sprint goals.
- Emphasis on early usable increments (MVP first, then enhancements).

### 6.2 High-Level Timeline (Simulated)

- **Discovery & Shaping (Iteration 0):**
  - Problem framing, personas, key workflows
  - Draft backlog and high-level architecture

- **Sprint 1 – MVP Task Management:**
  - Basic task CRUD (Create, Read, Update, Delete)
  - Single list view with status and due date

- **Sprint 2 – Usability & Filtering:**
  - Filter by status and assignee
  - Small UX refinements based on hypothetical feedback

- **Sprint 3 – Hardening & UAT Readiness:**
  - Edge cases, validation, better empty states
  - UAT scenario preparation, bug triage

Detailed sprint breakdown is documented in:  
`team-todo-web-app/planning/sprint-plan.md` (planned content).

---

## 7. Requirements & User Stories

Requirements and user stories are maintained in:

- `team-todo-web-app/requirements/user-stories.md`

The backlog is structured into:

- **Epics**
  - EP-01 Core Task Management
  - EP-02 Visibility & Filtering
  - EP-03 Team Experience & Adoption

- **Example User Stories**

```text
US-01: As a team member, I want to create a task with a title, description, due date and assignee so that responsibilities are clear.

US-02: As a team member, I want to change the status of a task (To Do, In Progress, Done) so that the board reflects reality.

US-03: As a team lead, I want to filter tasks by assignee so that I can quickly see each person’s workload.

US-04: As a team member, I want to edit a task when requirements change so that the information stays accurate.

US-05: As a team lead, I want to see all tasks overdue or due soon so that I can follow up proactively.
