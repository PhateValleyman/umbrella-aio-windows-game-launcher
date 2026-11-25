# Roadmap

## P0 — Repository and build baseline
- [x] Verify both GitHub repositories are accessible.
- [x] Point the root `app` submodule URL at the Umbrella app fork.
- [ ] Verify fork parent metadata and exact submodule gitlinks.
- [ ] Establish a reproducible unmodified debug build.
- [ ] Record a baseline APK and runtime smoke-test results.

## P1 — Umbrella identity
- [ ] Create original Umbrella launcher icon and adaptive icon assets.
- [ ] Create splash/launch screen assets.
- [ ] Define colors, typography, spacing, focus, and controller states.
- [ ] Add branding without removing upstream credits or legal notices.

## P2 — Aurora-inspired dashboard
- [ ] Inspect existing Activity/navigation architecture.
- [ ] Prototype horizontal coverflow and focus transitions.
- [ ] Implement D-pad/confirm/back navigation.
- [ ] Preserve access to existing Winlator workflows.

## P3 — Game library
- [ ] Define a versioned local game metadata model.
- [ ] Display cover art with offline fallback.
- [ ] Add favorites, categories, and recently played.
- [ ] Connect entries to existing Winlator shortcuts/containers.

## P4 — Integration and profiles
- [ ] Add game detail view and safe launch handoff.
- [ ] Add per-game presets only where existing APIs permit.
- [ ] Verify container settings and launch behavior remain unchanged.

## P5 — Controller and device validation
- [ ] Test D-pad, confirm, back, shoulders, and focus restoration.
- [ ] Test handheld and external-display layouts.
- [ ] Run on the target ARM64 Android device.

## P6 — Release readiness
- [ ] Complete license/SBOM audit.
- [ ] Document build and reproducible release steps.
- [ ] Produce release notes and rollback guidance.
