# Plain Video Maker

A premium, fully offline client-side web application designed to format, preview, and render text-based video files (Reels, Shorts, and Standard Landscape videos) directly inside the web browser. The tool operates 100% locally with zero server dependency, protecting user data and scripting privacy.

## Features

- **Local Video Encoding**: Encodes HTML5 Canvas animations and procedural web audio into high-definition WebM container files directly on the client machine.
- **Dual Aspect Ratios**: Supports Reel/Shorts (9:16 aspect ratio, 1080x1920) and standard landscape (16:9 aspect ratio, 1920x1080) output configurations.
- **Customizable Background Styling**: Supports background colors, linear gradients, and local image uploads.
- **Cinematic Ken Burns Zoom**: Applies a custom cinematic 8% scaling zoom animation to background images during video rendering.
- **Smart Text Pagination**: Automatically divides long scripts into slides based on character limits, or forces manual slide breaks via `---` on a new line.
- **Procedural Sound Mixing**: Uses Web Audio API oscillator and noise nodes to synthesize mechanical keyboard typing sound effects and slide transit click sounds, which are mixed alongside uploaded background MP3/WAV tracks.
- **Sleek Dual-Theme Interface**: Seamless integration of light and dark layouts with Feather-style outline indicators.

## Tech Stack

- **Markup & Layout**: Semantic HTML5 and modern CSS (Vanilla CSS Custom Properties for theme tokens).
- **Video Capture & Encoding**: MediaStream / MediaRecorder APIs and HTML5 Canvas 2D Context.
- **Audio Processing & Synthesis**: Web Audio API (BiquadFilters, GainNodes, OscillatorNodes, AudioBufferSources, and MediaStreamAudioDestinationNode).
- **Typography & Font Handling**: Embedded local font families (Fredoka, Montserrat, and Noto Sans Malayalam) to ensure offline layout integrity.

## Prerequisites

To run this application, you only need a modern web browser that supports:
- HTML5 Canvas & RequestAnimationFrame API
- Web Audio API (specifically AudioContext and BiquadFilters)
- MediaRecorder API with WebM video container support

Tested browsers include Google Chrome, Microsoft Edge, Brave, and Mozilla Firefox. No Node.js runtime, build tools, or databases are required.

## Installation & Setup

1. **Clone the Repository**
   Clone the repository to your local machine:
   ```bash
   git clone https://github.com/saheermk/plain-video-maker.git
   ```

2. **Navigate to Directory**
   ```bash
   cd plain-video-maker
   ```

3. **Open index.html**
   Open the `index.html` file directly in any modern browser:
   - Double-click the file, or
   - Use a simple HTTP server (such as Python's HTTP server or VS Code's Live Server extension) for optimal local font loading:
     ```bash
     python3 -m http.server 8000
     ```
     Then navigate to `http://localhost:8000` in your browser.

## Usage Examples

### Standard Slide Creation
1. Enter your script in the primary script area.
2. Adjust the "Max Characters Per Page" slider to set the length of each slide.
3. Choose "Fredoka (Bold Rounded)" under Layout & Fonts.
4. Select "Reel / Shorts (9:16)" under Aspect Ratio.
5. Click "Play Preview" to view the animation and typewriter effects in real-time.
6. Click "Export Video" to record and download the output WebM video file.

### Manual Slide Breaks
To control exactly where a slide ends, write your slides separated by `---` on its own line:
```text
This is the first slide.
---
This is the second slide.
```

## Contributing

Contributions to improve features, fix layout alignment bugs, or optimize audio synthesis are welcome. 

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add some amazing feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/amazing-feature
   ```
5. Open a Pull Request.
