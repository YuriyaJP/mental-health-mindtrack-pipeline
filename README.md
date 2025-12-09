# Multimodal Fairness-Aware Mental Health Journaling Agent

A voice journaling assistant that transcribes speech, analyzes vocal tone, and generates safe, helpful reflections and prompts. It uses a small memory window for conversation continuity, runs locally to protect privacy, and includes fairness and robustness checks to ensure consistent performance across accents and audio conditions. The system includes a real-time perception pipeline, a policy-constrained reasoning module, a short-term memory layer, and a fairness and robustness evaluation suite built with Fairlearn.

This project forecasts mental health states, especially early signs of suicidality, from daily journal-style entries using NLP techniques. It aims to detect emotional distress before it escalates into crises.

## System Architecture
User Audio
   |
   v
Audio Preprocessing
   |
   v
Speech-to-Text (ASR)
   |
   v
Prosody Extraction
   |
   v
Multimodal Fusion (text + prosody)
   |
   v
LLM Reasoning (summary + prompts)
   |
   v
Safety Filter
   |
   v
Final Output (reflection + follow-up prompt)

---

##  Setup

```bash
pip install -r requirements.txt
pip install fairlearn librosa sounddevice
```

## Data Sources

| Source                 | Type    | Notes                                  |
|------------------------|---------|----------------------------------------|
| Simulated Journals      | Text    | Synthetic and Franz Kafka's Diaries logs from 1920s (copyright expired) |
| Custom Labels          | CSV     | suicide, ADHD, OCD, depression, Aspebergs, PTSD |
| Mental Health Reddit Posts | JSON | Anonymized comments from 2 datasets  |
