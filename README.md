# online-text_sentiment_analysis

This project involves data collection, transformation, and analysis using dbt, Airflow, and NLP models to track sentiment over time for a specific topic (topic agnostic).

Tech stack: dbt, Airflow, PostgreSQL, Tweepy (Twitter API), Pushshift (Reddit API), Hugging Face (NLP), Streamlit (dashboard)

Idea: Analyze sentiment on Twitter/Reddit/other online forums for a specific topic (like climate change, political topic, or current event).
* Data Sources: Scrape data via Tweepy (Twitter) or Pushshift (Reddit).
* dbt Models:
  - clean raw text data, remove spam/duplicates
  - use Hugging Face/BERT to classify sentiment
Aggregate daily/weekly sentiment trends:
* Airflow DAG: Automate data collection & processing every 6-12 hours
* Visualization: Build a dashboard showing sentiment over time (likely in Streamlit)
