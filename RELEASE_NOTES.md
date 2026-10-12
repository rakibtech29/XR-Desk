# XR Desk 3.5.0 (preview)

*Released: 2026-10-12*

The first public preview of XR Desk: your Android phone on your Windows PC, as one screen window or as one window per app.

## What is new
- **Phone screen window** with mouse and keyboard control, aspect-locked resize, rotation support and a side bar (Multi window, Sound, Volume up / down, Phone screen on / off).
- **Multi window**: apps you open on the phone get their own windows, with the app's name and icon and their own taskbar buttons. A window closes when its app is closed on the phone; closing a window removes the app from the phone's Recents.
- **App window title bar**: Sound on / off for each window, Mobile / Desktop mode (portrait / landscape), Free resize (preview).
- **Sound forwarding** that is really switched on and off on the phone (nothing is captured while it is off), and a separate **Device Sound** switch for the phone's speaker.
- **Main window**: phone list with model names, Refresh, Play / Stop, Logs card that shows everything XR Desk does.
- The **About** button opens the author's Telegram page.
- Everything XR Desk starts on the phone is removed again when you stop or close it (no leftover server files, tunnels or extra screens).

## Not ready yet (marked *Coming soon* in the program)
Update Check, Install XR Desk APK, Get Premium, Check Device Status, Setup Device, Unlock Screen, Show Screen, Launch Cloner, Launch 2nd Space.

## Known limits
- Tested only on a Samsung Galaxy A22 (Android 13), Windows 10 / 11.
- Fingerprint and screen-lock prompts and other secure screens cannot be shown in an app window. Switch *Multi window* off and use the phone screen window for them.
- The sound is the phone's whole media sound, not per app.
- USB connection only.
- There is no installer yet. This preview is not code-signed, so Windows SmartScreen may warn.

## How to connect
Turn on *USB debugging* in the phone's Developer options, connect by USB cable, tap **Allow** on the phone, start XR Desk, pick the phone, press **Play**. Details are in the [README](README.md#connect-your-phone).

## Download
Get the installer from the assets below (when attached) and check its SHA-256 against the `.sha256` file next to it.
