Trimarr

Automated media processing and transcoding for Radarr and Sonarr.

Trimarr is a self-hosted media-processing application designed to clean up, optimize and standardize movie and TV libraries after download. It connects to Radarr and Sonarr, applies reusable processing flows and provides a clear overview of active, queued and completed jobs.

[!IMPORTANT]
Trimarr is currently under active development. Features, configuration and installation steps may change between releases.

Why Trimarr?

Media from different sources often arrives with inconsistent codecs, unnecessary audio tracks, unwanted subtitles, incompatible metadata or inefficient file sizes. Trimarr automates that cleanup while keeping the workflow visible and configurable.

The goal is a smaller, cleaner and more compatible media library without requiring every file to be handled manually.

Features

Radarr and Sonarr integration

Automated processing after library import

Reusable processing flows

Hardware-accelerated transcoding

Configurable video and audio output

Audio and subtitle language priorities

Removal of unwanted commentary tracks and track names

Embedded or extracted subtitle handling

Optional black-bar detection and cropping

Optional Dolby Vision metadata removal for broader compatibility

Resolution, channel and bitrate limits

Weekly full-power, low-power and paused schedules

Live queue, progress, ETA and processing statistics

Before-and-after media details

Library browser for movies and TV series

Dark, responsive web interface

Processing flows

A flow is a reusable collection of preferences that determines how Trimarr processes media.

A flow can define:

Video codec and encoder

Hardware encoder

Quality level

Maximum resolution

Audio codec, bitrate and channel limit

Preferred audio languages

Preferred subtitle languages

Subtitle delivery method

Output container

Track cleanup rules

Different flows can be assigned to individual Radarr and Sonarr connections.

How it works

Radarr or Sonarr imports a completed download into the media library.

Trimarr detects the imported media through the configured connection.

The assigned flow determines which tracks are kept, removed, converted or extracted.

Trimarr processes the media using the selected CPU or hardware encoder.

The optimized output replaces the original library copy when processing completes successfully.

Progress, logs and before-and-after details remain available in the Trimarr interface.

Scheduling

Trimarr can apply different processing modes throughout the week:

Full power — normal processing performance.

Low power — reduced CPU/GPU use and fewer concurrent jobs.

Off — prevents new jobs from starting during the selected period.

Processing can also be paused manually. When a job is active, Trimarr can either let it finish or stop it immediately before pausing the queue.

Compatibility

Trimarr is intended for self-hosted environments and media-server workflows using tools such as:

Radarr

Sonarr

FFmpeg-compatible processing

Hardware encoders such as NVIDIA NVENC, Intel Quick Sync or other supported encoders

Actual codec and hardware support depends on the host system, container configuration and installed processing tools.

Installation

Installation documentation will be added when the deployment process and supported environments are finalized.

Before publishing installation commands, document the exact requirements for:

Docker or native deployment

Required environment variables

Media-library volume mappings

Radarr and Sonarr URLs and API keys

FFmpeg and hardware-device access

Persistent configuration and database storage

Safety

Trimarr modifies media files. Test new flows with non-critical media before applying them to an entire library, and maintain a backup of important content.

Project status

Trimarr is under active development. Bug reports, testing feedback and feature suggestions are welcome once contribution guidelines and issue templates are available.

License

No license has been published yet. Until a license is added, the source code remains protected by standard copyright rules.
