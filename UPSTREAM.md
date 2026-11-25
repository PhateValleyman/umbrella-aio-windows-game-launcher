# Upstream and Fork Policy

## Sources
- Main upstream: https://github.com/brunodev85/winlator
- Android app upstream: https://github.com/brunodev85/winlator-app
- Vortek upstream: https://github.com/brunodev85/vortek
- Gladio upstream: https://github.com/brunodev85/gladio
- Official project website: https://www.winlator.org/

## Forks
- Umbrella main: https://github.com/PhateValleyman/umbrella-aio-windows-game-launcher
- Umbrella Android app: https://github.com/PhateValleyman/-umbrella-winlator-app-

## Submodules
The root repository's `app` submodule is configured to use the Umbrella application fork. Vortek and Gladio continue to track their upstream repositories. The submodule gitlinks pin exact commits; branch names in `.gitmodules` do not automatically advance those pins.

## Sync policy
- Fetch upstream changes and review release notes, commits, and submodule changes before syncing.
- Use a dedicated upstream-sync branch.
- Do not force-push or rewrite shared history.
- Preserve Umbrella changes as focused commits and resolve conflicts deliberately.
- Update submodule pointers only after the target commit is fetched and reviewed.
- Record the upstream tag/commit used for every release.

## Baseline
The initial fork was based on Winlator 11.2 / tag `v11.2.0` (verify the exact local gitlink and commit before building).
