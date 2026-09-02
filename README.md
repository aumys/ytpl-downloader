# YTPL Downloader

YTPL Downloader is a Windows x64 YouTube video and playlist downloader with playlist range selection, TV-friendly MP4 output, and a link extraction mode.

## Automatic Updates

The application checks the project update manifest at startup:

https://raw.githubusercontent.com/aumys/ytpl-downloader/main/update.json

When a newer application version is available, the application shows an update notice and opens the GitHub Releases page selected in the manifest.

## Components

The application checks for required components before downloading them. It first tries to reuse existing local installations and copies usable executables into its private application cache when possible. It downloads missing or outdated components only when required.

Required components:
- yt-dlp
- Deno
- FFmpeg
- FFprobe

## Recommended TV Format

The recommended TV preset is MP4 using H.264/AVC video and AAC audio, with 720p or 1080p selected according to the TV and desired file size.

## Release

Binary application releases should be published through GitHub Releases. The repository source remains separate from release assets.

## License

License to be decided before the first public release.
