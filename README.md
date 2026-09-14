# NoDeadAir — downloads

One window that watches many live streams at once, tells you the moment someone you follow goes
live, and clips the good part with one key. Twitch and Kick, side by side, without a browser tab
per stream. Windows 10/11, 64-bit.

**This repository holds downloads only — no source code.** It exists so the build can be shared
without publishing the project.

## Get it

**[Download the latest release →](../../releases/latest)**

Unzip anywhere and run `NoDeadAir.App.exe`. Nothing installs: no Program Files, no registry, no
service. Delete the folder and it is gone.

## Before you run it

The executable is **not code-signed**, so Windows will show *"Windows protected your PC"* on first
launch — **More info → Run anyway**. Some antivirus tools also flag unsigned programs that can read
a browser's cookie file, which this one does in order to reuse your Twitch/Kick login.

Because you are being asked to trust an unsigned binary, every release includes:

- a **SHA-256** checksum, so you can prove the file you downloaded is the file that was published;
- a **VirusTotal** link for that exact file;
- **`SECURITY-PASS.md`** inside the zip, describing precisely what the build does and does not do,
  and where it keeps your sign-in.

Verify the checksum in PowerShell before running anything:

```powershell
Get-FileHash .\NoDeadAir-v<version>-share.zip -Algorithm SHA256
```

If that value does not match the one in the release notes, do not run it.

## First run

1. A welcome window opens with **Sign in to Twitch** and **Sign in to Kick**. The platforms' own
   login pages load inside the app — NoDeadAir never sees your password. You do not need to add
   any channels first.
2. Press **Add my live follows** and the grid fills with people you follow who are live now.
3. Or skip signing in entirely and add channels by name — playback, chat reading, grid and focus
   all work signed out. Sign-in is only needed for your Following list, sending chat, went-live
   alerts, and clipping.

Keys, once you have tiles: `1`–`8` select · `C` clip · `M` mute · `S` solo · `G` grid/focus ·
`F` Following · `L` Library · `R` Clip Studio · `E` Editor · `Esc` back.

## Where it puts things

| What | Where |
|---|---|
| The app | the folder you unzipped — portable |
| Your clips | `Videos\NoDeadAir Clips\` (changeable in Settings → Clipping) |
| Settings, logs | `%APPDATA%\NoDeadAir-Fork` |
| Your sign-in | `%LOCALAPPDATA%\NoDeadAir\webview`, encrypted by Windows (DPAPI) to your user account |

NoDeadAir never writes your login to its own files. Removing those folders removes everything.

## Bundled software

FFmpeg (gyan.dev essentials build, GPLv3) ships alongside the app and is used only to trim and
probe clips you have already downloaded — never to capture a stream. `NOTICES.txt` and
`FFMPEG-LICENSE.txt` are in the zip.

---

A hobby project shared with a few people. Not affiliated with Twitch or Kick.
