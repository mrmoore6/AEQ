# SONIC FORGE AI - Web Application

## Neural Audio Equalizer Pro - Web Edition

A powerful web-based audio equalizer with neural EQ analysis, playlist management, and advanced audio filtering capabilities.

---

## 🌟 Features

### 🎵 Playlist Management
- Import multiple MP3/MP4 audio files
- Add, remove, and clear tracks
- Shuffle functionality for random playback
- Previous/Next track navigation
- Auto-play next track when current ends
- Persistent playlist storage (track names saved in browser localStorage)

### 🎚️ Audio Filters
- **High Pass Filter**: Remove low frequencies (20-500 Hz)
- **Low Pass Filter**: Remove high frequencies (5000-20000 Hz)
- **Denoiser**: Reduce background noise (0-100%)
- **Auto-Save**: Filtered audio automatically saved as WAV
- **Auto-Add**: Processed WAV files automatically added to playlist

### 📊 Neural EQ Analysis
- Real-time frequency analysis during playback
- 7-band EQ visualization (60Hz, 150Hz, 400Hz, 1kHz, 2.5kHz, 6kHz, 12kHz)
- Visual feedback with orange bars
- dB level display for each frequency band

### 🎮 Music Player
- Play/Pause controls
- Stop button
- Previous/Next track buttons
- Volume control (0-100%)
- Position slider for seeking
- Time display (current/total)
- Now Playing indicator

### 💾 Automatic WAV Conversion
- All filtered audio is automatically converted to WAV format
- Files saved to Downloads folder
- Processed files automatically added back to playlist
- Naming convention: `[original_name]_filtered.wav`

---

## 🚀 Quick Start

### 1. Open the Application
```bash
cd ~/Desktop/AEQ
open sonic_forge_web.html
```

Or simply double-click `sonic_forge_web.html` in Finder.

### 2. Import Audio Files
- Click the "▲ IMPORT AUDIO FILES (MP3/MP4)" button
- Select one or multiple audio files
- Files will be added to the playlist

### 3. Play Music
- Click on a track in the playlist to load it
- Use the ▶ button to play/pause
- Use ⏮ and ⏭ buttons to navigate tracks
- Adjust volume with the slider
- Use the position slider to seek

### 4. Apply Audio Filters
1. Adjust the filter sliders:
   - **High Pass**: Remove rumble and low-end noise
   - **Low Pass**: Remove hiss and high-frequency noise
   - **Denoiser**: Reduce overall background noise
2. Click "Apply Filters & Save as WAV"
3. The filtered audio will be:
   - Applied to the current track
   - Automatically saved as WAV to Downloads
   - Added to the playlist for immediate playback

### 5. Playlist Controls
- **Clear All**: Remove all tracks from playlist
- **🔀 Shuffle**: Randomize playlist order (button turns green when active)
- **❌ (on track)**: Remove individual track from playlist

---

## 💻 Technical Details

### Files
- `sonic_forge_web.html` - Main HTML structure
- `sonic_forge_web.css` - Styling (black & orange theme)
- `sonic_forge_web_enhanced.js` - JavaScript functionality

### Technologies
- **Web Audio API**: Audio processing and filtering
- **Biquad Filters**: High-pass and low-pass filtering
- **OfflineAudioContext**: Audio rendering for WAV export
- **LocalStorage**: Playlist persistence
- **WAV Encoding**: Custom 16-bit PCM WAV file generation

### Browser Compatibility
- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge

### Audio Processing Pipeline
1. **File Import**: MP3/MP4 files decoded using Web Audio API
2. **Playback**: Real-time audio playback with EQ visualization
3. **Filter Application**:
   - High Pass Filter: Biquad filter with adjustable frequency
   - Low Pass Filter: Biquad filter with adjustable frequency
   - Denoiser: Gain reduction for noise suppression
4. **WAV Export**: 16-bit PCM format, automatic download
5. **Playlist Update**: Processed file added back to playlist

---

## 🎨 Design

