# TMS Android App

This app opens your TMS portal (tms_Portal_v4_1.html) inside Android.
Your HTML and Apps Script are NOT changed. Same login, same data, same Apps Script URL.

Phone features added: GPS, camera / photo upload, Excel download (saved in Downloads), bill print.

## Easiest way to get the APK (no Android Studio)
1. Create a new GitHub repository (private is fine).
2. Upload ALL files of this folder (keep the folder structure, include the hidden `.github` folder).
3. Open the repository -> Actions tab -> "Build APK" -> Run workflow.
4. After ~5 minutes open the finished run -> Artifacts -> download "TMS-apk" -> unzip -> app-debug.apk
5. Send app-debug.apk to the phone (WhatsApp / Drive), tap it, allow "Install unknown apps", install.

## With Android Studio
1. File -> Open -> select this folder, wait for Gradle sync.
2. Build -> Build APK(s). File is in app/build/outputs/apk/debug/app-debug.apk

## Update the portal later
Replace app/src/main/assets/index.html with the new HTML file (keep the name index.html),
then build again. Increase versionCode / versionName in app/build.gradle.kts.

## Notes
- Internet is required (same as the web version).
- Only Android 10 or newer (minSdk 29).
- GPS tracking works while the app is open, same as in a browser.
- This is a debug APK for direct install. For Google Play a signed release build is needed.
