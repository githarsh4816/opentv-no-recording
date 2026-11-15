# OpenTV 0.11.10 — recording-disabled build

This fork removes recording controls from the player and guide, removes the Recordings navigation tab and Recording Settings entry, and disables the recording foreground service and recording alarm receiver in the Android manifest.

Live TV, VOD, EPG, catch-up, favourites, reminders, and auto-switch reminders are retained.

The recording implementation/database source files are retained to minimize unrelated changes. This is a UI-level removal plus manifest-level disabling of the recording service/receiver, not a deletion of every recording-related class.
