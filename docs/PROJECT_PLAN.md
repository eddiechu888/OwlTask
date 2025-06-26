# OwlTask Project Plan

## Project Description
OwlTask is a web-based task management tool aimed at real-time coordination across individuals and groups. The system addresses the common problem of scattered task tracking by providing a single location where assignments, due dates and current status can be viewed and updated. By leveraging a lightweight architecture and extensible design, the application allows teams to organize work without the overhead of heavy project management software.

The initial release keeps the feature set minimal in order to produce a stable foundation. OwlTask offers basic user registration, group creation and role assignment. Users can create tasks, assign them to individuals or groups, and mark progress as they go. The importance of this application lies in its ability to synchronize multiple users in real-time so that everyone always sees an up-to-date picture of the work being done.

## Use Case Descriptions
- **General team member** – Wants to create and update tasks assigned to them or their group. They need to check deadlines and mark work complete when finished.
- **Team lead** – Monitors task status for their team. They reassign work when necessary and ask the system for quick summaries of progress.

## Functional Requirements
- Users must be able to register, log in and belong to one or more groups.
- The system shall allow creation of tasks with title, description, due date, priority and assignee(s).
- Users shall update task status and mark tasks complete.
- Connected clients receive real-time updates through a WebSocket channel.
- The system shall answer status questions such as "How's progress since <date>?" via GPT‑4o summaries.
- Browser notifications alert users about new assignments or approaching deadlines.

## Natural Language Progress Summaries
To help leads quickly understand team status, OwlTask provides a natural
language reporting feature. The application collects recent task changes,
deadlines and assignments then calls GPT‑4o to generate a concise report
describing completed work, upcoming milestones and who is working on what.
This contextual summary responds to prompts like "How's progress since last
week?" without requiring a deep dive into each task.

## Non‑Functional Requirements
- The user interface must be responsive to desktop, tablet and phone screens.
- The application must support concurrent editing with eventual consistency across clients.
- The design should enable easy extension of the data model and API.
- The entire system runs in a single Docker container deployable to Heroku.
- Implementation should employ design patterns such as Observer, Composite, Command and Strategy to ensure maintainability.

## Omitted Items
Some capabilities are deliberately postponed to keep the scope manageable:
- Hierarchical permissions or extensive role management.
- Integration with third‑party calendar or notification systems.
- Advanced search, tagging or analytics.

These features could be layered on later by extending the API and database schema while reusing the existing WebSocket infrastructure.

## Underlying Infrastructure
The backend uses Java with Spark to expose REST endpoints and WebSocket messaging. A PostgreSQL database stores users, groups and tasks. The frontend is implemented with React and TypeScript. Both components run in a Docker container that can be deployed directly to Heroku for testing or production use. GPT‑4o integration is encapsulated in a service layer so that status summaries can be generated without blocking real‑time updates.

## Schedule
1. **Week 1** – Finalize requirements and create initial UI prototypes.
2. **Week 2** – Implement user and group management with basic task CRUD operations.
3. **Week 3** – Add real‑time update logic and notifications.
4. **Week 4** – Integrate GPT‑4o status summaries and polish the UI.
5. **Week 5** – Testing, bug fixing and final documentation.
