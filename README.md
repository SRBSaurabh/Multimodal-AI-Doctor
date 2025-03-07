# AI Doctor 2.0

**Medical Chatbot with MultiModal LLM (Vision & Voice)**

## Table of Contents

1. [Project Overview](#project-overview)
2. [Tools and Technologies](#tools-and-technologies)
3. [Installing Dependencies](#installing-dependencies)
   - [FFmpeg and PortAudio](#installing-ffmpeg-and-portaudio)
   - [Python Virtual Environment](#setting-up-a-python-virtual-environment)
4. [Project Phases & Execution](#project-phases-and-python-commands)
5. [Technical Architecture](#technical-architecture)
6. [Future Improvements](#future-improvements)

---

## Project Overview

**AI Doctor 2.0** is a **medical chatbot** leveraging **multimodal LLMs** to enable **vision and voice-based interaction**. The project includes **image-based medical diagnostics, speech-to-text transcription, and text-to-speech conversion**, offering an interactive healthcare AI assistant.

---

## Tools and Technologies

- **Groq API** – AI inference
- **OpenAI Whisper** – Speech-to-Text (STT) model
- **Llama 3 Vision** – Vision-based LLM (by Meta)
- **gTTS & ElevenLabs** – Text-to-Speech (TTS)
- **Gradio** – UI for interaction
- **Python** – Core development language
- **VS Code** – Development environment
  
![workflow](https://github.com/user-attachments/assets/31f16a39-5c58-4679-bf18-9891761c7773)

---

## Installing Dependencies

### Installing FFmpeg and PortAudio (Windows)

1. **Download & Extract FFmpeg:**
   - Get the latest **static build** from [FFmpeg Downloads](https://ffmpeg.org/download.html)
   - Extract it to `C:\ffmpeg`
   - Add `C:\ffmpeg\bin` to system **PATH** (Environment Variables)

2. **Install PortAudio:**
   - Download from [PortAudio Downloads](http://www.portaudio.com/download.html)
   - Follow installation instructions

---

### Setting Up a Python Virtual Environment (Windows - Conda)

1. **Create Conda environment:**
   ```bash
   conda create --name ai_doctor python=3.11
   ```
2. **Activate environment:**
   ```bash
   conda activate ai_doctor
   ```
3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## Project Phases and Python Commands

### Phase 1: **Setup the Brain of the Doctor (Multimodal LLM)**
   ```bash
   python brain_of_the_doctor.py
   ```
   - Setup **GROQ API key**
   - Convert **image to required format**
   - Initialize **Multimodal LLM**

### Phase 2: **Setup Voice of the Patient**
   ```bash
   python voice_of_the_patient.py
   ```
   - Setup **Audio Recorder** (FFmpeg & PortAudio)
   - Setup **Speech-to-Text (STT) model** for transcription

### Phase 3: **Setup Voice of the Doctor**
   ```bash
   python voice_of_the_doctor.py
   ```
   - Setup **Text-to-Speech (TTS) model** using **gTTS & ElevenLabs**
   - Convert **Text output to voice**

### Phase 4: **Setup Gradio UI for VoiceBot**
   ```bash
   python gradio_app.py
   ```
   - Deploy **VoiceBot UI with Gradio**

---

## Technical Architecture

```
[User] --> [Voice Input] --> [Speech-to-Text (Whisper)] --> [LLM Processing (Llama 3 Vision)]
      --> [Text Output] --> [Text-to-Speech (gTTS, ElevenLabs)] --> [Voice Response to User]
```

---

## Future Improvements

- **Integrate advanced LLMs** (Paid LLMs for better vision capabilities)
- **Fine-tune vision models** for medical images
- **Add multilingual support** for better accessibility

---
