# Team To-Do Web App – IT Project Example (Self-Initiated)

## 0. Personal Note – Why I Built This

I created this project as part of my **transition from general project management into IT / digital project management**.

In my current work I don’t manage software development directly, so I wanted a safe, realistic way to practise:

- Writing requirements and user stories  
- Planning sprints and releases  
- Thinking about risks, testing and UAT  
- Using tools like GitHub to document IT projects  

This is a **self-initiated learning project**, not a commercial product.  
However, I structured it the way I would approach a **real internal web app** for a small team.



## 1. Executive Summary

This repository documents a complete **project example** for a lightweight **Team To-Do Web Application**.

The goal of the project is to show how I work as an **IT Project Manager / Delivery Lead** across the full lifecycle:

- Understanding the problem and business goals  
- Defining scope and requirements  
- Planning delivery using sprints and a simple roadmap  
- Managing risks and assumptions  
- Preparing for testing, UAT and release

The focus is on **project management thinking and structure**, not on writing the actual code.



## 2. Business Context & Problem Statement

Small teams often manage tasks across many places (chat, email, personal notes). This creates:

- Low visibility into who is doing what  
- Missed deadlines and follow-ups  
- No single source of truth for the team’s work  

**Business Goal**  
Provide a simple web app where a team can see all tasks in one place, with:

- Clear owners  
- Clear due dates  
- Clear status (To Do / In Progress / Done)

**Outcome I would aim for in a real team**

- Better visibility for the team lead  
- Fewer “forgotten” tasks  
- More predictable delivery on deadlines



## 3. Objectives & Example Success Metrics

### 3.1 Objectives

1. Give the team a **central view** of all tasks.  
2. Make it easy to **create, update and complete tasks**.  
3. Use an **agile way of working** (backlog, sprints, releases).  
4. Show how I would manage an **IT project end-to-end**, even in a small scope.

### 3.2 Example Metrics (for a real implementation)

If this app were really deployed, I would look at things like:

- % of active tasks that have an **owner and due date**  
- % of tasks completed **on or before due date**  
- Adoption: how many team members use it at least **once a week**  
- Stability of sprints: how often we deliver what we commit to

For this portfolio project, these are **target ideas**, not measured live metrics.



## 4. Scope, Constraints & Assumptions

### 4.1 In Scope (for the first version)

- Web UI where users can:
  - Create tasks  
  - See a list or board of tasks  
  - Edit tasks  
  - Change status (To Do / In Progress / Done)  
- Basic filtering (e.g. by assignee, by status)
- Simple way to spot overdue / near-due tasks
- Documentation:
  - Requirements and user stories  
  - Sprint plan  
  - Risk log  
  - Test / UAT checklist  
  - Release notes for v1.0 (simulated)

### 4.2 Out of Scope (for the first version)

- Mobile app  
- Complex roles and permissions  
- Integrations (Slack, email, calendar, etc.)  
- Advanced reporting / analytics  
- Enterprise-level security features (SSO, RBAC, etc.)

These could be part of a **future roadmap**.

### 4.3 Constraints (for this case study)

- No dedicated dev team in this project – the focus is on **planning and documentation**.  
- Tools are kept simple: GitHub for documentation, plus any boards or spreadsheets used during planning.


## 5. Stakeholders, Roles & Ways of Working

### 5.1 Example Stakeholder Map (if this were real)

| Role             | Example Person           | Focus                                           |
|------------------|--------------------------|-------------------------------------------------|
| Sponsor          | Head of Operations       | Wants better visibility and on-time delivery    |
| Product Owner    | Team Lead                | Owns backlog, priorities, and acceptance        |
| IT Project Mgr   | Myself                   | Planning, coordination, risks, communication    |
| Engineering Lead | Senior Developer         | Technical design, estimates, implementation     |
| QA / UAT         | Selected team members    | Validating that it works in real workflows      |

### 5.2 Cadence (how I’d run it)

If this were a real project, I would suggest:

- Regular **backlog refinement** (weekly or bi-weekly)  
- **Planning** at the start of each sprint  
- **Sprint review/demo** at the end of each sprint  
- **Retrospective** to improve how the team works  
- Short **check-ins** if needed, especially early in the project

In this case study, these are represented as notes and structured plans rather than real meetings.



## 6. Solution Overview

### 6.1 What the app does (conceptually)

The Team To-Do Web App lets a team:

- Create tasks with:
  - Title  
  - Description  
  - Assignee  
  - Due date  
  - Status  
- View all tasks in:
  - A list view  
  - Optionally a simple board view (To Do / In Progress / Done)  
- Filter tasks, for example:
  - By assignee  
  - By status  
