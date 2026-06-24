# PRD — Habit Tracker Pro

## Overview
A browser-based habit tracking application built with vanilla JavaScript. Users can create, track, and analyze daily habits with streak counting, progress visualization, and persistent storage. No server, no sign-up, no dependencies.

## Problem Statement
Students and young professionals struggle to maintain consistent daily habits. Existing solutions are either too complex (require accounts, subscriptions) or too simple (no feedback, no motivation). The gap: a lightweight, fast, always-available tool that gives real accountability without friction.

## Target User
**Primary:** Mirbosit Adilov — Business Analytics student, entrepreneur, managing multiple responsibilities across time zones.
**Secondary:** Any student or professional who wants to build daily routines without downloading an app.

## User Stories
1. As a user, I want to add a habit with a name and category so I can organize my routines.
2. As a user, I want to mark a habit as complete today so I can track my daily progress.
3. As a user, I want to see my current streak so I stay motivated to keep going.
4. As a user, I want to see my best streak so I know my personal record.
5. As a user, I want a progress bar so I can visualize how close I am to mastering a habit.
6. As a user, I want my data to persist after closing the browser so I don't lose my progress.
7. As a user, I want to delete a habit I no longer track.
8. As a user, I want to see today's overall completion score.

## Functional Requirements

### Habit Management
- Add habit: name (required) + category (Health / Study / Personal)
- Delete habit with confirmation prompt
- Reset streak for individual habit

### Daily Tracking
- Mark habit as done / undo for today only
- Streak increments only once per day
- Missing a day breaks the streak

### Progress & Stats
- Progress bar: streak / 30 days × 100%
- Best streak memory per habit
- Daily score: X / Y habits completed today
- Category filter: view All / Health / Study / Personal

### Persistence
- All data saved to localStorage on every change
- Data loads automatically on page open

## Technical Specifications
- Vanilla JavaScript only — no frameworks, no CDN
- Single HTML file with embedded CSS and JS
- localStorage for persistence
- DOM manipulation only — no alert() boxes
- Mobile responsive

## State Structure
```javascript
habits = [
  {
    id: 1234567890,
    name: "Read 30 minutes",
    category: "Study",
    streak: 7,
    bestStreak: 12,
    completedDates: ["Mon Jun 16 2026", "Tue Jun 17 2026"],
    createdAt: "Sun Jun 15 2026"
  }
]
```

## Success Metrics
- User can add and track a habit in under 30 seconds
- Streak logic is accurate — never increments twice in one day
- Data persists across browser sessions
- Works on mobile without horizontal scrolling

## Out of Scope
- User accounts or authentication
- Backend server or database
- Push notifications
- Social features
- External API calls