---
title: "Task 06 — Deep Fake Audio Interview"
output: github_document
---

# Task 06: Deep Fake Audio Interview

This repository contains all materials for generating a **short, human-sounding, street-style audio interview** based on the Task 5 narrative.  
The repo is **reproducible**, uses **free tools only**, and is designed to run easily in **Google Colab**.

---

##  What’s included

- **Task_6_Interview script.docx**  
  Finalized Host ↔ Analyst dialogue with disclosure up front.  
  Adapted directly from Task 5 narrative into natural, back-and-forth prompts and follow-ups.

- **audio_file_creation_python_script.py**  
  Self-contained, Colab-friendly script that:
  - Installs minimal dependencies + FFmpeg  
  - Downloads **Piper TTS** binary and two free voices (HOST & GUEST)  
  - Synthesizes each line into audio clips  
  - Stitches with gentle pauses/crossfades + normalized levels  
  - Exports as a single MP3 file  

- **AI Audio Interview.mp3**  
  The finished export: a two-voice synthetic interview.

---

## Quick Start (Google Colab Recommended)

1. Open **Google Colab** → *File* → *Upload* and select `audio_file_creation_python_script.py`.
2. Run the cell(s).  

The script will:  
- Install FFmpeg and Piper TTS  
- Parse the dialogue from `Task_6_Interview script.docx`  
- Generate line-by-line audio (Host + Guest)  
- Stitch with crossfades and normalization  
- Export **AI Audio Interview.mp3** (download prompt will appear)

---

## Customizing the Audio

Inside `audio_file_creation_python_script.py`:

- **Voices** → Swap the HOST/GUEST model URLs for other Piper voices  
- **Pace** → Adjust `length_scale` (`↑ = slower speech`)  
- **Pauses** → Change `sentence_silence` or crossfade length (e.g., 35–50 ms)  
- **Loudness** → Modify pre-export gain (e.g., `−1.5 dB`)  
- **Quality** → Increase MP3 bitrate (e.g., `192k → 256k`)  

To change the dialogue, edit **Task_6_Interview script.docx** and re-run the script.

---

##  Interview Coverage

The audio captures a **concise sidewalk conversation** summarizing Task 5 results:

- Results roughly matched expectations (variance small)  
- Scoring leaned top-heavy; spreading creation reduces predictability  
- Tight games hinged on **trainable margins** (end-game, special teams)  
- In fast, high-possession games, **shot selection matters more**  
- **Action plan**: diversify creation, rehearse end-game sets, manage tempo  

---

## Ethics & Disclosure

- The audio **clearly states** it is AI-generated for **academic research** (intro/outro).  
- No imitation of real people — **only synthetic voices** are used.  
- Both script & code are included for **transparency and reproducibility**.

---

## Troubleshooting

- **Dependency warnings in Colab** → Safe to ignore, just run as-is  
- **“Binary not found” / download errors** → Re-run the cell (Colab may drop temp files)  
- **Clicks between lines** → Increase crossfade (e.g., 50 ms)  
- **Speech too fast/slow** → Adjust `length_scale`  
- **Audio too quiet/loud** → Modify gain before export  

---

