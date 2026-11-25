# Architecture

## Product boundary
Umbrella AIO Windows Game Launcher is an Android application based on Winlator. Winlator remains responsible for Windows compatibility, Wine/Proton integration, container lifecycle, graphics translation, and game process launch. Umbrella adds the branded shell and game-library experience around those capabilities.

## Repository layout
- Root repository: upstream Winlator integration, submodule pins, project-level documentation, release coordination, and future shared branding assets.
- `app/`: Android application source (Umbrella app fork).
- `vortek/`: upstream Vortek component.
- `gladio/`: upstream Gladio component.
- `docs/`: architecture, build, upstream, licensing, and roadmap records.

## Application layers (planned; verify actual source packages before implementation)
- Dashboard: controller-first home screen and horizontal featured-game browsing.
- Library: local game entries, artwork metadata, favorites, categories, and recently played.
- Game detail: launch action and per-game metadata/settings entry points.
- Winlator integration: adapters around existing container, shortcut, and launch APIs.
- Controller input: D-pad navigation, confirm, back, shoulders/triggers where supported.
- Profiles: optional per-game launch presets; do not duplicate or bypass existing container configuration.
- Settings: Umbrella presentation preferences plus existing Winlator settings.

## Data principles
- Preserve Winlator's existing persistence formats and container data.
- New library metadata should be additive, versioned, and recoverable.
- Artwork caching must be bounded and must not block offline library browsing.
- Do not store storefront credentials or game binaries in the library metadata.
- Any migration must be backward-compatible or provide an explicit backup and rollback path.

## Runtime constraints
The initial target is ARM64 Android. Native compatibility components and their ABI constraints must remain intact. UI work must not change Wine, Box64, graphics drivers, or container behavior unless a separately scoped change requires it.

## Design system
Use an industrial black/charcoal base, Umbrella red accents, restrained hex/carbon texture, high-contrast focus states, and large cover artwork. Keep typography and controls legible at handheld viewing distance and on external displays.