- See which tasks are:
  - Overdue  
  - Due soon  

### 6.2 Non-functional aspects (at a high level)

If it were built for real use, I would care about:

- **Ease of use:** very simple, low learning curve  
- **Performance:** fast enough for a small team (no long delays)  
- **Reliability:** no data loss during normal use  
- **Future potential:** possibility to add integrations later



## 7. Delivery Approach

### 7.1 Method

I used a **Scrum-style** approach with:

- A product backlog written as **user stories** with acceptance criteria  
- **Sprints** with clear goals  
- Simple **release planning** (MVP first, improvements later)

### 7.2 High-Level Sprint Plan

Planned sprints are described in:  
`team-todo-web-app/planning/sprint-plan.md`

At a high level:

- **Sprint 0 – Discovery**  
  Understand the problem, define personas, draft backlog and scope.

- **Sprint 1 – Core Task Management (MVP)**  
  Basic task creation, list view and status updates.

- **Sprint 2 – Visibility & Usability**  
  Filters, overdue/soon highlighting, simple board view.

- **Sprint 3 – Hardening & UAT Prep**  
  Clean-up, edge cases, UAT checklist and v1.0 release notes.

---

## 8. Requirements & User Stories

Detailed user stories and acceptance criteria are in:  
`team-todo-web-app/requirements/user-stories.md`

Stories are organised into epics:

- **EP-01 Core Task Management** – create, view, edit, update tasks  
- **EP-02 Visibility & Filtering** – filters, highlighting, board view  
- **EP-03 Team Experience & Adoption** – error handling, onboarding, simple activity info

The user stories are written in standard **“As a…, I want…, so that…”** format.



## 9. Risks, Assumptions & Dependencies

A simple **risk and assumptions log** is kept in:  
`team-todo-web-app/planning/risk-log.md`

Typical examples:

- Risk of **low adoption** if the tool doesn’t fit existing habits.  
- Risk of **scope creep** if we try to add integrations too early.  
- Assumption that the team can use a **web-based tool** comfortably.  

In a real environment, this log would be reviewed regularly and linked to actions.



## 10. Environments, Releases & Change (Conceptual)

In a real implementation, I would expect:

- At least two environments:
  - **Test/UAT**  
  - **Production**  
- A simple release flow:
  - Build and test in **Test/UAT**  
  - UAT sign-off  
  - Deploy to **Production**  

Here, this is represented as **documentation only**, in:  
`team-todo-web-app/releases/release-notes-v1.0.md`

The release notes describe:

- What’s included in v1.0  
- Any known limitations  
- Ideas for next versions



## 11. Quality Strategy: Testing & UAT

The approach to quality in this project focuses on **clear acceptance criteria** and a structured UAT checklist.

### 11.1 Testing

Basic functional checks include:

- Creating tasks with required fields  
- Editing and updating tasks  
- Changing status correctly  
- Filtering by assignee and status  
- Highlighting overdue / near-due tasks  

Test scenarios are documented in:  
`team-todo-web-app/uat/testing-checklist.md`

### 11.2 UAT Approach

If we had real users, I would:

- Choose a small group of team members  
- Give them realistic scenarios (e.g. “Create all tasks for next week”)  
- Ask for feedback on:
  - Ease of use  
  - Missing features  
  - Confusing parts of the UI  

Their feedback would then feed into the **backlog** for future iterations.



## 12. How I Would Work With a Real Team

Even for a small internal app like this, I would focus on:

- **Transparency:** Everyone sees the same backlog and priorities.  
- **Simple documentation:** Just enough to keep us aligned.  
- **Regular feedback:** Quick demos, UAT, open discussion of what works and what doesn’t.  
- **Respect for technical reality:** Adjusting scope based on real constraints from developers and tech leads.

---

## 13. Outcomes & Learnings (from This Project)

This project helped me:

- Practise turning a problem into a **clear scope and backlog**.  
- Write user stories and acceptance criteria in a structured way.  
- Think through a **realistic sprint and release plan**.  
- Consider risks, dependencies, testing and UAT like I would in a real IT environment.  

It also shows how I would use **GitHub** not only for code, but also as a place to store and share **project documentation**.



## 14. Repository Structure

```text
team-todo-web-app/
  ├── README.md                          # This project overview
  ├── requirements/
  │   └── user-stories.md               # Backlog and acceptance criteria
  ├── planning/
  │   ├── sprint-plan.md                # Sprint breakdown, goals and scope
  │   └── risk-log.md                   # Risks, assumptions and dependencies
  ├── uat/
  │   └── testing-checklist.md          # Test scenarios and UAT script
  └── releases/
      └── release-notes-v1.0.md         # Simulated release notes
