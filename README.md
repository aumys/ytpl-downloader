# YTPL Downloader - Ultimate Pro Edition 🚀

![YTPL Downloader](https://img.shields.io/badge/Version-4.0-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Windows-blue)
![Language](https://img.shields.io/badge/Language-PowerShell-blueviolet)

YTPL Downloader is a powerful, IDM-style, professional YouTube and Playlist downloading application built completely in PowerShell and WPF (XAML). It utilizes the powerful `yt-dlp` and `FFmpeg` engines under the hood.

## 🌟 Key Features

- **IDM-Style UI:** Clean, dark-themed UI with pop-up progress dialogs and completion actions.
- **Smart Clipboard Monitor:** Automatically detects and grabs media links from your clipboard.
- **Pause & Resume:** Full support for pausing and resuming active downloads.
- **Advanced Quality Presets:** Download in TV MP4 (H.264+AAC), 1080p, 720p, MKV, WebM, and MP3.
- **Playlist Management:** Download full playlists or specific ranges (e.g., videos 185 to 245).
- **Pro Metadata & Auth:**
  - Embed English/Urdu Subtitles automatically.
  - Download video thumbnails (JPG).
  - Use Browser Cookies (Chrome, Edge, Firefox) for age-restricted or private videos.
  - Custom file naming formats (Date, Channel Name, Title).
- **Automated Post-Actions:** Turn off your PC automatically after downloads finish.
- **Thread Optimization:** Up to 16 concurrent fragments for maximum download speed.

## ⚙️ Installation & Usage

1. Download the `YTPL-Downloader.exe` from the Releases tab (or compile it yourself using `ps2exe`).
2. Place the executable in any folder. 
3. *Note: Ensure `yt-dlp.exe` and `ffmpeg.exe` are in the same folder, or let the smart auto-setup handle dependencies if configured.*
4. Open the app, paste a URL, select your desired quality, and hit **Start Download**.

## 🛠️ Compilation (For Developers)

To compile the raw PowerShell script into a Windows executable without a console window, run:

```powershell
Invoke-ps2exe -inputFile "ytpl-app.ps1" -outputFile "YTPL-Downloader.exe" -noConsole
```

## 📜 License

This project is created for educational and personal use.
