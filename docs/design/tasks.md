# GoalTrack Tasks

## Task 1 — Adapt the Data Model

### Objective

Adapt the existing starter-project data to support the GoalTrack specification.

### Work

Create or modify the sample data so that it represents:

- Goals
- Tasks
- Goal/task relationships

Each goal should include:

- `id`
- `name`
- `description`
- `category`
- `image_url`

Each task should include:

- `id`
- `goal_id`
- `name`
- `description`
- `due_date`
- `completed`

Include multiple goals and multiple tasks so the interface can demonstrate different progress states.

### Acceptance Criteria

- Goal data contains all required goal fields.
- Task data contains all required task fields.
- Each task has a valid `goal_id`.
- Sample data includes both completed and incomplete tasks.
- At least one goal can demonstrate multiple tasks.
- The existing application can load the adapted data.

---

## Task 2 — Adapt the Goal Collection View

### Objective

Update the existing collection/list view to display GoalTrack goals.

### Work

Modify the existing collection view rather than creating an entirely new page.

Each goal card should display:

- Goal name
- Short description
- Progress
- Number of incomplete tasks
- A clear control for opening the goal

Use the existing Bootstrap-based styling and responsive layout.

### Acceptance Criteria

- Every goal in the data source is displayed.
- Goal names are visible.
- Descriptions are visible.
- Progress is visible.
- Incomplete task counts are visible.
- Each goal can be selected.
- The layout remains usable on smaller screens.

---

## Task 3 — Connect Goal Cards to Goal Details

### Objective

Allow users to open the correct goal detail page from the Goal collection.

### Work

Use the existing routing/navigation system to connect each goal card to its corresponding goal detail route.

The selected goal ID should identify which goal is displayed.

### Acceptance Criteria

- Selecting a goal opens the goal detail page.
- The correct goal is displayed.
- Different goal cards open their corresponding goals.
- Users can return to the Goal collection.

---

## Task 4 — Adapt the Goal Detail View

### Objective

Update the existing detail view to display the selected GoalTrack goal and its tasks.

### Work

Display:

- Goal name
- Goal description
- Goal progress
- Connected tasks
- Task names
- Completion status
- Due dates when available

Filter or otherwise identify tasks using their `goal_id`.

### Acceptance Criteria

- The selected goal's information is displayed.
- Only tasks connected to the selected goal are displayed.
- Task names are visible.
- Completion status is visible.
- Due dates are displayed when available.
- The user can return to the Goal collection.

---

## Task 5 — Add Task Completion

### Objective

Allow users to mark tasks complete and incomplete.

### Work

Add a completion control beside each task.

When the control is used:

- An incomplete task becomes complete.
- A completed task can become incomplete again.
- The visual state of the task changes immediately.

### Acceptance Criteria

- An incomplete task can be marked complete.
- A completed task can be marked incomplete.
- The changed state is visible immediately.
- The task remains associated with the correct goal.

---

## Task 6 — Add Goal Progress Calculation

### Objective

Calculate goal progress from task completion.

### Work

Calculate progress using:

`completed tasks / total tasks`

Update the progress whenever a task changes between complete and incomplete.

### Acceptance Criteria

- Progress is based on the current task states.
- Completing a task increases the appropriate progress value.
- Marking a task incomplete decreases the appropriate progress value.
- The updated progress appears without a page reload.
- A goal with no tasks does not cause a calculation error.

---

## Task 7 — Add Due-Date Editing

### Objective

Allow users to change a task's due date from the goal detail page.

### Work

Add a simple date input/control for tasks.

When the user selects a new date, update the task's displayed due date.

### Acceptance Criteria

- Tasks with due dates display their dates.
- The user can select a new date.
- The updated date appears immediately.
- The task remains connected to its original goal.
- Tasks without due dates remain valid.

---

## Task 8 — Add Empty-State Handling

### Objective

Make the application understandable when a goal has no tasks.

### Work

