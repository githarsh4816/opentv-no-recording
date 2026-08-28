# Recording-disabled OpenTV build

This fork disables recording at the user-facing level and disables the recording service and scheduled-recording receiver in the Android manifest.

Recording UI removed from the player, guide, main navigation, and settings. Catch-up and reminders remain available.

Build with GitHub Actions using `.github/workflows/build-apk.yml`.
