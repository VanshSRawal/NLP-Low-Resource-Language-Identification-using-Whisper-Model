# Spoken Language ID (Mini-Project) — Whisper (Faster-Whisper)

A light, CPU-friendly **spoken language identification** (LID) mini-project built on the pre-trained **Whisper** model via **faster-whisper**.  
Upload short audio clips (5–10s) and get the **predicted language (ISO 639-1 code)** with a **confidence score**.  
Designed to demonstrate a practical **deep-learning** NLP/speech pipeline in minutes.

---

## ✨ Features
- 🔊 Input: `.wav` / `.mp3` / `.m4a` short clips (5–10s)
- 🧠 Model: Whisper **small** (fast) or **medium** (more accurate), both on **CPU**
- 📈 Output: language code (e.g., `mr`, `hi`, `bn`) + confidence; optional top-k bar chart
- 🧪 Batch mini-eval: run a subset of files and summarize predictions
- 🧰 100% reproducible in **Google Colab** or locally (Python)

---

## 🚀 Quickstart (Local)

1. **Install dependencies**
```bash
sudo apt-get update && sudo apt-get install -y ffmpeg
pip install -r requirements.txt
```

2. **Run the notebook**
Upload `app.ipynb` to Colab or run locally using Jupyter.  
Upload 3–5 test audio clips and visualize the predicted language probabilities.

---

## 🧠 Deep Learning Technique
- Transformer-based **Whisper** model (Encoder–Decoder architecture).
- Pre-trained on ~680k hours of multilingual speech data.
- Used via **transfer learning** for inference (no retraining needed).

---

## 🏗️ Architecture Overview
```
Audio Clip → (Auto Preprocess: decode, 16 kHz mono, VAD)
          → Whisper Encoder (features)
          → Language Token Classifier
          → Predicted Code + Confidence
          → Visualization (bar chart/table)
```

---

## 📊 Dataset
- **Source:** Marathi Speech Corpus (SLR-64) from [OpenSLR.org](https://openslr.org/64/)  
- **Languages tested:** Marathi, Hindi, Bengali, Sinhala  
- **Clip length:** 5–10 seconds each

---

## 🧹 Pre-processing
- Automatically handled by **faster-whisper**:
  - Decoding and resampling to 16 kHz mono
  - Normalization and silence trimming (VAD)
- Optional: trim to 5s for faster inference

---

## 📚 References
- OpenSLR datasets: https://openslr.org  
- Faster-Whisper: https://github.com/guillaumekln/faster-whisper  
- Whisper: https://github.com/openai/whisper  
- Book: Jurafsky & Martin, *Speech and Language Processing (3rd Ed)*  

---

## 👥 Team
Group Mini-Project — NLP Course  
Members (add your names and roll numbers)  
Batch: 2025  

---

## 🧩 Learnings
- Understood how pre-trained deep learning models can be reused for language identification.  
- Learned about Whisper’s Transformer architecture and zero-shot multilingual capability.  
- Explored dataset handling, preprocessing, and evaluation in Colab.  
- Gained hands-on experience visualizing predictions and managing reproducible notebooks.  
- Learned trade-offs between model size, inference speed, and accuracy in real-world applications.

---

## 🗺️ Future Scope
- Integrate speech-to-text transcription alongside language ID.  
- Add Streamlit UI for a web-based demo.  
- Extend dataset to more low-resource Indian languages.  
- Experiment with fine-tuning or few-shot adaptation.

---
