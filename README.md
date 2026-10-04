# O/L Sprint — Android starter

This package wraps the current O/L Sprint browser prototype in a Capacitor Android shell and includes a GitHub Actions workflow to build a debug APK in the cloud. You can do the setup from an Android phone using a browser; you do not need Android Studio locally.

## What is included
- `www/index.html`: the current working prototype (MCQ practice, written practice, custom questions and local progress).
- `www/manifest.webmanifest` and `www/sw.js`: installable/offline-friendly web-app support.
- `capacitor.config.json` and `package.json`: Capacitor wrapper setup.
- `.github/workflows/build-android.yml`: cloud APK build workflow.

## Build the APK using only your phone
1. Sign in to GitHub and create a **new empty repository** named `ol-sprint` (a free account is fine). Do not add a README or licence during creation.
2. Upload the contents of this ZIP to the repository, making sure `.github/workflows/build-android.yml` is included. If GitHub's mobile upload interface hides dot-folders, use GitHub's website in your browser with Desktop site enabled, or create the workflow file through **Add file → Create new file** at `.github/workflows/build-android.yml`.
3. Open the repository's **Actions** tab and enable Actions if prompted.
4. Select **Build O-L Sprint Android APK**, tap **Run workflow**, then run it on `main`. A push to `main` also triggers a build.
5. When the run finishes successfully, open that run, scroll to **Artifacts**, and download `ol-sprint-debug-apk`. Extract the ZIP to obtain `app-debug.apk`.
6. Open the APK on your Android phone and allow installation from that browser/file manager if Android asks. Only install APKs you built from a repository you control.

## Important notes
- This is a **debug APK**, suitable for testing, not a signed release for Google Play.
- A Google Play release requires a release signing key, package/version setup, testing, a Play Console developer account and compliance with current Play policies. Play Console registration may have a fee; do not assume publishing can be completely free.
- This is a starter build, not a complete official past-paper library. Sample questions are practice examples, not claimed to be official past-paper questions. Verify exam content against Sri Lankan syllabus materials and marking schemes.
- Progress and custom questions are currently stored locally in the app/browser storage. There is no account or cloud sync. Export a backup from the app before clearing its data.
- To keep the project safe, review the source before building and never commit passwords, signing keys or other secrets.
