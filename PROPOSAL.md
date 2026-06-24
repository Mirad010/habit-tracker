# MP2 Proposal — Habit Tracker Pro

## What I'm building
A professional daily habit tracking tool that helps users build consistent routines by tracking streaks, visualizing progress, and providing motivational feedback — all running entirely in the browser with no server required.

## Who it's for / why
For myself — Mirbosit Adilov, a student balancing coursework, entrepreneurship, and personal development across time zones. The problem: I start habits strong but lose track after a few days because I have no visual system to hold me accountable. Existing apps are bloated or require sign-ups. I need something lightweight, fast, and always available.

## The state it tracks
- Array of habit objects: name, category, creation date, streak count, best streak, completed dates array
- Today's date (to determine which habits are done today)
- Overall completion rate across all habits
- Streak history per habit

## Core features
1. Add habits with name and category (Health, Study, Personal)
2. Mark habits complete each day — one click
3. Live streak counter with best streak memory
4. Progress bar toward 30-day mastery goal
5. Daily completion score (e.g. 4/5 habits done today)
6. localStorage persistence — data survives browser close
7. Delete habits with confirmation
8. Reset individual habit streak

## What I don't know yet
- How to compare today's date against stored dates accurately
- How to handle streak logic when a day is skipped
- Best way to structure habit objects in localStorage
- How to make DOM updates feel smooth without a framework