### Color Scheme
- **Primary Background**: Black (#000000)
- **Accent Color**: Orange (#FF8C00)
- **Container Background**: Dark gray (#1a1a1a)
- **Text**: White/Gray gradient
- **Borders**: Orange highlights

### UI Layout
1. **Title Section**: SONIC FORGE AI branding
2. **Import Button**: Large, prominent file selector
3. **Playlist Section**: Scrollable track list
4. **Progress Bar**: Visual processing feedback
5. **Audio Filters**: Slider controls with real-time values
6. **EQ Visualization**: 7-band frequency display
7. **Music Player**: Full playback controls
8. **Processing Log**: Detailed operation feedback

---

## 📝 Important Notes

### Playlist Persistence
- ✅ Track names and metadata are saved to browser localStorage
- ❌ Audio files themselves cannot be stored in localStorage (browser limitation)
- ⚠️ After browser restart, track names are preserved for reference only
- 🔄 You must re-import audio files to play them after restart

### WAV File Handling
- ✅ All filtered audio is automatically converted to WAV
- 💾 WAV files are saved to your Downloads folder
- ➕ Processed WAV files are automatically added to the playlist
- 🔁 You can apply filters multiple times to create different versions
- 📝 Files are named: `[original_name]_filtered.wav`

### Performance
- ⏱️ Large audio files may take time to process
- ⚡ Filter application is done offline (non-blocking UI)
- 📊 Real-time EQ updates during playback
- 💾 WAV export happens automatically after filtering

---

## 🔧 Troubleshooting

### Audio won't play
- ✅ Check browser console for errors (F12)
- ✅ Ensure audio file format is supported (MP3/MP4)
- ✅ Try refreshing the page
- ✅ Check system audio settings

### Filters not working
- ✅ Make sure an audio file is loaded
- ✅ Check that Audio Context is initialized
- ✅ Try importing the file again
- ✅ Check browser console for errors

### Playlist not saving
- ✅ Check browser localStorage is enabled
- ✅ Clear browser cache and try again
- ⚠️ Note: Audio files must be re-imported after restart
- ✅ Only track names/metadata are saved, not audio data

### WAV files not downloading
- ✅ Check browser download settings
- ✅ Ensure pop-ups are not blocked
- ✅ Check Downloads folder permissions
- ✅ Try a different browser

### EQ visualization not updating
- ✅ Ensure audio is playing
- ✅ Check that analyser node is connected
- ✅ Try reloading the track

---

## 💡 Tips & Best Practices

### Filter Settings
- **High Pass (80 Hz)**: Good starting point for removing rumble
- **Low Pass (16000 Hz)**: Preserves most audible frequencies
- **Denoiser (30%)**: Moderate noise reduction without artifacts

### Workflow
1. Import all your audio files first
2. Listen to each track to identify issues
3. Adjust filters for the current track
4. Apply filters - WAV is auto-saved and added to playlist
5. Continue with next track or play the processed version

### Playlist Management
- Use shuffle for variety
- Remove tracks you don't need
- Processed WAV files appear at the end of the playlist
- Clear All to start fresh

---

## 🚀 Future Enhancements

- [ ] Additional filter types (reverb, echo, compression)
- [ ] Custom EQ band adjustment (manual control)
- [ ] Batch processing (apply filters to all tracks)
- [ ] Cloud storage integration
- [ ] Waveform visualization
- [ ] Spectrum analyzer
- [ ] Preset filter configurations
- [ ] Export playlist as M3U
- [ ] Drag-and-drop file import
- [ ] Keyboard shortcuts

---

## 📚 API Reference

### Main Class: `SonicForgeWeb`

#### Methods
- `handleFileSelect(event)` - Process file input
- `addToPlaylist(file)` - Add file to playlist
- `loadTrack(index)` - Load track by index
- `play()` - Start playback
- `pause()` - Pause playback
- `stopPlayback()` - Stop and reset
- `applyFilters()` - Apply filters and save WAV
- `savePlaylistToStorage()` - Save to localStorage
- `loadPlaylistFromStorage()` - Load from localStorage

#### Properties
- `audioContext` - Web Audio API context
- `audioBuffer` - Current audio buffer
- `playlist` - Array of track objects
- `currentTrackIndex` - Currently playing track
- `isPlaying` - Playback state

---

## ℹ️ Additional Information

### File Size Limits
- Browser memory limits apply
- Recommended: < 50MB per file
- Large files may cause performance issues

### Supported Formats
- ✅ MP3 (MPEG Audio Layer 3)
- ✅ MP4 (MPEG-4 Audio)
- ❌ WAV input (not needed, output only)
- ❌ FLAC (not supported by Web Audio API)

### Privacy
- ✅ All processing happens locally in browser
- ✅ No files uploaded to servers
- ✅ No data collection
- ✅ Playlist saved only in your browser

---

## 📞 Support

For issues or questions:
1. Check this README
2. Check browser console (F12)
3. Try a different browser
4. Clear browser cache

---

## 🏆 Credits

**SONIC FORGE AI** - Neural Audio Equalizer Pro  
Web Edition

Developed with:
- Web Audio API
- JavaScript ES6+
- HTML5
- CSS3

---

**Version**: 1.0  
**Last Updated**: January 9, 2026  
**Status**: Production Ready ✅
