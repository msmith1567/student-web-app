# GoalTrack Plan

## Approach Summary

GoalTrack will be developed incrementally as a front-end web application prototype. The first version will focus on creating a functional and understandable user experience using the existing starter project rather than introducing unnecessary new technologies.

The implementation will begin by adapting the existing data model and sample data to represent goals and tasks. The goal collection view will then be updated to display GoalTrack goals with useful information such as descriptions, progress, and incomplete task counts. After that, the goal detail view will be adapted to show the selected goal and its connected tasks.

The next stage will add the main interactions required by the specification. Users will be able to mark tasks complete or incomplete, see goal progress update immediately, and change task due dates. Navigation, empty states, and error states will also be refined so the prototype provides a complete primary user flow.

The first version will remain a client-side prototype using placeholder/local data. Authentication, collaboration, notifications, payments, server-side storage, and other advanced features are outside the scope of this version.

## Goals

The primary goal is to create a working front-end prototype that demonstrates how GoalTrack connects larger goals with smaller tasks.

The prototype should allow a user to:

1. Open the Home page and understand the purpose of GoalTrack.
2. Navigate to the Goal collection.
3. View multiple goals and understand their current progress.
4. Open a specific goal.
5. View the tasks associated with that goal.
6. Mark tasks complete or incomplete.
7. See goal progress update immediately.
8. Change a task's due date.
9. Return to the Goal collection.
10. Understand when a goal has no tasks or when data cannot be loaded.

## Scope

### In Scope

- Home page
- Goal collection page
- Goal detail page
- About page
- Navigation between pages
- Goal cards
- Goal descriptions
- Goal progress indicators
- Incomplete task counts
- Task lists
- Task completion controls
- Changing task due dates
- Progress recalculation
- Empty states
- Error states
- Responsive layout
- Placeholder/sample data
- Front-end interaction using client-side data

### Out of Scope

- User accounts
- Authentication
- Collaboration between users
- Notifications
- Payments
- Server-side database
- Cloud data synchronization
- Recurring tasks
- Sharing goals
- AI assistance
- Production-level security
- Advanced analytics

## Tech Stack

### Frontend

- HTML
- CSS
- JavaScript
- Existing starter-project framework and structure
- Bootstrap classes and components already provided by the template

### Data

The first version will use the existing starter project's client-side/text data approach with placeholder data.

The primary data structures will be:

**Goal**
- `id`
- `name`
- `description`
- `category`
- `image_url`

**Task**
- `id`
- `goal_id`
- `name`
- `description`
- `due_date`
- `completed`

Each goal can contain multiple tasks. Each task belongs to one goal through `goal_id`.

### Hosting

The completed front-end prototype will be published through GitHub Pages.

## User Flow

The primary user flow is:

Home → Goal Collection → Goal Detail → Complete Task → Progress Updates

A secondary flow is:

Goal Collection → Goal Detail → Change Due Date → Updated Task

Users should also be able to return from the goal detail page to the goal collection.

## Components

### Home

The Home page introduces GoalTrack and provides a clear action for viewing goals.

### Goal Collection

The Goal collection displays the available goals as cards.

Each card should provide:

- Goal name
- Short description
- Progress
- Number of incomplete tasks
- A clear way to open the goal

### Goal Detail

The Goal detail page displays:

- Goal name
- Goal description
- Goal progress
- Connected tasks
- Task completion status
- Task due dates
- Due-date editing controls
- Navigation back to the Goal collection

### Task Interaction

Tasks can be changed between incomplete and complete.

When a task's completion status changes, the progress for the associated goal is recalculated immediately.

### Empty State

If a goal contains no tasks, the application should display a useful message instead of leaving the task area blank.

Example:

> No tasks yet. Add a task to start making progress.

### Error State

If goal/task data cannot be loaded, the application should display an understandable error message.

Example:

> We couldn't load your goals. Please try again.

## Implementation Sequence

### Phase 1 — Adapt the Data

Modify the existing starter data to represent GoalTrack goals and tasks.

The data should contain enough sample goals and tasks to demonstrate the main application flow.

### Phase 2 — Adapt the Goal Collection

Update the existing collection/list view to display GoalTrack goals.

Each goal card should display the information required by the specification and provide navigation to the goal detail page.

### Phase 3 — Adapt the Goal Detail

Update the detail view so that it displays the selected goal and all tasks connected through `goal_id`.

### Phase 4 — Add Task Completion

Add the ability to mark tasks complete and incomplete.

The interface should immediately reflect the changed status.

### Phase 5 — Add Progress Calculation

Calculate goal progress using:

`completed tasks / total tasks`

Update the progress indicator immediately when task completion changes.

### Phase 6 — Add Due-Date Editing

Allow users to select a task's due-date control and change its due date.

The updated date should remain associated with the correct task and goal.

### Phase 7 — Navigation and States

Verify navigation between Home, Goal collection, Goal detail, and About.

Add clear empty and error states.

### Phase 8 — Responsive and Visual Refinement

Use the existing Bootstrap-based styling and starter-project structure to make the interface clear and usable on desktop and mobile-sized screens.

Focus on readable text, consistent spacing, clear controls, and visible status information.

### Phase 9 — Testing

Test the primary user flow:

1. Open Home.
2. Open Goals.
3. Select a goal.
4. View its tasks.
5. Complete a task.
6. Confirm progress changes.
7. Mark the task incomplete again.
8. Change a due date.
9. Return to the Goal collection.

Also test empty and error states.

## Dependencies

- Existing starter project
- Existing routing/navigation structure
- Existing styling framework
- Existing client-side data structure
- GitHub repository
- GitHub Pages deployment

The implementation should reuse the existing starter project wherever possible instead of replacing the application architecture.

## Assumptions

- The first version is a front-end prototype.
- Authentication is not required.
- A server database is not required.
- Placeholder data is acceptable for the prototype.
- GitHub Pages can host the front-end application.
- Progress is calculated from task completion.
- Due dates are optional.
- A goal may contain zero or more tasks.
- Each task belongs to one goal.
- The existing starter project can be adapted without a complete rewrite.

## Risks and Mitigation

| Risk | Mitigation |
|---|---|
| The project becomes too large | Keep the first version limited to the requirements in the specification. |
| Existing template code is changed unnecessarily | Reuse existing components, routing, styling, and data structures where possible. |
| Progress calculations become inconsistent | Calculate progress directly from the current task completion states. |
| Navigation becomes confusing | Keep Home, Goals, and About visible in the main navigation and provide a back action from goal details. |
| Empty data creates confusing screens | Provide explicit empty-state messages. |
| Data errors produce blank pages | Provide an explicit error message. |
| Mobile layout becomes difficult to use | Test the major screens at desktop and mobile-sized widths. |

## Success Criteria

The plan will be considered successful when the resulting prototype:

1. Allows a user to reach the Goal collection from Home.
2. Displays goals as understandable cards.
3. Allows a user to open a goal.
4. Displays the goal's connected tasks.
5. Allows tasks to be completed and marked incomplete.
6. Updates goal progress immediately.
7. Allows task due dates to be changed.
8. Provides clear navigation.
9. Provides useful empty and error states.
10. Supports the primary collection → detail → complete-task flow.

## Future Development

After the front-end prototype is completed and evaluated, future versions could add:

- User accounts
- Persistent database storage
- Cloud synchronization
- Task creation and editing
- Goal creation and editing
- Notifications and reminders
- Recurring tasks
- Collaboration
- Additional progress analytics
- AI-assisted planning

These features are intentionally deferred so that the first prototype remains manageable and focused.