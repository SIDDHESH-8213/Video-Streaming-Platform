# Video-Streaming-Platform
![image](https://github.com/user-attachments/assets/31c2baad-57ff-4502-9d62-bed3bf66402b)

A Node.js and Express application that:
1. **Uploads a video** from the client.
2. **Encodes** the video into multiple resolutions (e.g., 240p, 480p, 720p) using **FFmpeg**.
3. **Splits** each resolution into small `.ts` segments of ~5 seconds.
4. Provides `.m3u8` playlists so the client can **stream** in HLS format.

---

## Overview

- **Why HLS?**  
  HTTP Live Streaming (HLS) divides video into small segments (`.ts`) with a playlist file (`.m3u8`).  
  It lets players adapt the quality based on the viewer’s network speed (adaptive bitrate).

- **Why Multiple Qualities?**  
  By creating 240p, 480p, 720p variants, viewers can watch smoothly even on slower connections.

---

## Features

- **File Upload**: Uses [Multer](https://www.npmjs.com/package/multer) to handle single file uploads.  
- **Video Conversion**: Uses [FFmpeg](https://ffmpeg.org/) to encode videos.  
- **Adaptive Streaming**: Generates multiple resolution playlists for HLS.  
- **UUID-based**: Unique folders for each upload.  
- **CORS Support**: Configured to accept requests from specific frontends (e.g., `localhost:3000`).

---

## Prerequisites

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **FFmpeg** installed and accessible via command line:
  - Windows: [Gyan’s builds](https://www.gyan.dev/ffmpeg/builds/) or `choco install ffmpeg`
  - macOS: `brew install ffmpeg`
  - Linux: `sudo apt-get install ffmpeg`

---

Feel free to edit, expand, or remove any sections to match your project’s specifics!
