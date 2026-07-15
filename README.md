# Nova Ludo

Offline pass-and-play Ludo for 2, 3, or 4 players on one device — built as a
web app and packaged into an installable Android APK using Capacitor +
GitHub Actions (no Android Studio needed on your computer).

## How to get the APK on your phone

1. Create a new repository on GitHub, e.g. `nova-ludo`.
2. Upload every file in this folder to that repo, keeping the folder structure:
   ```
   nova-ludo/
   ├── www/
   │   └── index.html
   ├── package.json
   ├── capacitor.config.json
   └── .github/
       └── workflows/
           └── build-apk.yml
   ```
   Use **Add file → Upload files** on GitHub and drag the whole folder in,
   then commit to the `main` branch.

3. Go to the **Actions** tab in your repo — a "Build APK" run starts
   automatically. Wait for the green checkmark (~2–4 minutes).

4. Open that run, scroll to **Artifacts**, and download
   **nova-ludo-debug-apk**. Unzip it to get `app-debug.apk`.

5. Send `app-debug.apk` to your phone (Google Drive, email, USB) and tap it
   to install. The first time, Android will ask you to allow "install
   unknown apps" for whichever app you opened the file with — approve that.

That's it — you can now play offline pass-and-play Ludo with friends on your
phone, no internet required to play.

## Making changes later

Edit `www/index.html` and push the change — the Actions workflow rebuilds
the APK automatically every time.
