# 🛍️ Retail Sentiment Analyzer | Landmark Group
Turn 30 k multilingual app-store reviews into **actionable KPIs** in 3 clicks.

## Business Question
&gt; Which drivers (price, delivery, app UX, product quality) hurt our NPS the most — and by how much?

## What I Built
1. **Auto-translation** → detects 6 languages, converts to EN (GoogleTranslator)  
2. **Text-cleaning** → emoji, contractions, punct, links removed  
3. **Ensemble scoring** → VADER + RoBERTa (twitter-base) → weighted avg  
4. **Likert bucket** → Very Satisfied → Very Dissatisfied (business language)  
5. **Category tagger** → 10 retail facets (price, delivery, returns, app, etc.) via synonym dictionary  
6. **CSV export** → ready for Tableau / Power BI

## Key Insights (sample 500 rows)
| Driver | % Negative | Example Quote |
|---|---|---|
| **Delivery** | 42 % | “very horrible experience… they even do not deliver” |
| **Price** | 38 % | “very bad high price” |
| **App UI** | 31 % | “useless application uses your money” |

Likert distribution:  
- Very Satisfied 22 %  
- Satisfied 31 %  
- Neutral 18 %  
- Dissatisfied 15 %  
- Very Dissatisfied 14 %  

→ **Priority matrix**: fix delivery SLA & price-perception messaging first.

## How to Run
Open in Colab (zero install):  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/retail-sentiment-analyzer/blob/main/Sentiment_Analysis_Lifestyle.ipynb)

Or local:
```bash
pip install -r requirements.txt
jupyter notebook Sentiment_Analysis_Lifestyle.ipynb
