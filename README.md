# Gen AI Voice Transcriber

**Organization:** Ecube Analytics  
**Status:** Early-stage prototype

A powerful voice-to-text transcription app built on OpenAI’s Whisper model. Designed as a Streamlit/Flask interface that lets users upload audio files and receive speech-to-text output with support for multiple languages, speaker diarization, and privacy considerations for future local model integration.

---

## Project Overview

An AI-driven transcription tool that converts audio files (e.g., interviews, podcasts, voice notes) into text using OpenAI’s Whisper. Features include:

- **Simple user interface** for uploading audio and viewing transcripts in real time.
- Uses the **OpenAI Whisper API**, capable of multilingual recognition and improved performance in noisy environments :contentReference[oaicite:1]{index=1}.
- Supports `.wav`, `.mp3`, and `.m4a` formats.
- Currently cloud-dependent, with secure handling of API credentials using best practices (config file or environment variables).

---

## How to Set It Up

1. **Clone the repo**  
   ```bash
   git clone <repo-url>
   cd GenAI_Voice_Transcriber
2. Install dependencies
   ```bash
   pip install -r requirements.txt
3. Set your OpenAI key
   ```bash
   export OPENAI_API_KEY="sk-..."
4. Run the app Using Streamlit:
   '''bash
   streamlit run app.py

   Or using flask
    '''bASH
   python app.py
 5. Upload audio files and get transcriptions immediately.

---
```
## Sample Folder Structure
.
├── app.py                  # Main Streamlit or Flask application
├── transcriber.py          # Whisper-based transcription logic
├── requirements.txt        # Dependencies list
├── config.py               # Secure API key loader
├── utils/                  # Audio processing, diarization helper scripts
└── README.md               # This document
```
---

Future Enhancements
- Local Model Option: Leverage on-prem NVIDIA A5000 GPUs with LLaMA 3.3 70B and updated Whisper models to enable offline transcription—cutting API costs and preserving data privacy.
- Hybrid Transcription Pipeline: Allow users to toggle between OpenAI API-based transcription and local model inference.
- Advanced Features:
  --- Improve accuracy with speaker diarization (via WhisperX or pyannote.audio)
  --- Support for live-stream audio processing
  --- GUI enhancements for real-time text display
  --- Add transcription evaluation metrics or interface controls

---

##  Notes & Considerations
  --- This tool currently requires an active OpenAI API key (paid tier).
  
  --- Whisper is a state-of-the-art multilingual speech recognition model known for its robustness across various accents and background noise conditions
    
