# Specification: GoalTrack

App description: GoalTrack is a simple web app for students and other individual users who want to connect larger goals with the smaller tasks needed to complete them. Users can browse goals, open a goal to see its tasks and progress, and mark tasks complete or update due dates.

## Style and Theme

GoalTrack should feel calm, clear, and motivating rather than crowded. The interface should use the starter project's Bootstrap-based layout, simple cards, readable headings, and consistent spacing.

Overall mood: Calm, organized, and encouraging.

Use the existing style guide and Bootstrap classes for fonts, spacing, buttons, cards, and responsive layout. Use clear status text and progress indicators rather than relying only on color.

## User Scenarios

### Story 1 (most important)

A student opens GoalTrack and sees a collection of current goals. They select a goal such as "Pass my networking course," see the goal description, a progress indicator, and a list of smaller tasks with due dates, then mark a completed task so the progress updates.

### Story 2

A user opens a goal and notices that one task is overdue. They select the task, review its details, and update its due date so the next action is clear.

### Story 3

A user returns to the home page and wants to quickly understand what needs attention. The page highlights current goals and the number of incomplete or overdue tasks without requiring the user to open every goal.

* * *

## Requirements

Write clear statements about what the app must do.

### Functional Requirements

1. The app must include these pages:
   * Home (`#/`)
   * Goal collection (`#/items`)
   * Goal detail (`#/items/:id`)
   * About (`#/about`)
2. The navigation bar must let people move to Home, Goals, and About.
3. The Home page must introduce GoalTrack and provide a clear action to view goals.
4. The Goal collection page must show one card for each goal in the data source.
5. Each goal card must show the goal name, short description, progress, and number of incomplete tasks.
6. Each goal card must provide a clear way to open that goal's detail page.
7. The Goal detail page must show the goal name, description, progress, and all tasks connected to that goal.
8. Each task must show a task name, completion status, and due date when one exists.
9. A user must be able to mark an incomplete task complete and mark a completed task incomplete again.
10. When a task's completion status changes, the goal progress must update immediately.
11. The detail page must allow a user to change a task's due date.
12. The app must show a clear empty-state message when a goal has no tasks.
13. The app must show a clear error message instead of a blank page if the data cannot load.
14. The app must provide visible navigation or a back action so users can return from a goal detail page to the goal collection.
15. The first version does not require user accounts, collaboration, notifications, payments, or server-side storage.

### Key Data

Use a simple data structure that can be represented in the starter project's text data file.

* Goal
  * id
  * name
  * description
  * category
  * image_url
* Task
  * id
  * goal_id
  * name
  * description
  * due_date
  * completed

A goal can have many tasks. Each task belongs to one goal through `goal_id`.

## Interaction Details

### Opening a goal

1. User opens the Goal collection.
2. User selects a goal card.
3. GoalTrack opens the matching goal detail page.
4. The detail page displays the goal information and connected tasks.

### Completing a task

1. User selects the completion control beside a task.
2. The task visibly changes to completed.
3. The progress indicator recalculates from completed tasks divided by total tasks.
4. The updated progress remains visible without requiring a page reload.

### Updating a due date

1. User selects the due-date control for a task.
2. A simple date input is shown.
3. User chooses a new date.
4. GoalTrack updates the displayed due date and keeps the task connected to its goal.

### Error and empty states

If data cannot be loaded, show a short message such as "We couldn't load your goals. Please try again." If a goal has no tasks, show "No tasks yet. Add a task to start making progress." The interface should never leave the main content area blank without explanation.

## Success Criteria

1. A new person can open the Goal collection from Home in one click.
2. A new person can open a goal detail page from the collection without help.
3. A user can identify the number of completed and incomplete tasks from the goal detail page.
4. A user can complete a task and see the goal progress update without refreshing the page.
5. A user can change a task due date without leaving the goal detail page.
6. If the data cannot load, the app shows a clear message instead of a blank page.
7. The prototype supports the main flow from goal collection → goal detail → complete task.

## Assumptions

* This is a beginner project and a prototype, not a production productivity service.
* The first version uses a simple text/CSV data source and client-side interaction.
* GitHub Pages can host the static HTML, CSS, JavaScript, and data files used by the prototype.
* The first version does not require authentication or a server database.
* Progress is calculated from the tasks connected to each goal.
* Due dates are optional; tasks without due dates remain valid.
* The interface should work on desktop and mobile-sized screens.
* Advanced features such as reminders, recurring tasks, sharing, and AI assistance are outside the first version.
* Findings from competitive research and prototype evaluation should be used to revise the specification before implementation.

## Revision Notes

Research identified useful patterns in existing task tools: projects/goals should contain tasks; task details should be available without losing context; due dates and progress should be visible; and users benefit from list/collection views that reduce navigation. The prototype also emphasizes a short primary flow and clear completion feedback. User interview findings and two outside usability observations should be added after the prototype is tested with real participants.