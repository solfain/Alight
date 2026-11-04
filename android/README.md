# Android wrapper

This is a small native Android WebView shell for the Open Motion browser editor. It packages the root `index.html`, PWA manifest, service worker, and icons into the APK at build time; the web editor itself remains in the repository root.

## Build

The GitHub Actions workflow `.github/workflows/android-apk.yml` builds a sideloadable debug APK and uploads it as the `open-motion-android-debug-apk` workflow artifact. A local build needs JDK 17, Android SDK platform 35/build-tools 35.0.0, and Gradle 8.9:

```sh
gradle --no-daemon -p android :app:assembleDebug
```

The generated APK is at `android/app/build/outputs/apk/debug/app-debug.apk`.
