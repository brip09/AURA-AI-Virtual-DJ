# AURA DJ – Android APK

Easiest (no Android Studio): 
1. Create a new GitHub repo and push this folder to it.
2. Open the repo's Actions tab, run "Build AURA APK" (it also runs on every push).
3. When it finishes, download the artifact "AURA-DJ-debug-apk", unzip, and copy app-debug.apk to your phone.
4. On the phone, allow "Install unknown apps" for your file manager/browser and tap the APK.

Local build (needs Node 20, JDK 17, Android SDK):
  npm install && npx cap add android && npx cap sync android
  cd android && ./gradlew assembleDebug
  APK: android/app/build/outputs/apk/debug/app-debug.apk

This is a debug-signed APK for sideloading. A Play Store release needs your own signing key (assembleRelease).
Edit www/index.html to change the app.
