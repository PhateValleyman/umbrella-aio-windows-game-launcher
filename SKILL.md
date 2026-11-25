# Umbrella AIO Windows Game Launcher — Project Skill

## Mission
Maintain an Umbrella-branded Android fork of Winlator, preserving the upstream Windows compatibility stack while adding a controller-first game-library experience inspired by the Xbox 360 Aurora dashboard.

## Authority and safety
- The project owner decides product direction and approves scope changes.
- Treat upstream code, third-party components, binaries, and license notices as separate provenance domains.
- Never remove copyright, attribution, license, or source-offer notices.
- Do not claim a build, test, device run, or release succeeded without recorded evidence.
- Do not overwrite user data, container images, game files, or existing settings during development tests.
- Prefer small, reversible commits. Inspect the current tree and relevant implementation before editing.
- Do not introduce analytics, telemetry, account sync, or network services without explicit approval.

## Repository roles
- Main repository: `PhateValleyman/umbrella-aio-windows-game-launcher`.
- Android application submodule: `PhateValleyman/-umbrella-winlator-app-`.
- Upstream application: `brunodev85/winlator-app`.
- Upstream main project: `brunodev85/winlator`.
- Other upstream submodules remain `brunodev85/vortek` and `brunodev85/gladio`.

## Required workflow
1. Inspect repository status, branch, recent commits, submodule pointers, and the relevant source before changes.
2. Reproduce the issue or record the baseline behavior.
3. Diagnose the cause; separate observations from hypotheses.
4. Make the smallest change that addresses the diagnosed cause.
5. Verify formatting, compilation, static checks, and relevant behavior where available.
6. Record tests actually run, device/ABI used, limitations, and any unverified behavior.
7. Keep commits focused and explain the rationale.

## Android constraints
- Primary development/test target: ARM64 Android, API 34.
- Preserve the upstream ARM64 native ABI unless a deliberate architecture change is approved.
- Do not change package ID, namespace, authorities, permissions, or exported components without a full reference audit and upgrade/migration plan.
- Validate native build configuration and packaged libraries before claiming APK compatibility.

## UI direction
- Umbrella industrial black/red visual identity.
- Controller-first navigation, large readable focus states, horizontal game browsing, cover art, game details, and library organization.
- Aurora-inspired interaction patterns are a reference, not a license to copy proprietary assets or branding.
- Preserve core Winlator container management and launch workflows.

## Documentation
Keep `docs/ARCHITECTURE.md`, `BUILD.md`, `UPSTREAM.md`, `LICENSES.md`, and `ROADMAP.md) current when architecture, build, provenance, licensing, or scope changes.
