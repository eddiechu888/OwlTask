# OwlTask Project Plan

## Overview
OwlTask is a web-based task management tool for real-time coordination across individuals and groups. The goal is to keep the first release minimal and easily extensible.

This project plan outlines the initial feature set, architecture, and timelines.

## Core Features
- **User management**: register/login, create groups, assign basic roles.
- **Task creation and assignment**: users can create tasks, assign them to individuals or groups, add due dates and priorities.
- **Task status tracking**: update a task's progress, mark tasks complete, and view tasks by owner, group, or due date.
- **Basic notifications**: browser alerts for assignment changes or approaching deadlines.
- **Real-time updates**: websocket-based message passing to keep connected clients synchronized.

## Unique Extension: GPT-4o Status Summaries
To keep the interface friendly, OwlTask supports natural language queries such as "How's progress since <date>?" The system collects recent task activity, upcoming deadlines, and current assignments, then uses GPT-4o to produce a concise summary describing completed work, approaching due dates, and what team members are working on. The response is contextual and informative.


## Implementation Approach
- **Architecture**: Lightweight MVVM spanning frontend and backend. The React client acts as the View and communicates with a Java-based ViewModel via REST and websockets.
- **Backend**: Java with Spark handles websocket messaging, REST endpoints, and GPT-4o integration.
- **Frontend**: React and TypeScript provide a responsive interface.
- **Database**: simple relational schema for users, groups, tasks, and comments.
- **Design patterns**: Observer for WebSocket notifications, Composite for nested tasks, Command to encapsulate task actions, and Strategy for pluggable sorting or notification approaches.
- **Deployment**: containerized app deployed to Heroku.

## Schedule (high level)
1. **Week 1** – Finalize requirements and create initial UI prototypes.
2. **Week 2** – Implement user and group management with basic task CRUD operations.
3. **Week 3** – Add real-time update logic and notifications.
4. **Week 4** – Integrate GPT-4o status summaries and polish the UI.
5. **Week 5** – Testing, bug fixing, and final documentation.

## Future Improvements
This plan intentionally keeps the scope modest. Future features such as hierarchical permissions, advanced search, or integration with external tools can be added later due to the project's extensible design.

