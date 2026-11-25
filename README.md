# Rootless 7ths — Android app

A small Android app that wraps the chord chart (`app/src/main/assets/index.html`)
in a full-screen WebView. Works offline; tap any grid to hear it.

## Get the APK without installing anything (GitHub)
1. Create a new GitHub repository and upload the contents of this folder
   (including the hidden `.github` folder).
2. Open the repo's **Actions** tab. The "Build APK" job runs on every push
   (or press **Run workflow**). It takes about 3–4 minutes.
3. Open the finished run and download **RootlessChords-apk** (a zip holding `app-debug.apk`).

## Or build in Android Studio
Open this folder in Android Studio (Hedgehog or newer), let it sync, then
**Build ▸ Build APK(s)**. The file appears in `app/build/outputs/apk/debug/`.

## Install and share
- Copy `app-debug.apk` to the phone and open it. Android asks once to allow
  installs from that source (Files app, Drive, etc.).
- To share, send the same APK file to anyone; they install it the same way.
- The debug build is signed with a development key, which is fine for
  personal sharing. For the Play Store, create a signed release build
  (Build ▸ Generate Signed App Bundle).

## Updating the chart
Replace `app/src/main/assets/index.html` and bump `versionCode` in `app/build.gradle`.
