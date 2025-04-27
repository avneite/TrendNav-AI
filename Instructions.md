# Instructions for Running TrendNav

This guide provides step-by-step instructions to set up, run, and explore **TrendNav** for real-time product trend analysis across Reddit and Amazon.

---

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/trendnav.git
cd trendnav
```

---

## 2. Install Dependencies

Ensure **Python 3.8 or higher** is installed.

```bash
pip install -r requirements.txt
```

---

## 3. Download NLTK Resources

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

---

## 4. Configure AWS SageMaker (Optional for Cloud Deployment)

If running on **Amazon SageMaker**:
- Ensure your **IAM roles** have necessary permissions.
- Upload the project folder to your SageMaker environment.
- Use **SageMaker Studio** or a **notebook instance** for execution.

For **local runs**, SageMaker is **not required**.

---

## 5. Prepare Data Sources

- **Reddit Data**: Configure scraping scripts or Reddit API credentials within the notebook.
- **Amazon Data**: Ensure access to Amazon product data (via APIs or Kaggle datasets).

---

## 6. Run the Streamlit Dashboard

Launch the application locally or on SageMaker:

```bash
streamlit run TrendNav_Final.ipynb
```

This opens the **interactive dashboard** in your default browser.

---

## 7. Dashboard Features

- **Trending Products**: View product trends from Reddit and Amazon.
- **Sentiment Breakdown**: Analyze customer sentiment (positive, neutral, negative).
- **Keyword Relationships**: Explore extracted keywords and grouped phrases.
- **Inventory Mapping**: See how trends map to Amazon inventory using **Sentence-Transformers** and **fuzzy matching**.
- **Filter & Customize**: Adjust views based on sentiment, frequency, or source platform.

---

## 8. Modify or Extend

- **Sentiment Models**: Swap **RoBERTa** with other Hugging Face models.
- **Keyword Extraction**: Tune **KeyBERT** or **NER** settings.
- **Inventory Mapping**: Adjust **cosine similarity thresholds** or fuzzy matching criteria.

---

## Notes

- The project is optimized for **Amazon SageMaker** but works locally for smaller datasets.
- Ensure compatibility with **pyspark** and **Hugging Face Transformers** if running locally.
- For large-scale deployments, SageMaker offers scalable compute power.

---

For issues or feature requests, raise an issue on the repository or contact the project maintainer.
