# StreameX Android Wrapper

Minimal Capacitor Android shell for https://streamex.hn/.

- Package: `com.streamex.app`
- App name: `StreameX`
- Live website remains the UI/content source.
- Native Android back navigation.
- Native HTML5 fullscreen video handling with landscape/portrait switching.
- External HTTP(S)/mailto/tel destinations use Android intents.
- Only `INTERNET` permission is declared.

## Build locally

```bash
npm install
npm run build
npx cap sync android
cd android
./gradlew assembleDebug
```

## Build from an Android phone with GitHub Actions

This repository includes `.github/workflows/build-android.yml`.

1. Create a GitHub repository and upload this entire `streamex-app` folder.
2. Open the repository's **Actions** tab.
3. Select **Build StreameX APK**.
4. Tap **Run workflow** (the workflow also runs automatically when you push to `main` or `master`).
5. Wait for the green checkmark.
6. Open the completed workflow run and download the **StreameX-debug-apk** artifact.
7. Extract the artifact and install `app-debug.apk` on the Android phone.

The GitHub runner installs Node.js, Java 21, Android API 36/build tools, and Gradle 8.14.3 automatically. No Android Studio or local Android SDK is required on your phone.
