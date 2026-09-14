# NoDeadAir

Watch a wall of live streams in one window. Get told the moment someone you follow goes live.
Clip the good part with one key.

Twitch and Kick, side by side, without a browser tab per stream.

### [⬇ Download for Windows](../../releases/latest)

Windows 10 or 11, 64-bit. Unzip anywhere and run it — nothing installs, and deleting the folder
removes it completely.

---

## Getting started

**Sign in.** A welcome window opens the first time. Twitch and Kick load their own login pages
inside the app, so your password never touches NoDeadAir.

**Fill the grid.** Press *Add my live follows* and the people you follow who are live right now
appear as tiles. Or type any channel name to add it yourself.

**Watch.** Click a tile to focus it — full quality and sound, everything else drops back and stays
muted. Chat sits beside it.

**Clip it.** Press `C` and the moment is saved to your Library, ready to trim.

| | | | |
|---|---|---|---|
| `1`–`8` pick a tile | `C` clip | `M` mute | `S` solo |
| `G` grid / focus | `F` following | `L` library | `R` trim your last clip |

---

## Don't want to sign in?

You don't have to. Add channels by name and watching, chat reading, grid and focus all work
straight away.

Signing in only unlocks the things that need your account: your Following list, sending chat
messages, went-live alerts, and clipping.

---

## A note on trust

This app isn't code-signed, so Windows will show **"Windows protected your PC"** the first time.
Choose *More info → Run anyway*. That warning appears for every unsigned program and says nothing
about what's inside.

Since you're being asked to trust an unsigned download, every release ships with:

- a **SHA-256 checksum**, so you can confirm your download matches what was published
- **VirusTotal scans** of both the zip and the app itself, with any detections named in the release
  notes rather than glossed over
- **`SECURITY-PASS.md`** inside the zip — plain-English notes on what the app does, what it
  deliberately doesn't, and where it keeps things

NoDeadAir reads your browser's cookie storage on purpose, so it can reuse your existing Twitch and
Kick login instead of asking for a password. That's a common antivirus heuristic, and combined with
being unsigned it's why a scanner may occasionally flag it.

Your Twitch and Kick sign-in is stored by the Edge browser component built into Windows,
encrypted for your user account. NoDeadAir never writes your login to a file of its own.

---

## Where things go

| | |
|---|---|
| The app | wherever you unzipped it |
| Your clips | `Videos\NoDeadAir Clips` — change it in Settings |
| Settings and logs | `%APPDATA%\NoDeadAir-Fork` |

FFmpeg ships alongside for trimming clips. Licences are in the zip.

---

*A hobby project, shared with a few people. Not affiliated with Twitch or Kick.*
