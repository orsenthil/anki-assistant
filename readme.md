# Anki Assistant

## Watch the demo!
<p align="center">

<a href="http://www.youtube.com/watch?v=dSwf3j4xhG8" target="_blank">
  <img src="http://img.youtube.com/vi/dSwf3j4xhG8/0.jpg" alt="Demo Video">
</a>

</p>

I love learning new things, but the process of actually acquiring and maintaining knowledge isn't very fun. I've loved using [Anki](https://apps.ankiweb.net/) to help me organize what I'm learing, and make sure I don't forget things. This makes it easier to remember things I learn without having to come up with my own spaced repetition plan. I hate staring at a screen for so long though, so I've often wished I could do my flashcards without having to look at a screen all the time. I finally decided to make it happen. I focused a lot on reducing latency to make it feel as streamlined as possible.

## Tech Stack
- Text-To-Speech: [OpenAI TTS](https://platform.openai.com/docs/guides/text-to-speech) (`tts-1-hd`, voice `nova`) with macOS `say` as an instant fallback
- Speech-To-Text: [mlx-whisper](https://github.com/ml-explore/mlx-examples/tree/main/whisper) (`whisper-tiny.en`, Metal GPU-accelerated on Apple Silicon)
- Language Model: [GPT-4o-mini](https://platform.openai.com/docs/models) (LaTeX-to-speech translation and answer grading)
- Others: [PyWebView](https://github.com/r0x0r/pywebview), [Silero VAD](https://github.com/snakers4/silero-vad), [KaTeX](https://katex.org/)

## Setup

### Prerequisites

- macOS with Apple Silicon (M1/M2/M3) — required for mlx-whisper Metal acceleration
- Python 3.10+
- [Anki](https://apps.ankiweb.net/) installed with an existing card collection
- An [OpenAI API key](https://platform.openai.com/api-keys)

### 1. Clone the repo

```bash
git clone https://github.com/superMDguy/anki-assistant.git
cd anki-assistant
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

PyAudio requires PortAudio. If the install fails, install it first:

```bash
brew install portaudio
pip install -r requirements.txt
```

### 3. Find your Anki collection path

Your Anki collection file (`collection.anki2`) is typically at:

```
~/Library/Application Support/Anki2/<YourProfileName>/collection.anki2
```

You can confirm the exact path in Anki via **Help → Open Profile Folder** and then looking for `collection.anki2` in that folder. **Close Anki before running the assistant** — only one process can open the collection at a time.

### 4. Create `config.py`

Create a file named `config.py` in the project root (it is gitignored):

```python
OPENAI_KEY = "sk-..."
ANKI_PATH = "/Users/yourname/Library/Application Support/Anki2/YourProfile/collection.anki2"
```

### 5. Create the audio cache directory

```bash
mkdir cached_audio
```

TTS responses are cached here as MP3s so repeated cards play instantly without an API call.

### 6. Run it

```bash
# Full mode — uses microphone and speakers
python anki_ai.py

# Test mode — uses keyboard input/output, no audio hardware required
python anki_ai.py noaudio
```

### How it works

1. A PyWebView window opens and displays the front of each due card (with KaTeX math rendering).
2. The question is read aloud via macOS `say` immediately, then an OpenAI TTS version is cached in the background for next time.
3. Silero VAD listens on your microphone and starts recording when you speak.
4. After 2 seconds of silence, mlx-whisper transcribes your answer.
5. GPT-4o-mini scores your response 1–4 and the screen flashes green (4) or red (<4).
6. If you scored below 4, the correct answer is shown and read aloud.

**Voice commands:**
- Say **"skip card"** to bury the current card.
- Say **"I don't know"** to automatically score it 1.

### Notes

- Only **Basic** card types are reviewed; cloze cards are skipped.
- Cards whose answers contain images or rendered LaTeX are also skipped.
- mlx-whisper downloads the model (~150 MB) on first run and caches it locally.
