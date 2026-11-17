# Journal App

Contents:
- www/ -> the web app (index.html, manifest, service worker, icons)
- package.json + capacitor.config.json -> to build a real Android app (APK)

## Option 1: Quick (PWABuilder / hosting)
1. Upload the www folder to any HTTPS hosting (GitHub Pages, Netlify, Vercel).
2. Open the link on your phone -> "Add to Home Screen". Works offline.
3. For an APK: give the link to https://www.pwabuilder.com and choose Android.

## Option 2: Android APK with Capacitor
Needs Node.js and Android Studio.
    npm install
    npx cap add android
    npx cap sync
    npx cap open android
Then in Android Studio: Build > Build APK(s).

## Option 3: Online APK builders (WebIntoApp, Appilix, ...)
Upload the www folder (zipped) and set the name "Journal".

Notes:
- Trading data is stored in localStorage inside the app (per device).
- The news calendar needs internet; everything else works offline.
