# Recording-disabled OpenTV source variant

This source variant removes the recording feature from the user-facing app:

- Removes the Recordings navigation tab and recordings library screen from the main navigation.
- Removes recording storage settings from the Settings hub and its navigation route.
- Removes the live-player Record/Stop control.
- Removes the guide preview quick-record control and guide recording/scheduling dialogs.
- Removes the recording foreground service and recording alarm receiver from the Android manifest.
- Removes scheduled-series recording rescan triggers from app view-model/sync paths.
- Removes the recording-only exact-alarm and battery-optimisation permissions.
- Leaves normal live TV, movies, series, EPG display, catch-up playback, and programme reminder alarm components in place.

## Scope note

This is a UI/runtime-disabled variant, not a complete deletion of every recording-related Kotlin class, Room entity/DAO, database migration, or unused dependency. Those dormant implementation files remain in the source tree to avoid an unverified database/schema migration in this first pass. The manifest no longer registers the recording service/receiver, and the app no longer exposes recording controls or screens.

## Build

Use the repository's existing GitHub Actions workflow to build the APK. The source has not been compiled in this environment because the Gradle wrapper could not download Gradle 8.11.1 (network DNS unavailable here).
