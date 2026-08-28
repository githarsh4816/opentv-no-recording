# Build the patched OpenTV APK with GitHub Actions

1. Create a new PRIVATE GitHub repository.
2. Upload all files/folders from this project to the repository.
3. Open the repository's **Actions** tab.
4. Select **Build OpenTV APK**.
5. Click **Run workflow**.
6. Wait for the workflow to finish.
7. Open the completed workflow run.
8. At the bottom, under **Artifacts**, download `opentv-recording-disabled`.
9. Extract the downloaded artifact; the APK inside is the recording-disabled build.

The workflow uses GitHub's hosted Ubuntu runner, JDK 17, Android SDK API 35, and the project's Gradle wrapper. No Android Studio is required on your PC.
