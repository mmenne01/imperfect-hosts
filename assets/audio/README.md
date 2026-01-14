# Audio Files for Music Player

This folder contains the audio files used by the music player on the website.

## How to Add Your Music Files

### Method 1: Using File Explorer (Easiest)
1. Open File Explorer and navigate to: `d:\Imperfect Hosts\github\imperfect-hosts\assets\audio\`
2. Copy your MP3 files into this folder
3. Make sure the filenames match what's in the playlist (or update the playlist)

### Method 2: Using Command Line
```bash
# Copy a file from another location
copy "C:\path\to\your\song.mp3" "d:\Imperfect Hosts\github\imperfect-hosts\assets\audio\song.mp3"
```

## Current Playlist Configuration

The playlist is configured in `_layouts/default.html` (around line 468-493).

Currently expecting these files:
- `spare-change.mp3`
- `loading-dock-lullaby.mp3`
- `rents-due.mp3`
- `breakroom-daydreams.mp3`

## Updating the Playlist

To change the tracks in the playlist:

1. Open `_layouts/default.html`
2. Find the `tracks` array (around line 468)
3. Update the track information:

```javascript
const tracks = [
    {
        title: "Your Song Title",
        artist: "Imperfect Hosts",
        duration: "3:45",  // Format: MM:SS
        src: "/assets/audio/your-filename.mp3"
    },
    // Add more tracks...
];
```

## Supported Audio Formats

- MP3 (recommended for best compatibility)
- WAV (larger file size)
- OGG (good compression, good browser support)

## Tips

- Keep filenames simple (no spaces, use hyphens: `my-song.mp3`)
- Recommended bitrate: 128-320 kbps for MP3
- Make sure files aren't too large (consider compression for web delivery)
- Test the player after adding files to ensure they load correctly

## Using External URLs

You can also use external URLs instead of local files:

```javascript
src: "https://example.com/your-song.mp3"
```

This is useful if you host your music on:
- SoundCloud
- Bandcamp
- Your own CDN
- Any public audio hosting service
