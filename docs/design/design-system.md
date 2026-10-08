# GoalTrack - Design System

## Brand Principles

GoalTrack should feel calm, clear, organized, and motivating. The interface should avoid unnecessary visual clutter and make goals and tasks easy to understand.

## Color Palette

- Primary: Bootstrap Blue `#0d6efd`
- Background: Light Gray `#f8f9fa`
- Cards: White `#ffffff`
- Main text: Dark Gray `#212529`
- Secondary text: Gray `#6c757d`
- Success: Bootstrap Success
- Warning: Bootstrap Warning
- Error: Bootstrap Danger
- Borders: Light Gray

Color should not be the only way to communicate status.

## Typography

GoalTrack uses the existing Bootstrap typography system. Headings should clearly separate sections and body text should remain readable. Bold text may emphasize goal names, task names, and labels.

## Logo Usage

No custom graphic logo is required for this version. The application name **GoalTrack** is the primary brand identifier in the navigation.

## Spacing & Grid

Use Bootstrap's responsive grid and spacing utilities. Keep consistent spacing between navigation, page sections, cards, tasks, buttons, forms, headings, and descriptions.

## Core Components

### Navigation

Provides access to Home, Goals, and About.

### Buttons

Use Bootstrap button styles with clear labels such as View Goals, View Goal, and Back to Goals.

### Goal Cards

Goal cards display:

- Goal name
- Short description
- Progress
- Number of incomplete tasks

Selecting a goal opens its detail view.

### Progress

Goal progress is calculated from completed tasks divided by total tasks.

### Task Items

Each task displays:

- Task name
- Completion status
- Due date when available

Users can mark tasks complete or incomplete and change due dates.

### Empty States

Empty states clearly explain when a goal has no tasks.

### Error States

Error states clearly explain when goal data cannot be loaded.

## Voice & Tone

GoalTrack uses language that is:

- Friendly
- Concise
- Encouraging
- Easy to understand

Avoid unnecessary technical language.

## Accessibility Standards

GoalTrack should:

- Use readable text with sufficient contrast.
- Avoid color as the only way to communicate information.
- Use descriptive labels for buttons and form controls.
- Use semantic HTML where appropriate.
- Support keyboard interaction.
- Keep navigation clear and consistent.
- Provide useful empty and error states.

The design aims to follow WCAG 2.1 AA principles where practical.

## Responsive Design

GoalTrack should work on desktop and mobile screen sizes.

The interface should:

- Prevent horizontal overflow.
- Keep text readable.
- Keep buttons and controls usable.
- Allow cards and task information to stack on smaller screens.

Bootstrap responsive classes should be used whenever possible.

## Version & Change Log

### Version 1.0 - Week 5

Initial GoalTrack design system created for the front-end build.