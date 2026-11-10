# ffmpeg (video rendering and conversion)

| | |
|---|---|
| Download | [ffmpeg.org/download](https://ffmpeg.org/download.html) |
| Source | [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) |
| Last checked | 2026-11-10 |

## Where it fits
seaMotion exports video in the browser. ffmpeg is for everything after export: converting, compressing, GIFs for PRs,
image sequences and poster frames.

## Install
| System | Command |
|---|---|
| Mac | `brew install ffmpeg` |
| Windows | `winget install Gyan.FFmpeg` |
| Linux | `sudo apt install ffmpeg` |

Check: `ffmpeg -version`

## Recipes
| Task | Command |
|---|---|
| WebM to MP4 (clients, social) | `ffmpeg -i in.webm -c:v libx264 -crf 20 -pix_fmt yuv420p -movflags +faststart out.mp4` |
| Compress a web hero video | `ffmpeg -i in.mp4 -c:v libx264 -crf 26 -preset slow -an -movflags +faststart hero.mp4` |
| Smaller WebM for the web | `ffmpeg -i in.mp4 -c:v libvpx-vp9 -crf 34 -b:v 0 -an hero.webm` |
| GIF for previews and PRs | `ffmpeg -i in.mp4 -vf "fps=24,scale=640:-1:flags=lanczos,split[a][b];[a]palettegen[p];[b][p]paletteuse" out.gif` |
| Image sequence to video | `ffmpeg -framerate 60 -i frame_%04d.png -c:v libx264 -pix_fmt yuv420p out.mp4` |
| Poster frame for `<video>` | `ffmpeg -ss 1 -i in.mp4 -frames:v 1 poster.jpg` |
| Resize to 1080 wide | `ffmpeg -i in.mp4 -vf "scale=1080:-2" -c:v libx264 -crf 22 out-1080.mp4` |

## Tips
- MP4 for the web: always `-pix_fmt yuv420p` and `-movflags +faststart`, or some phones and browsers won't play it.
- Hero videos have no sound: drop audio with `-an`.
- `-crf`: lower is better quality and bigger. 18–23 for delivery, 26–30 for web backgrounds.
- Put the size in the file name: `hero-1920.mp4`, `hero-1080.webm`.
