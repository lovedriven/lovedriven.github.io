# LoveDriven Ministries staff portal (PWA)

Live site: https://lovedriven.github.io/

## Files
- index.html – the portal (talks to the Apps Script backend)
- manifest.webmanifest, sw.js, offline.html, icons/ – make it an installable PWA
- .nojekyll – lets GitHub Pages serve the `.well-known` folder (needed later for the Android app)

## Make the Android APK/AAB
1. Upload all of these files to the root of the `lovedriven.github.io` repo (replace index.html) and commit.
2. Wait ~1 minute, then open https://lovedriven.github.io/manifest.webmanifest to confirm it loads.
3. Go to https://www.pwabuilder.com, enter https://lovedriven.github.io/ and press Start.
4. Fix nothing red; then Package for Stores > Android.
   - Package ID: org.lovedriven.portal (any reverse-domain name; keep it forever)
   - App name: LoveDriven Ministries Portal; Short name: LoveDriven
   - Signing key: choose "New" and download the zip. KEEP the .keystore file and passwords safe.
5. From the downloaded zip, install the .apk on a phone to test. Use the .aab for Google Play.
6. Add the file `assetlinks.json` from that zip to this repo at `.well-known/assetlinks.json`
   so the app opens full screen without the browser address bar. Commit and wait a minute.
