# XR Desk 3.5.0 (preview)

*Released: 2026-10-12*

The first public preview of XR Desk: your Android phone on your Windows PC, as one screen window or as one window per app.

## What is new
- **Phone screen window** with mouse and keyboard control, aspect-locked resize, rotation support and a side bar (Multi window, Sound, Volume up / down, Phone screen on / off).
- **Multi window**: apps you open on the phone get their own windows, with the app's name and icon and their own taskbar buttons. A window closes when its app is closed on the phone; closing a window removes the app from the phone's Recents.
- **App window title bar**: Sound on / off for each window, Mobile / Desktop mode (portrait / landscape), Free resize (preview).
- **Sound forwarding** that is really switched on and off on the phone (nothing is captured while it is off), and a separate **Device Sound** switch for the phone's speaker.
- **Main window**: phone list with model names, Refresh, Play / Stop, Logs card that shows everything XR Desk does.
- **Free version: up to 3 app windows** for one phone. A fourth app stays on the phone and a popup says: *You can create 3 windows as a free user. Please buy Premium or close an app window.*
- **Update Check**: a window that checks GitHub Releases, asks before it downloads, shows percent, size and speed, and verifies the installer with its SHA-256.
- The **About** and **Buy Premium** buttons open the author's Telegram page.
- **Installer** for Windows: per-user, no administrator, with adb, the scrcpy server, Qt and FFmpeg included.
- Everything XR Desk starts on the phone is removed again when you stop or close it (no leftover server files, tunnels or extra screens).

## Not ready yet (marked *Coming soon* in the program)
Install XR Desk APK, Get Premium, Check Device Status, Setup Device, Unlock Screen, Show Screen, Launch Cloner, Launch 2nd Space.

## Known limits
- Tested only on a Samsung Galaxy A22 (Android 13), Windows 10 / 11.
- Fingerprint and screen-lock prompts and other secure screens cannot be shown in an app window. Switch *Multi window* off and use the phone screen window for them.
- The sound is the phone's whole media sound, not per app.
- USB connection only.
- The installer is not code-signed, so Windows SmartScreen may warn (*More info > Run anyway*).

## How to connect
Turn on *USB debugging* in the phone's Developer options, connect by USB cable, tap **Allow** on the phone, start XR Desk, pick the phone, press **Play**. Details are in the [README](README.md#connect-your-phone).

## Download
Download **XRDesk-Setup-3.5.0.exe** from the assets below and run it. You can check its SHA-256 against the `.sha256` file next to it.
