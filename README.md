# Kutub Sittah JSONL (The 6 Authentic Hadeeth Books)

This repository contains the six major books of Hadeeth (Al-Kutub Al-Sittah) in **JSONL (JSON Lines)** format, extracted from the Shamela library. 

This dataset is designed for developers, researchers, and students who need a machine-readable, offline-friendly version of these distinct texts for building Islamic apps, search engines, or AI models.

## 📂 Datasets Included

| File Name | Book Name | Approx. Pages | Source Text |
|-----------|-----------|---------------|-------------|
| `offline_sahih_bukhari.jsonl` | **Sahih Al-Bukhari** | ~11,000 | Sahih Al-Bukhari (Shamela ID 735) |
| `offline_sahih_muslim.jsonl` | **Sahih Muslim** | ~7,500 | Sahih Muslim (Shamela ID 1727) |
| `offline_sunan_abu_dawood.jsonl` | **Sunan Abu Dawood** | ~7,200 | Sunan Abi Dawood (Shamela ID 1726) |
| `offline_jami_at_tirmidhi.jsonl` | **Jami` At-Tirmidhi** | ~6,600 | Jami` At-Tirmidhi (Shamela ID 7895) |
| `offline_sunan_an_nasai.jsonl` | **Sunan An-Nasa'i** | ~8,300 | Sunan An-Nasa'i (Shamela ID 829) |
| `offline_sunan_ibn_majah.jsonl` | **Sunan Ibn Majah** | ~5,900 | Sunan Ibn Majah (Shamela ID 1198) |

## 🛠 Data Structure
Each line in the `.jsonl` files is a valid JSON object representing a single page or significant section of the book:

```json
{
  "id": "1726-1",
  "body": "Arabic text of the Hadeeth or Chapter...",
  "foot": "Footnotes and commentary (if available)..."
}
```

*   **`id`**: Unique identifier (BookID-PageNumber).
*   **`body`**: The main text (Matn).
*   **`foot`**: Footnotes (Hashiya/Sharh) often containing critical grading or explanation.

## 🚀 Usage Example (Python)

```python
import json

with open('offline_sahih_bukhari.jsonl', 'r', encoding='utf-8') as f:
    for line in f:
        data = json.loads(line)
        print(f"Page {data['id']}: {data['body'][:50]}...")
```

## 🤲 Request for Dua
I ask Allah (`Subhanahu Wa Ta'ala`) to accept this humble effort and make it a means of benefit for the Ummah. 

**Please include the author (Hassan Musthafa) and all those who contributed to this work in your righteous Duas.**

May Allah make it a Sadaqah Jariyah (continuous charity) and a source of guidance.

## 📜 License
This data is provided mainly for educational and development purposes. Please respect the original source attribution (Shamela).
