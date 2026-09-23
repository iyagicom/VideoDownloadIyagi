<p align="center"><img src="videodownloadiyagi.png" width="128" alt="VideoDownloadIyagi"></p>

# VideoDownloadIyagi

Finds the video playing in your browser and **saves it to your PC**.

A **browser extension** detects the video; the **VideoDownloadIyagi engine** installed on your PC downloads it.
Nothing is downloaded inside the browser, so large videos are fast and keep downloading after you close the browser.

[한국어 README](README_ko.md)

<p align="center"><img src="popup.png" width="420" alt="Extension popup"></p>

---

## ✨ Features

* **Automatic detection** — HLS (m3u8), MP4, WebM and more, straight from the page's network traffic, with a toolbar badge
* **Quality & audio choice** — pick among HLS renditions (1080p, 720p…) and audio tracks
* **Fast** — 6 HLS segments at once; large files in 4 parallel ranges
* **Resume** — continues where it stopped after a pause or a dropped connection
* **Lossless merge** — video and audio into MP4 / MKV without re-encoding (needs FFmpeg)
* **AES-128 HLS** — standard encrypted streams
* **Stays logged in** — uses the browser's cookies and headers, refreshed from the extension when they expire
* **Tray engine** — job list, progress, completion notices; keeps going after the browser closes
* **Browsers** — Chrome · Edge · Chromium · Brave · Vivaldi (Firefox coming)

## 📥 Install

### 1. Engine

Download the file for your system from [**Releases**](https://github.com/iyagicom/VideoDownloadIyagi/releases/latest).

| System | File |
|---|---|
| Ubuntu 24.04 | `videodownloadiyagi_<ver>.ubuntu24.04_amd64.deb` |
| Ubuntu 26.04 | `videodownloadiyagi_<ver>.ubuntu26.04_amd64.deb` |
| Fedora | `videodownloadiyagi-<ver>-1.x86_64.rpm` |
| Arch | `videodownloadiyagi-<ver>-1-x86_64.pkg.tar.zst` |
| Other Linux | `.AppImage` or `.zip` |

deb/rpm/pkg.tar.zst connect to your browsers on install; AppImage/zip connect themselves when **run once**.
Merging video and audio needs `ffmpeg`; without it the tracks are saved separately.

### 2. Browser extension

Until the Chrome Web Store listing, install it unpacked:

1. Download `videodownloadiyagi-extension-<ver>.zip` from Releases and unzip it
   (deb/rpm/zst installs already have it at `/usr/share/videodownloadiyagi/extension`)
2. Open `chrome://extensions` (Edge: `edge://extensions`) → turn on **Developer mode**
3. **Load unpacked** → choose that folder
4. Play a video and click the toolbar icon — it should say **Engine connected**

## ⚠️ Not supported

DRM-protected content (Widevine, PlayReady, FairPlay) is not downloaded, and there is no circumvention.
YouTube and similar streaming services are not supported.
Save only videos you are legitimately allowed to watch, for personal use.

## 🔒 Privacy

Cookies and login data stay in the engine's memory only during a download and are never written to disk or logs.
The extension and the engine talk only inside your PC (no external server) and no local network port is opened.
