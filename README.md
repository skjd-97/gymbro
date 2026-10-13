# GymBro — Android APK

GymBro is an Android wrapper for the supplied GymBro Offline Workout Tracker HTML app.

## Build the APK using GitHub (no PC build tools required)
1. Sign in to GitHub and create a **new public repository** named `GymBro`.
2. Upload all files and folders from this project ZIP (including `.github/workflows/build-apk.yml`). On GitHub's mobile site, you may need to use the browser's **Desktop site** option to upload folders; alternatively upload files individually while preserving paths.
3. Open the repository's **Actions** tab.
4. Select **Build GymBro APK** → **Run workflow**.
5. Wait for the workflow to finish successfully.
6. Open the completed workflow run, scroll to **Artifacts**, and download `GymBro-debug-APK`.
7. Extract the downloaded artifact ZIP; it contains `app-debug.apk`. Install it on Android. Android may ask you to allow installing apps from that browser/file manager.

## What is included
- `www/index.html` — the original GymBro tracker interface and JavaScript.
- `capacitor.config.json` — app identity and web assets configuration.
- `.github/workflows/build-apk.yml` — GitHub Actions workflow to compile and publish the APK as an artifact.

## Notes
- The generated APK is a **debug APK**, suitable for testing and sharing. It is not a Play Store release build.
- Anyone with access to the repository can get the source. Anyone you share the APK artifact with can install it, subject to Android security settings.
- The supplied HTML loads Tailwind CSS, Font Awesome, and Google Fonts from external CDNs, so some styling/icons/fonts may need internet on first use or when those assets are unavailable. Workout history is stored locally in the app's WebView storage and is not automatically synced between phones.
- Before a public release, test on several Android devices and consider creating a signed release APK.
