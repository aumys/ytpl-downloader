# YTPL Downloader Project Context

## Project Identity
- Project name: YTPL Downloader
- Repository: https://github.com/aumys/ytpl-downloader
- Default branch: main
- Target platform: Windows x64
- Primary executable name: ytpl-downloader.exe

## Core Purpose
A Windows desktop application for downloading authorized YouTube videos and playlists, extracting currently available media URLs, selecting playlist ranges, choosing output formats, and supporting TV-friendly MP4 output.

## Current Features
- Video downloader for a single video URL.
- Playlist downloader.
- Playlist Start and End range selection.
- End = 0 means through the end of the playlist.
- Link extractor for playlist/video URLs.
- Copy selected/all URLs.
- TXT/CSV export where supported.
- Download progress, current title, ETA, status, log, and Stop button.
- Save-folder selection.
- TV-oriented MP4 presets.
- Automatic dependency detection and setup.
- Automatic dependency update checks.
- Application update notification design using a GitHub-hosted manifest.

## Output Formats
Preferred TV presets:
- TV MP4 1080p (H.264 + AAC)
- TV MP4 720p (H.264 + AAC)
- TV MP4 480p (H.264 + AAC)

Other presets:
- MP4 1080p (best)
- MP4 720p (best)
- MP4 480p (best)
- MKV (best)
- WebM (best)
- MP3 audio

TV compatibility note: H.264/AVC video + AAC audio in an MP4 container is the preferred general-purpose TV target, but exact compatibility varies by TV model.

## Dependencies
- yt-dlp
- Deno (for JavaScript runtime support where needed)
- FFmpeg and ffprobe for merging/conversion/audio extraction

## Dependency Policy
Startup should:
1. Check whether each dependency already exists on the computer.
2. Reuse or copy an existing executable when safe.
3. Check its version against the configured/current release.
4. Download only if missing or outdated.
5. Keep dependencies in the application's local cache/directory.

Dependency data should be centrally configurable rather than hard-coded in many locations.

## Application Update Policy
The application itself uses semantic versioning:
- 1.0.0 = first public release
- 1.0.x = bug fixes
- 1.x.0 = feature releases
- 2.x.0 = major redesign/breaking changes

On startup:
1. Read the online update manifest.
2. Compare local application version with the remote version.
3. If a newer version exists, show a clear notification.
4. On user approval, open the official GitHub Releases/download page.
5. Do not silently replace the application unless a future release architecture explicitly adds a safe updater.

## GitHub Release Policy
The EXE should be attached to GitHub Releases rather than stored as a normal repository source file.
Recommended asset name:
- ytpl-downloader.exe

Recommended tag format:
- v1.0.0
- v1.1.0
- v1.1.1

## GitHub Data Files
- update.json: application version and release/download-page metadata.
- config/components.json: dependency providers, repositories, assets, and update policies.
- PROJECT_CONTEXT.md: master project memory for future chats.
- CHANGELOG.md: chronological release/change history.
- README.md: public project documentation.

## Coding Rule
All source code must be English-only.
- Variable names: English.
- Function names: English.
- Comments: English.
- Configuration keys/values: English.
- Technical UI strings: English.

Do not put Urdu text inside source-code files. User-facing explanations outside code may be Urdu.

## Important Reliability Rules
- Do not use fragile PowerShell BackgroundWorker event attachment patterns that caused previous null/runspace errors.
- Keep long-running yt-dlp work outside the GUI thread.
- GUI must remain responsive during extraction/download.
- Avoid direct media URL assumptions: extracted media URLs can expire.
- Use safe temporary files and cleanup.
- Never store passwords, tokens, or private keys in the repository.

## Current Development History
1. Started as a YouTube playlist link extractor.
2. Added playlist range selection.
3. Added responsive GUI and Stop/Cancel behavior.
4. Added video downloader functionality.
5. Added output-format selection, including TV-friendly MP4 presets.
6. Added automatic dependency setup/update checks.
7. Added GitHub-hosted configuration and application update manifest.
8. Repository `aumys/ytpl-downloader` created and used as the persistent project home.

## Current Next Steps
- Publish the first stable GitHub Release with the final EXE.
- Set real release/update URLs in the EXE instead of placeholders.
- Add a robust GitHub Actions build pipeline for future releases.
- Keep CHANGELOG.md and PROJECT_CONTEXT.md updated after meaningful changes.
- Add checksum/signature strategy for published EXE builds.
- Test on clean Windows machines and common TV-compatible output cases.

## Chat Continuation Protocol
At the start of a new chat, read PROJECT_CONTEXT.md first and continue from its Current Next Steps and latest Development History. Do not assume old chat messages are available.

## User Requirements to Preserve
- Code must be English-only.
- The project should be maintained as a persistent GitHub repository.
- Prefer a single portable EXE for end users.
- The EXE should minimize manual setup on other PCs.
- Dependencies should be detected/reused when possible and downloaded only when necessary.
- The app should notify users about newer application versions and take them to the official release/download page.
