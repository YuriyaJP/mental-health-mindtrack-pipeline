# Mental Health NLP Pipeline

This project forecasts mental health states, especially early signs of suicidality, from daily journal-style entries using NLP techniques. It aims to detect emotional distress before it escalates into crises.

We focus on fairness-aware forecasting, especially when demographic data is unavailable, by exploring proxy-based methods and tools like Fairlearn.

---

##  Setup

```bash
pip install -r requirements.txt
cp .env.example .env  # Add HuggingFace or OpenAI API keys
```

## Data Sources

| Source                 | Type    | Notes                                  |
|------------------------|---------|----------------------------------------|
| Simulated Journals      | Text    | Synthetic or user-generated daily logs |
| Custom Labels          | CSV     | Includes emotions, suicidal ideation, etc |
| Mental Health Reddit Posts | JSON | Anonymized comments (optional)          |
| External lexicons       | TXT/CSV | NRC, LIWC, PHQ-9 scoring resources     |
