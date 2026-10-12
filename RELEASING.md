# How to publish a new version

Every version is a **GitHub Release**. The *Update Check* button of XR Desk reads the latest release of this repository, so the steps below must be the same every time.

## Rules
- Version numbers are `MAJOR.MINOR.PATCH` (for example `3.5.1`). The release tag is the same with a `v` in front: `v3.5.1`.
- The installer is named `XRDesk-Setup-<version>.exe` (for example `XRDesk-Setup-3.5.1.exe`). One installer per release.
- Next to it goes a file with its SHA-256: `XRDesk-Setup-<version>.exe.sha256`. XR Desk checks it after downloading.
- The repository must stay **public**: *Update Check* asks the public GitHub API, no token is built into the program.
- Only the newest **published, non-draft, non-pre-release** release counts as "latest". Mark a test build as *pre-release* so it is not offered to users.

## Steps
1. Change the version in the program (and in `assets/app.rc`), build it, make the installer.
2. Write what changed at the top of `CHANGELOG.md`, and put the same text in `RELEASE_NOTES.md` (the release page shows it).
3. Make the hash file (PowerShell, in the folder of the installer):
   ```powershell
   (Get-FileHash .\XRDesk-Setup-3.5.1.exe -Algorithm SHA256).Hash.ToLower() + "  XRDesk-Setup-3.5.1.exe" | Set-Content .\XRDesk-Setup-3.5.1.exe.sha256
   ```
4. Commit the notes and tag the version:
   ```powershell
   git add CHANGELOG.md RELEASE_NOTES.md README.md
   git commit -m "XR Desk 3.5.1"
   git push
   ```
5. Create the release and upload the files (GitHub CLI):
   ```powershell
   gh release create v3.5.1 .\XRDesk-Setup-3.5.1.exe .\XRDesk-Setup-3.5.1.exe.sha256 --title "XR Desk 3.5.1" --notes-file RELEASE_NOTES.md
   ```
   For a test build add `--prerelease`. The same can be done on the website: *Releases → Draft a new release*, choose the tag `v3.5.1`, paste the notes, drag the two files, *Publish release*.
6. Open the release page and check: the tag, the notes, the two files.

## Check what *Update Check* will see
```powershell
(Invoke-RestMethod https://api.github.com/repos/<owner>/XR-Desk/releases/latest).tag_name
```
