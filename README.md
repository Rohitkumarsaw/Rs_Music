# Rs Music

**Offline music player. Your library, your rules.**  
No account. No ads. No analytics. No `INTERNET` permission. Every song stays on your device.

![Version](https://img.shields.io/badge/version-1.0.0-cyan) ![Android](https://img.shields.io/badge/Android-7.0%2B-green) ![Offline](https://img.shields.io/badge/100%25-offline-blue) ![Ads](https://img.shields.io/badge/ads-none-brightgreen) ![License](https://img.shields.io/badge/license-freeware-lightgrey)

---

## ✨ Features

- **Background playback** — media notification, lock-screen controls, headset / Bluetooth buttons and audio focus (auto-pause on calls)
- **Full local library** — songs, albums, folders, playlists, artists, genres, recently added, recently played and most played
- **Instant search & sort** — find by title, artist, album or filename; sort by name, date, duration or size
- **Playback controls** — play/pause, next/previous, seek, `+/-10s` skip, shuffle, repeat and **0.5x–2.0x** speed
- **Queue with persistence** — drag to reorder, jump to any track, and resume your queue after restarting the app
- **Sleep timer** — 5/10/15/30/45 minutes or 1 hour with a live countdown
- **Themes** — Light, Dark, pure black AMOLED, Follow system, Material You and custom accent colours
- **Synced lyrics** — reads `.lrc` lyrics (imported, sidecar or embedded) and highlights the current line
- **Tag & artwork editor** — edit title, artist, album, genre and year, or change the cover image
- **Backup & restore** — export playlists and settings to local files and import them again
- **Zero ads, zero tracking** — no third-party SDKs, no cloud, no telemetry

> **Privacy note:** the app has **no `INTERNET` permission**. It does declare `ACCESS_NETWORK_STATE`, which only lets it check whether a network is available — it never sends your library anywhere.

---

## 📸 Screenshots

| Player | Library | Playlists |
|---|---|---|
| ![Player](screenshots/01_player.jpg) | ![Library](screenshots/02_library.jpg) | ![Playlists](screenshots/03_playlists.jpg) |

| Folders | Themes |
|---|---|
| ![Folders](screenshots/04_folders.jpg) | ![Themes](screenshots/05_themes.jpg) |

---

## 📥 Download

| Source | Link |
|---|---|
| **Direct APK (universal)** | [Download v1.0.0 APK](https://github.com/Rohitkumarsaw/Rs_Music/releases/download/v1.0.0/app-release.apk) |
| Release page / changelog | [GitHub release v1.0.0](https://github.com/Rohitkumarsaw/Rs_Music/releases/tag/v1.0.0) |
| Uptodown | Coming soon (review pending) |
| Google Play | Coming soon |

**Version:** `1.0.0` · **Size:** `30.5 MB` · **Android:** `7.0+` · **Architectures:** `arm64-v8a`, `armeabi-v7a`, `x86_64`

The APK is **universal** — it runs on virtually every modern Android device, including x86 emulators. Play Console receives the signed AAB instead.

---

## 🛠️ Install (from APK)

1. Download `app-release.apk`
2. Open the file; allow **Install unknown apps** for your browser/file manager when prompted
3. Grant **audio/media** access once (and notifications if you want playback controls)
4. Your local songs appear automatically — no sign-in, no setup wizard

> Updating from an older version? Keep a backup of your playlists first. If the installer reports a signature conflict, uninstall the old version first (this removes local app data).

---

## 🔐 Privacy & permissions

Rs Music contains **no `INTERNET` permission** — it cannot transmit your music, playlists or settings.

| Permission | Why |
|---|---|
| `READ_MEDIA_AUDIO` / `READ_EXTERNAL_STORAGE` (maxSdk 32) | Read your local songs |
| `WRITE_EXTERNAL_STORAGE` (maxSdk 29) | Older Android tag/artwork writes |
| `POST_NOTIFICATIONS` | Playback notification with controls |
| `FOREGROUND_SERVICE` / `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Keep audio playing with the screen off |
| `WAKE_LOCK` | Stable playback |
| `ACCESS_NETWORK_STATE` | Check connectivity only — **no data is sent** |

| Never collected | Never used |
|---|---|
| Personal information | Ads / ad identifiers |
| Device identifiers | Analytics / crash reporting |
| Location, contacts, photos | Cookies or trackers |
| Usage data | Cloud sync or third-party services |

All playlists, settings and library state stay in Android private app storage. Exported backup files are ordinary local files you control. Uninstalling the app removes its local data; delete exported backups yourself if you no longer need them.

---

## 📋 Technical details

| Field | Value |
|---|---|
| Package | `com.rsmusic.rs_music` |
| Version name / code | `1.0.0` / `1` |
| Min SDK / Target SDK / Compile SDK | `24` / `36` / `37` |
| APK SHA-256 | `F099CDD032FE3AF512E6EA18FC28661F3E12E88C302EFBEB32B4FDDEE63FC625` |
| Signing certificate SHA-256 | `E7:88:28:17:DA:0D:9F:C8:0A:ED:A6:95:27:C8:34:4E:8C:1B:92:F7:F9:C4:05:5A:E1:94:6F:E6:BA:45:C1:91` |
| Developer | Rohit Kumar · RS STUDIOZ |

Verify the downloaded APK:

```powershell
Get-FileHash .\app-release.apk -Algorithm SHA256
```

---

## 🧱 Build from source

```bash
cd Rs_Music
flutter pub get
flutter build apk --release          # universal APK
flutter build appbundle --release    # signed AAB for Play Console
```

Requirements: Flutter SDK, Android SDK, JDK and your own signing configuration.

> Do **not** run `flutter clean` on this project. The Gradle memory settings are intentionally tuned for a low-RAM machine (`-Xmx1536m`, `org.gradle.workers.max=1`, `kotlin.daemon.jvmargs=-Xmx768m`).

**Signing material (`key.properties`, keystore) is never committed to this repository.** Keep it offline only.

---

## 📁 Repository structure

```text
.
├── index.html              # 3D landing page (rename the downloaded HTML to this)
├── README.md               # this file
├── screenshots/            # app screenshots used above
├── app-release.apk         # universal release APK (or host it and link above)
└── privacy-policy.html     # optional public policy copy
```

---

## 📫 Contact

Bug reports, feedback or privacy questions:  
**dellofficial795@gmail.com**

---

## 📄 License

Rs Music is **free to use**. Source code and branding are proprietary; redistribution of modified builds under the same name is not permitted.

---

<p align="center">Made for people who just want to press play.</p>
