# GoalTrack Tasks Prompt

Using `docs/design/plan.md` and `docs/design/specification.md`, create the tasks document for the GoalTrack front-end prototype.

Use the tasks guide and existing tasks template as references.

The purpose of these tasks is to adapt the existing starter web application into a working GoalTrack front-end prototype. Focus on front-end development and adapting the existing template. Avoid tasks that require a complete rewrite of the application.

The prototype must support:

- Home page
- Goal collection
- Goal detail
- About page
- Navigation
- Goal cards
- Goal descriptions
- Goal progress
- Incomplete task counts
- Tasks connected to goals
- Task completion/incompletion
- Immediate progress updates
- Task due-date editing
- Empty states
- Error states
- Responsive layout

Use the following data structures:

Goal:
- id
- name
- description
- category
- image_url

Task:
- id
- goal_id
- name
- description
- due_date
- completed

The primary user flow is:

Home → Goal Collection → Goal Detail → Complete Task → Progress Updates

A secondary flow is:

Goal Detail → Change Due Date → Updated Task

Create small, actionable tasks in a logical order.

Each task should have:

- Objective
- Work to be completed
- Acceptance criteria

Include a final testing task and a final requirement-check task.

Do not add authentication, databases, collaboration, notifications, payments, AI features, or other advanced features because they are outside the scope of the first prototype.

Be mindful of the existing starter application and reuse its existing routing, components, data structures, and Bootstrap styling where possible.

After creating the tasks, check them against the specification and plan. Remove redundant tasks and make sure every major requirement has a corresponding implementation or testing task.