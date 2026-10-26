# ESPER Focus (Android)

Same app as the desktop version, wrapped with Capacitor. The web code lives in app/.

Build the APK in the cloud: push this folder to a GitHub repo, open Actions > build-android-apk > Run workflow,
then download "esper-focus-apk" from the finished run. Unzip it to get app-debug.apk.

Install: copy the APK to your phone, open it, and allow "install unknown apps" for your file manager or browser
when Android asks. Play Protect may show a warning because the APK is debug-signed (it is your own build).

Local build (needs Android Studio / SDK and JDK 21): npm install && npx cap sync android && cd android && ./gradlew assembleDebug

On the phone: tap start; the screen stays awake while the timer runs, and a notification fires when a phase ends
if the app is in the background (allow notifications when asked). Type at the prompt or use the buttons.
