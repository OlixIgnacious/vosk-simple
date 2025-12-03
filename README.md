# Vosk Simple Demo

A minimal, clean Python example showing how to perform real‑time offline speech recognition using **Vosk** + **sounddevice**.

This repo demonstrates:
- How to load a Vosk speech-to-text model
- How to stream audio from a microphone
- How to perform real-time transcription
- How to handle partial + final results

---

## 🔧 Requirements

Install dependencies:

```bash
pip install vosk sounddevice
```

Download a Vosk model (recommended small English model):

https://alphacephei.com/vosk/models

Example folder structure:

```
vosk-simple/
  main.py
  models/
    vosk-model-small-en-us-0.15/
```

---

## 🎤 Running the Demo

```bash
python main.py
```

If you need to manually select a microphone device, run:

```bash
python list_devices.py
```

Then edit `DEVICE_INDEX` inside `main.py`.

---

## 📁 Files in This Repo

### `main.py`
Main real-time transcription script using:
- `sounddevice.RawInputStream`
- `KaldiRecognizer`
- Live partial & final transcription printing

### `list_devices.py`
Helper script to print all audio devices to help configure mic input.

---

## 📝 Notes

- Vosk models run fully **offline**.
- Real-time accuracy improves with a larger model.
- For Indian English accents, use the model:
  `vosk-model-small-en-in-0.4`

---

## 📜 License
MIT License.
