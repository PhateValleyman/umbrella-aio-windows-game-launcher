# Build and Verification

## Status
This document records the upstream baseline only. A reproducible Umbrella build has not yet been established.

## Upstream baseline
The application Gradle configuration currently declares:
- Namespace and application ID: `com.winlator`
- Compile SDK: 35
- Minimum SDK: 26
- Target SDK: 28
- Version: 11.2 (versionCode 33)
- NDK: 24.0.8215888
- CMake: 3.22.1
- Debug ABI filter: `arm64-v8a`

These values were read from `app/build.gradle` in the application fork. Confirm all variants and native build tasks before treating them as a complete build matrix.

## Build prerequisites
Use the Gradle wrapper and the exact Android Gradle Plugin/JDK/SDK/NDK versions declared by the checked-out source. Do not upgrade toolchains as part of an unrelated branding change.

## Initial verification sequence
1. Record `git status --short`, branch, commit, and submodule status.
2. Initialize submodules recursively and record their pinned commits.
3. Inspect Gradle wrapper, plugin versions, local SDK/NDK availability, and native CMake configuration.
4. Run Gradle configuration and dependency resolution.
5. Build the unmodified debug APK.
6. Inspect the APK package ID, manifest, native libraries, and ABI contents.
7. Install and test on a supported ARM64 Android device only after the build passes.

## Evidence
For each run, record the exact command, toolchain versions, exit status, artifact path, target ABI, and device/OS if physical testing occurred. A successful host build is not proof of successful device execution.
