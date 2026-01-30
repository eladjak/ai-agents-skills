# Kinetic Video Creator Skill

Automated kinetic typography video creation system using Remotion, ElevenLabs TTS, and music generation.

## What This Skill Does

Creates professional kinetic typography videos from a simple topic/idea:

1. ✅ Writes emotionally-crafted scripts with bracket directions
2. ✅ Generates speech with ElevenLabs TTS
3. ✅ Creates matching background music (exact duration)
4. ✅ Transcribes audio for word-level timing
5. ✅ Builds Remotion composition with animations
6. ✅ Renders final video
7. ✅ Optionally uploads to YouTube

## Prerequisites

### Required Skills
These skills must be installed first:
```bash
# Remotion skill
npx @anthropic-ai/claude-code skill add remotion-dev/skills/remotion-best-practices

# Aviz Skills Library
npx @anthropic-ai/claude-code skill add aviz85/claude-skills-library/skills/speech-generator
npx @anthropic-ai/claude-code skill add aviz85/claude-skills-library/skills/music-generator
npx @anthropic-ai/claude-code skill add aviz85/claude-skills-library/skills/transcribe
npx @anthropic-ai/claude-code skill add aviz85/claude-skills-library/skills/youtube-uploader
```

**IMPORTANT:** After installing skills, restart Claude Code!

### Required Dependencies
```bash
# Remotion
npm install remotion @remotion/cli @remotion/player

# FFmpeg (for audio mixing)
# macOS: brew install ffmpeg
# Ubuntu: sudo apt install ffmpeg
```

### Environment Variables
Create `.env` file:
```
ELEVENLABS_API_KEY=sk_3eb9c9aa286373eca54903fc91d399f28848240fb17d4d91
```

## Script Writing Guidelines

Write scripts with emotional bracket directions:

```
[dramatic pause] The future isn't coming.
[slowly, with weight] It's already here.
[building intensity] Every day, every decision...
[powerful, emphatic] ...shapes the world we'll live in.
[warm, inspiring] And you? You're part of it.
```

### Supported Directions
- **Pacing**: [pause], [long pause], [slowly], [faster]
- **Tone**: [whisper], [emphatic], [warm], [dramatic]
- **Dynamic**: [building], [descending], [with weight]

### Word Count Guide
- 30 sec = 60-80 words
- 60 sec = 120-150 words
- 90 sec = 180-220 words

## Workflow Steps

### 1. Script Writing
Ask Claude to write an emotional script:
```
"Write a 60-second kinetic video script about [topic]"
```

### 2. Speech Generation
Use the speech-generator skill:
```
"Generate speech from script.txt and save to speech.mp3"
```

### 3. Transcription
Use the transcribe skill for word-level timing:
```
"Transcribe speech.mp3 with word-level timing to transcript.json"
```

### 4. Music Generation
Use the music-generator skill (specify exact duration from transcription):
```
"Generate 87 seconds of inspirational cinematic music"
```

### 5. Audio Mixing
Mix speech + music with FFmpeg:
```bash
ffmpeg -y \
  -i speech.mp3 \
  -i music.mp3 \
  -filter_complex "[0:a]volume=1.0[speech];[1:a]volume=0.17[music];[speech][music]amix=inputs=2:duration=first[out]" \
  -map "[out]" -c:a libmp3lame -q:a 2 \
  final_audio.mp3
```

### 6. Remotion Composition
Create composition using template:
```tsx
import { MultiWordComposition } from '../templates/MultiWordComposition';
import transcriptData from '../projects/my-video/transcript.json';

export const MyKineticVideo: React.FC = () => {
  const WORD_TIMINGS = transcriptData.words.map(w => ({
    word: w.word,
    start: w.start,
    end: w.end,
  }));

  return (
    <MultiWordComposition
      wordTimings={WORD_TIMINGS}
      audioFile="../projects/my-video/final_audio.mp3"
      mode="wordCloud"
      heroFontSize={180}
      strongFontSize={120}
      normalFontSize={80}
      glowIntensity={1.5}
      dustEnabled={true}
      lightBeamsEnabled={true}
      colorScheme={3}
    />
  );
};
```

### 7. Render Video
Use remotion-render skill:
```
"Render the MyKineticVideo composition to output.mp4"
```

### 8. Upload (Optional)
Use youtube-uploader skill:
```
"Upload output.mp4 to YouTube with title 'My Kinetic Video'"
```

## Animation Modes

### Word Cloud (default)
- Multiple words appear together
- Grouped by timing gaps
- Best for: Fast-paced, dynamic content

### Single Word
- One word at a time, centered
- Best for: Dramatic, impactful statements

## Visual Customization

Available props:
- `heroFontSize`: Size for emphasis words (default: 180)
- `strongFontSize`: Size for important words (default: 120)
- `normalFontSize`: Size for regular words (default: 80)
- `glowIntensity`: 0-3, glow around text (default: 1.5)
- `dustEnabled`: Particle effects (default: true)
- `lightBeamsEnabled`: Light beam animations (default: true)
- `colorScheme`: 0-7, predefined color palettes (default: 3)

## Example Usage

### Quick Mode
```
"Create a kinetic video about the importance of persistence in achieving goals"
```

Claude will:
1. Write an emotional script
2. Generate speech
3. Create music
4. Transcribe timing
5. Build composition
6. Render video

### Manual Mode
For more control:
```
1. "Write a 90-second script about overcoming fear"
2. "Generate speech from script.txt"
3. "Transcribe speech.mp3"
4. "Generate 93 seconds of dramatic cinematic music"
5. "Mix audio files: speech.mp3 + music.mp3 → final_audio.mp3"
6. "Create Remotion composition with word cloud mode"
7. "Render MyKineticVideo composition"
```

## Troubleshooting

### Skill Not Found
```bash
# Install missing skill
npx @anthropic-ai/claude-code skill add aviz85/claude-skills-library/skills/[skill-name]

# Restart Claude Code
exit # then re-enter project
```

### FFmpeg Not Found
```bash
# macOS
brew install ffmpeg

# Ubuntu/Debian
sudo apt install ffmpeg

# Windows
# Download from https://ffmpeg.org/download.html
```

### ElevenLabs API Issues
- Check `.env` file has valid API key
- Verify API key has credits remaining
- Check network connectivity

### Remotion Render Fails
```bash
# Check Remotion installation
npm list remotion

# Reinstall if needed
npm install remotion @remotion/cli @remotion/player
```

## Resources

- **Remotion**: https://www.remotion.dev/
- **Remotion Skills**: https://skills.sh/remotion-dev/skills/remotion-best-practices
- **Remotion Assistant**: https://aviz85.github.io/remotion-assistant/
- **ElevenLabs**: https://elevenlabs.io/
- **Aviz Skills**: https://github.com/aviz85/claude-skills-library

## Credits

Created by Elad Jacoby
Based on Aviz85's Remotion Assistant and Claude Skills Library
Powered by Claude Sonnet 4.5

---

**Triggers**: kinetic video, kinetic typography, video creation, remotion, elevenlabs, tts video, animated text, speech to video
