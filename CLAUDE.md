# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Setup

Requires a `config.py` file (not tracked in git) with:
```python
OPENAI_KEY = "sk-..."
ANKI_PATH = "/path/to/collection.anki2"
```

Create the audio cache directory:
```bash
mkdir cached_audio
```

Install dependencies:
```bash
pip install -r requirements.txt
```

## Running

```bash
# Normal mode (with audio)
python anki_ai.py

# Test mode (text input/output instead of audio)
python anki_ai.py noaudio
```

## Architecture

Single-file application (`anki_ai.py`) that creates a voice-driven Anki flashcard review session. The flow is:

1. **PyWebView window** (`display_card.html`) renders the current card's HTML/LaTeX via KaTeX
2. **Main loop** (`main_backend`) iterates through due cards from the Anki collection, skipping cloze cards and cards with images/rendered LaTeX
3. **TTS pipeline**: first uses macOS `say` command immediately, then caches OpenAI TTS audio (`cached_audio/`) for future use; LaTeX is translated to speakable text via GPT-3.5 before speaking
4. **STT pipeline**: Silero VAD detects speech in a background thread, Faster-Whisper (`tiny.en`) transcribes; listening ends after 2 seconds of silence
5. **Scoring**: GPT-3.5 rates the user's spoken answer 1–4; score feeds directly into Anki's scheduler (`collection.sched.answerCard`)

The `window.evaluate_js()` bridge is used to update card HTML and flash the screen green/red after scoring.