Add a clear message when the selected goal contains no tasks.

Suggested message:

> No tasks yet. Add a task to start making progress.

### Acceptance Criteria

- A goal with zero tasks does not show an empty/blank task area.
- A clear message explains the situation.
- The page remains usable.
- The progress calculation does not produce an error.

---

## Task 9 — Add Error-State Handling

### Objective

Prevent the application from displaying a blank page when data cannot be loaded.

### Work

Add an error state for data-loading failures.

Suggested message:

> We couldn't load your goals. Please try again.

### Acceptance Criteria

- Data-loading errors produce a visible message.
- The error message explains that the data could not be loaded.
- The main content area is not left blank without explanation.

---

## Task 10 — Refine Navigation

### Objective

Make navigation between the main GoalTrack views clear and consistent.

### Work

Verify the navigation bar provides access to:

- Home
- Goals
- About

Also provide a clear way to return from goal details to the goal collection.

### Acceptance Criteria

- Home is accessible from the navigation.
- Goals is accessible from the navigation.
- About is accessible from the navigation.
- A user can return from a goal detail page to the Goal collection.
- Navigation works at the expected routes.

---

## Task 11 — Refine the Home Page

### Objective

Make the Home page clearly introduce GoalTrack and direct users toward the main functionality.

### Work

The Home page should:

- Explain what GoalTrack is.
- Communicate the relationship between goals and tasks.
- Provide a clear action for viewing goals.

### Acceptance Criteria

- A new user can understand the purpose of GoalTrack.
- A clear action leads to the Goal collection.
- The page fits the overall GoalTrack visual style.

---

## Task 12 — Responsive and Visual Refinement

### Objective

Improve the usability and consistency of the completed prototype.

### Work

Use the existing Bootstrap styles and starter-project structure.

Check:

- Spacing
- Headings
- Buttons
- Cards
- Progress indicators
- Task controls
- Navigation
- Mobile layout
- Desktop layout
- Readability

Use status text and clear labels in addition to color when communicating task or progress status.

### Acceptance Criteria

- The application is readable on desktop-sized screens.
- The application is usable on mobile-sized screens.
- Controls are clearly identifiable.
- Cards and sections have consistent spacing.
- Progress information is understandable.
- The visual design remains calm, clear, and organized.

---

## Task 13 — Test the Primary User Flow

### Objective

Verify that the prototype supports the primary GoalTrack scenario.

### Test Flow

1. Open the Home page.
2. Select the action to view goals.
3. Open the Goal collection.
4. Select a goal.
5. View the goal's tasks.
6. Mark an incomplete task complete.
7. Confirm that goal progress updates.
8. Mark the task incomplete again.
9. Change the task's due date.
10. Return to the Goal collection.

### Acceptance Criteria

- The entire flow can be completed without the application breaking.
- Goal information remains correct.
- Task information remains connected to the correct goal.
- Progress updates correctly.
- Due dates update correctly.
- Navigation works throughout the flow.

---

## Task 14 — Final Requirement Check

### Objective

Compare the completed prototype against the GoalTrack specification.

### Checklist

- [ ] Home page exists.
- [ ] Goal collection exists.
- [ ] Goal detail exists.
- [ ] About page exists.
- [ ] Navigation works.
- [ ] Goal cards display required information.
- [ ] Goal details display required information.
- [ ] Tasks display required information.
- [ ] Tasks can be completed.
- [ ] Tasks can be marked incomplete.
- [ ] Progress updates immediately.
- [ ] Due dates can be changed.
- [ ] Empty states are handled.
- [ ] Error states are handled.
- [ ] Users can return to the Goal collection.
- [ ] Responsive layout has been checked.
- [ ] Primary user flow works.

### Definition of Done

The front-end prototype is ready for evaluation when the main GoalTrack user flow works from beginning to end, the requirements above are implemented, the interface has been checked on desktop and mobile-sized screens, and no major navigation or interaction errors remain.