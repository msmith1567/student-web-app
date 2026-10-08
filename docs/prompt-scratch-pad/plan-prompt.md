# GoalTrack Plan Prompt

Given the existing GoalTrack business case and specification, create a draft of the plan document for the application.

Use the existing `docs/design/plan.md` template and the relevant plan guide as references. The plan should remain consistent with the existing specification and should not introduce unnecessary features or technologies.

GoalTrack is a simple web application that connects larger goals with smaller tasks. Users should be able to view goals, open a goal to see its tasks and progress, mark tasks complete or incomplete, and update task due dates.

The first version is a front-end prototype. It should use the existing starter project rather than requiring a complete rewrite.

Important requirements from the specification include:

- Home page
- Goal collection page
- Goal detail page
- About page
- Navigation between pages
- Goal cards showing name, description, progress, and incomplete task count
- Goal detail showing the goal and its connected tasks
- Tasks showing name, completion status, and due date when available
- Ability to mark tasks complete and incomplete
- Immediate progress updates
- Ability to change task due dates
- Empty state for goals without tasks
- Error state if data cannot load
- Back/navigation action from goal details
- No authentication, collaboration, notifications, payments, or server-side storage in the first version

The data model is:

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

A task belongs to one goal through `goal_id`.

The implementation should be incremental and should prioritize a working front-end prototype before any future backend or advanced functionality.

Keep the plan focused on the actual requirements. Do not invent features, technologies, or architecture that are not supported by the specification.

After creating the draft, check it against the specification and identify any inconsistencies, missing requirements, unnecessary scope, or unclear implementation decisions.

The final plan should cover:

- Approach
- Goals
- Scope
- Technology
- Data
- User flow
- Components
- Implementation sequence
- Dependencies
- Assumptions
- Risks
- Success criteria
- Future development