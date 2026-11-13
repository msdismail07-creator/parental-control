# Parental Control - APK build

## Easiest: build the APK online (no Android Studio)
1. Create a free GitHub account and a new repository.
2. Upload everything in this folder to it (keep the .github folder).
3. Open the Actions tab, run "Build APK" (it also runs on every push).
4. After about 5 minutes open the finished run and download "parental-control-apk".
5. Unzip, copy app-debug.apk to your phone, allow "Install unknown apps" and install.

## Or build on your PC (Android Studio)
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android
Then in Android Studio: Build > Build APK(s).

## ESP32 side
Advertise a BLE service 0000ffe0-0000-1000-8000-00805f9b34fb with a notify
characteristic 0000ffe1-0000-1000-8000-00805f9b34fb, sending text like
13.08270,80.27070,82  (lat,lon,battery%) every second.

## Notes
- This is a debug APK, fine for your own phones. A Play Store release needs a signed release build.
- Edit www/index.html to change the app, then push again.
