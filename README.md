# HellBrowser

**HellBrowser — a modern Android WebView browser with an automotive-focused interface.**

> **Safety:** Use HellBrowser only as a passenger or while safely parked. Never browse while driving.

## Requirements

- Android 15 (API 35) or newer
- Android Studio with a compatible JDK (the project targets Java/Kotlin 21)
- Internet access for Gradle dependency downloads on the first build

## What HellBrowser does

- Web browsing with Android WebView
- Multiple browser tabs
- Bookmarks and quick links
- Custom start/home page
- Mobile and desktop site modes
- Light and AMOLED-style dark themes
- Optional page darkening
- Configurable URL bar and quick-action controls
- Global display scaling
- Cached site icons
- Microphone and location permissions for supported websites
- Fullscreen web media support
- Android Auto / automotive integration
- Browser site-data and permission controls

## Build locally

1. Clone this repository.
2. Open it in Android Studio.
3. Allow Gradle to download the required dependencies.
4. Run the `app` configuration on an Android 15+ device/emulator.
5. For an APK, run:

```bash
./gradlew assembleDebug
```

## Build automatically on GitHub

The repository includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`.

After pushing the project to GitHub:

1. Open **Actions**.
2. Select **Build HellBrowser APK**.
3. Run the workflow or push a commit to trigger it.
4. Open the completed workflow run.
5. Download the generated APK from **Artifacts**.

### Before enabling release/update features

Replace `hel1xasura-hell` in the project with your actual GitHub username. In particular, configure the repository URL used by the in-app update checker and optional sponsor link.

## GitHub repository setup

Create a repository named `HellBrowser`, then upload the **contents** of this project folder (not the ZIP file itself):

```text
HellBrowser/
├── .github/workflows/build-apk.yml
├── app/
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
├── gradlew
├── gradlew.bat
└── README.md
```

After the first push, GitHub Actions can build the APK without requiring a paid build service.

## Application identity

- App name: **HellBrowser**
- Application ID: `com.hellbrowser.app`
- Minimum Android version: **Android 15 / API 35**
- Target Android version: **API 37**
- Current version: **2.2**

Changing the application ID means Android treats HellBrowser as a separate application from the old package. Existing installations using the old package will not be upgraded by this APK.

## Privacy and permissions

HellBrowser uses Android WebView to display websites. The application requests only the Android permissions needed by its browser/automotive features, including Internet access, microphone access, location access, notifications, and Android Auto surface access.

Websites loaded inside the browser can request supported WebView permissions. Review each permission request before allowing it.

**HellBrowser — browse when you're parked.**
