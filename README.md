# online-text/sentiment_analyser

This project involves data collection (web scraping), transformation, and analysis using dbt, Airflow, and NLP models to track sentiment over time for a specific topic (topic agnostic).

Tech stack: dbt, Airflow, PostgreSQL, google-api-python-client, Hugging Face (NLP), Streamlit (dashboard)

Idea: Analyze sentiment for online forums (likely Youtube) and/or for a specific topic (like climate change, political topic, or current event).
* Data Sources: Web-scrape data (Youtube API)  
* dbt Models:
  - clean raw text data, remove spam/duplicates
  - use Hugging Face/BERT to classify sentiment
Aggregate daily/weekly sentiment trends:
* Airflow DAG: Automate data collection & processing every 6-12 hours
* Visualization: Build a dashboard showing sentiment over time (likely in Streamlit)
