https://nvidia.com/en-us/geforce/guides/broadcasting-guide/

|                  |             | **Resolution** |          |         |
| ---------------- | ----------- | -------------- | -------- | ------- |
| **Upload Speed** | **Bitrate** | **H.264**      | **HEVC** | **AV1** |
| 4 Mbps           | 3 Mbps      | 576p           | 720p     | 720p    |
| 5 Mbps           | 4 Mbps      | 720p           | 720p     | 1080p   |
| 8 Mbps           | 6 Mbps      | 720p           | 1080p    | 1080p   |
| 10 Mbps          | 8 Mbps      | 1080p          | 1080p    | 1440p   |
| 12 Mbps          | 10 Mbps     | 1080p          | 1440p    | 1440p   |
| 15 Mbps          | 12 Mbps     | 1080p          | 1440p    | 4K      |
| 20 Mbps          | 15 Mbps     | 1080p          | 4k       | 4K      |
| 25 Mbps          | 20 Mbps     | 4k             | 4k       | 4K      |
| 50 Mbps          | 40 Mbps     | 4k             | 4k       | 4K      |
**Video Tab Settings:**
Base Resolution: Actual desktop resolution (4K)
Output Resolution: Resolution appropriate for Upload Speed
Downscale Filter: Lanczos, 36 samples = best quality
> "Many streamers opt to stream 1280x720 60FPS at 6,000 Kbps"

**Output Tab Settings:**
Simple:
- **Streaming:**
- **Bitrate:** Probably 4~6 Mbps for 1080p AV1
- **Encoder:** Twitch = NVENC, H.264 / Youtube = NVENC, AV1
- **Encoder Preset:** Most should use P6: Slower. If several encodes are going at the same time, then reduce.
Recording:
- **Recording Quality**: High Quality typically works for most users, but you can change this to Indistinguishable Quality if you have enough disk space or are going to do short videos (about 60 seconds).
- **Recording Format**: MKV
- **Encoder**: For local recordings you want to make sure that the format you record in is readable by the application you will use the file in. AV1 provides the best quality, followed by HEVC, and last by H.264. But H.264 has the most compatibility with apps.

**Other:**
Windows Game Mode
Windows Hardware-aaccelerated GPU scheduling (Default graphics settings)
OBS option to Run as Admin (top priority, good stream) `If GPU above 95%`
### Twitch Enhanced Broadcasting
Multitrack Video -> Enable Enhanced Broadcasting
Max Bandwidth & Max Video Tracks = Auto
