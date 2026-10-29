# Raudahdata Android app

The app opens https://raudahdata.com/user/index1.php (the phone-style login) inside a branded app:
splash screen, pull-to-refresh, back button, file upload, receipt downloads, WhatsApp/phone links open outside.

## Option A: build the APK from your phone/computer browser (no Android Studio)
1. Create a free account at github.com and make a new PRIVATE repository, e.g. "raudahdata-app".
2. Upload ALL the files and folders from this project (including the hidden ".github" folder).
3. Open the repository > Actions tab > "Build Android app" > Run workflow.
4. Wait about 5 minutes. Open the finished run and download the artifact "Raudahdata-apk" (a zip containing app-debug.apk).
5. Send the APK to a phone, tap it and install (allow "install unknown apps" when asked).

## Option B: Android Studio
1. Install Android Studio, choose Open and select this folder, wait for Gradle sync.
2. Build > Build Bundle(s) / APK(s) > Build APK(s). The file is in app/build/outputs/apk/debug/.

## For Google Play (later)
- Build > Generate Signed Bundle / APK > Android App Bundle. Create a keystore and KEEP IT SAFE with its passwords.
- Use playstore_icon_512.png as the store icon. Google needs a privacy policy web address and a $25 one-time developer account.

## Changing things
- Website address: MainActivity.kt (startUrl and siteHost).
- App name: app/src/main/res/values/strings.xml.  Colours: values/colors.xml.
- Version: app/build.gradle.kts (versionCode / versionName). Raise versionCode for every update you upload to Play.
