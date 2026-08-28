# OpenTV 0.11.7 — recording-disabled build

This source tree is modified to make recording/DVR unavailable from the user interface and to prevent scheduled recording services from being started.

Changes:
- Removed the Record button from the live player.
- Removed the quick-record button from the guide preview.
- Removed recording actions from the channel menu.
- Removed the Recordings tab.
- Removed the Recording settings entry/route.
- Disabled the recording foreground service and recording alarm receiver in AndroidManifest.xml.
- Removed startup re-arming of scheduled recordings.
- Kept IPTV playback, EPG, favourites, VOD, catch-up and normal playback intact.

The recording implementation source files are intentionally retained so this remains a small, maintainable fork and the database schema does not need to be changed.

Build:
1. Install JDK 17 and Android SDK/API 35.
2. From this directory run:
   `./gradlew :app:assembleDebug`
3. APK output:
   `app/build/outputs/apk/debug/app-debug.apk`

I could not perform the Gradle build in this environment because the Gradle 8.11.1 distribution is not cached and this environment cannot reach services.gradle.org.
