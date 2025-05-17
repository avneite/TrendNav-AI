# TrendNav AI - Social Signal-Driven Product Trend Discovery (Opportunity Scanner) for E-commerce Sellers 


**TrendNav AI** is an AI-powered system designed to help small and mid-sized e-commerce sellers identify emerging product trends early — before they gain traction on major marketplaces. By continuously **monitoring social media signals (such as Reddit and Amazon)**, TrendNav AI uncovers high-demand opportunities and highlights areas where sellers can optimize based on inventory availability. Leveraging state-of-the-art NLP and marketplace mapping, the system delivers timely, actionable insights that **enable smarter listing strategies, better sourcing decisions, and improved inventory planning**. It aggregates conversations from **Reddit** and **Amazon**, identifies trending products, and assesses customer sentiment. The insights are visualized through an interactive **Streamlit dashboard**. This project runs on **Amazon SageMaker**, ensuring scalable, cloud-based processing and model inference for large datasets.


## Key Features

- Aggregate data from Reddit and Amazon.
- Perform sentiment analysis using **RoBERTa** to classify intent (positive, negative, neutral).
- Extract keywords via **KeyBERT** (MiniLM) for Reddit and **NER** (RoBERTa) for Amazon.
- Group related phrases using **spaCy** and **TF-IDF**.
- Score trends by combining keyword frequency and sentiment.
- Map trends to Amazon inventory using **Sentence-Transformers** and fuzzy matching.
- Visualize insights via a **Streamlit dashboard**.

## Installation

Clone this repository:

```bash
git clone https://github.com/yourusername/TrendNav-AI.git
cd TrendNav-AI
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download required NLTK resources:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

## How It Works

1. **Data Aggregation**: Collect Reddit threads and Amazon product data.
2. **Sentiment Analysis**: Classify sentiment using **RoBERTa**.
3. **Keyword Extraction**: Use **KeyBERT** (Reddit) and **NER** (Amazon).
4. **Phrase Grouping**: Consolidate related terms with **spaCy** and **TF-IDF**.
5. **Trend Scoring**: Combine keyword frequency and sentiment for scoring.
6. **Marketplace Mapping**: Match trends to inventory via **Sentence-Transformers** and fuzzy matching.
7. **Visualization**: View trends and insights on a **Streamlit dashboard**.

## Usage

Run the Streamlit app:
Access through link : https://trend-navai-app-demo.streamlit.app/
or 
use the below code:
```bash
streamlit run treamlit-nav-dash.py
```

Explore trending products, sentiment insights, and inventory mappings interactively through the dashboard.

## Deployment

- Designed to run on **Amazon SageMaker** for scalable processing and model inference.
- Can also be executed locally for smaller datasets or testing.

## Libraries Used

- **pandas**, **numpy**, **matplotlib**, **altair** (data handling & visualization).
- **Hugging Face Transformers**, **Sentence-Transformers**, **NER Based BERT** (NLP models).
- **spaCy**, **TF-IDF**, **pyspark** (NLP preprocessing & scaling).
- **fuzzywuzzy / rapidfuzz** (fuzzy matching).
- **streamlit** (dashboarding).

## 📌 Contributor Note

This repository was originally created and maintained by **Auroshika Mohanty** as part of a team project at the Carlson School of Management.  
You can find the original source here: https://github.com/aurosikha-mohanty/TrendNav-AI  
This fork is for visibility and documentation of my personal contributions to the project.

### 👤 My Key Contributions:
- Implemented **Named Entity Recognition (NER)** using RoBERTa for Amazon product mentions  
- Developed **phrase grouping logic** using **spaCy** and **TF-IDF**  
- Contributed to the **trend scoring algorithm** based on sentiment polarity and keyword frequency  
- Enhanced the keyword extraction process using **KeyBERT** and entity recognition techniques  
- Supported the creation of **insights visualized in the Streamlit dashboard**

> _This fork is intended for showcase and personal portfolio purposes only._

