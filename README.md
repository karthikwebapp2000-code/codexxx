# codexxx - build steps

1. Put your photo at `www/assets/photo.jpg` (square, 1024x1024) and a copy at `assets/icon-only.png`.
2. Install Node.js, then run:  npm install
3. Create icons:   npx capacitor-assets generate
## Android APK
   npx cap add android
   npx cap sync
   npx cap open android   -> Android Studio: Build > Build APK(s)
   (Play Store: Build > Generate Signed Bundle, use .aab)
## iOS (needs a Mac + Xcode + Apple Developer account, $99/yr)
   npx cap add ios
   npx cap sync
   npx cap open ios       -> Xcode: Product > Archive > Distribute App > App Store Connect
## Notes
- Apple may reject apps that are only a website wrapper; codexxx works offline, which helps.
- Change appId in capacitor.config.json to your own, e.g. com.yourname.codexxx.
