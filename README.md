# YTPL Downloader

YTPL Downloader is a Windows x64 desktop application for downloading authorized YouTube videos and playlists, extracting media URLs, selecting playlist ranges, and creating TV-friendly MP4 files.

## Project

- Application name: YTPL Downloader
- Executable: `ytpl-downloader.exe`
- Target: Windows x64
- Repository: https://github.com/aumys/ytpl-downloader

## Features

- Single video downloading.
- Playlist downloading.
- Playlist Start and End range selection.
- Link extraction and export.
- Download progress, ETA, current item, log, and Stop controls.
- Save-folder selection.
- TV-friendly MP4 presets using H.264 video and AAC audio.
- MP4, MKV, WebM, and MP3 presets.
- Automatic detection and reuse of existing dependencies.
- Automatic dependency update checks.
- Application update notification through a GitHub-hosted manifest.

## Dependencies

- yt-dlp
- Deno
- FFmpeg
- ffprobe

The application checks for existing components before downloading them. Missing or outdated components are downloaded from their configured sources.

## Update System

The application version is managed independently from dependency versions. When a newer application version is published, the application can notify the user and open the official GitHub Releases page.

Configuration files:

- `update.json` - application update metadata.
- `config/components.json` - dependency configuration.
- `PROJECT_CONTEXT.md` - persistent project context for future development.
- `CHANGELOG.md` - project change history.

## Release

Application binaries should be published through GitHub Releases. The recommended release asset name is `ytpl-downloader.exe`.

## Development Rules

Source code must be English-only. Do not place Urdu text inside source code, configuration, or code comments.

Do not store credentials, tokens, passwords, or private keys in this repository.

## Legal

Use the application only for content you are authorized to download and in accordance with applicable laws and platform terms.
