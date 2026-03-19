# Building Reusable Module Components

Modula packages should be structured so routes assemble reusable UI parts instead of becoming giant page files.

## Core rule

- Keep route files thin.
- Put layout and shell wrappers in reusable components.
- Keep widgets separate from full page surfaces.
- Keep package-local state, services, and helpers out of route markup.

## Recommended package frontend structure

```text
frontend/
├── routes/
├── components/
│   ├── layout/
│   ├── cards/
│   ├── forms/
│   ├── lists/
│   ├── states/
│   └── widgets/
├── stores/
├── lib/
├── styles/
└── assets/
```

## Practical guidance

- Use shared shell wrappers so module pages inherit the same chrome, sidebar access, and width behavior.
- Extract repeated post cards, thread rows, result cards, and empty states into components.
- Keep page-level orchestration in routes or page shells.
- Keep API calls and state helpers in package-local `lib/` or `stores/`.
- Keep widget rendering logic separate from full page rendering logic.

## Source-of-truth workflow

The correct package lifecycle is:

1. Edit the GitHub source repo.
2. Build the release artifact.
3. Publish a GitHub release.
4. Submit or update through Marketplace.
5. Let Modula refresh runtime, surfaces, Board, and registries.

Do not treat the installed runtime copy as the authoring source.
