# BeeFit

BeeFit is an offline-first fitness planning PWA focused on equipment-aware workout generation.

The core question BeeFit should answer is:

> Given where I am training today, what should I train, what can I do with this equipment, and what am I missing this week?

BeeFit is planned as a free, installable, account-free app. It should help users choose a training target, generate a deterministic workout from the equipment available right now, log the session locally, and update muscle coverage after the workout is finished.

## Current Status

This repository is at project bootstrap stage. The first implementation target is a narrow vertical slice rather than a full workout platform.

The initial slice must prove:

- Equipment-aware workout generation.
- Local-first persistence.
- Basic workout logging.
- Muscle coverage updates after finishing a session.
- PWA and offline feasibility.

## Planned Stack

- Angular PWA
- TypeScript
- IndexedDB via Dexie
- Angular service worker for offline app shell support
- GitHub Pages for static hosting
- No required backend for the MVP
- No account or cloud sync for the MVP

## First Build Scope

The first build is intentionally small: 3 to 5 core screens that validate the product loop.

Planned screens:

- Dashboard
- Plan Workout
- Generated Workout
- Active Workout
- Session Summary

Planned seed data:

- Bodyweight preset
- Home dumbbells preset
- Simple gym preset
- Small curated beginner-safe exercise dataset

Planned first generator:

- Deterministic and inspectable.
- Filters exercises by selected equipment.
- Scores candidates by target muscle match, missing muscle coverage, movement balance, and recent weekly work.
- Produces stable output for the same inputs and stored session history.

## What Is Deferred

The first slice will not include:

- AI workout generation
- Accounts
- Cloud sync
- Custom exercise creation
- Equipment preset editing
- Training splits
- Cardio logging
- Mobility logging
- Import/export backup
- Advanced analytics
- Social features

These can be added after the core local-first generation and logging loop is proven.

## Development

The app has not been scaffolded yet. Once the Angular project is created, this section should be updated with exact setup commands.

Expected local workflow:

```bash
npm install
npm start
npm test
npm run build
```

## Privacy And Safety

BeeFit is designed to be local-first. MVP user data should live in the user's browser through IndexedDB, with no mandatory account or server-side data copy.

BeeFit should not present itself as medical advice. Beginner mode, conservative recommendations, pain warnings, and clear safety copy are part of the product direction.

## License

No license has been selected yet.
